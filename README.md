# Read Me First
This repo exists to demonstrate a bug where adding sleuth can cause tests with @DirtiesContext to fail. It is similar to https://github.com/spring-cloud/spring-cloud-sleuth/issues/1450. 

# Reproduce
Just run mvn clean install. The second test will fail. To get passing tests again, use older version of sleuth 2.1.0 (uncomment dep in pom.xml)

# Note
This repository is using Spring Cloud Gateway demonstrates the bug with Spring Cloud Gateway. It also requires Spring Cloud Gateway 2.2.1 (Hoxton SR1). If we use 2.2.0 then the tests will pass again. But I think the change in Spring Cloud Gateway is valid. The commit present in SCG  2.2.1 is https://github.com/spring-cloud/spring-cloud-gateway/commit/1e263bbc860a3c5a32b4b6abd540116a9496d3a6. But its just an example where we publish in elastic pool during an onApplicationEvent callback.
