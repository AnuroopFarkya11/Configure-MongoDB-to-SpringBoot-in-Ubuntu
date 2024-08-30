# Configure-MongoDB-to-SpringBoot-in-Ubuntu
The detailed instructions for configuring MongoDB with Spring Boot using Spring Data MongoDB in Ubuntu.

Steps to configure and run mongoDB 
Start Mongo DB
Open terminal 
Run a command to start mongo service 
sudo service mongod start
Then, type to get localhost url and port 
mongosh

Configure MongoDB
Navigate to resources/application.properties
Paste the below code 
spring.data.mongodb.host=localhost
spring.data.mongodb.port=27017
spring.data.mongodb.database=your_database_name

Add dependency to pom.xml
 <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-mongodb</artifactId>
            <version>3.3.3</version>
 </dependency>

Create a repository(interface) and extend MongoRepository<Pogo,DataType of id>   
public interface JournalEntryRepository extends MongoRepository<JournalEntity, ObjectId> {
}
