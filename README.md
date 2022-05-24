### [***0. Spring Initializr***](https://start.spring.io/#!type=maven-project&language=java&platformVersion=2.7.0&packaging=jar&jvmVersion=11&groupId=com.example&artifactId=batch&name=batch&description=Demo%20project%20for%20Spring%20Batch&packageName=com.example.batch&dependencies=batch,lombok,jdbc,mysql,h2,postgresql,mybatis)

### [***1. 배치란***](https://github.com/jojoldu/spring-batch-in-action/blob/master/1_%EB%B0%B0%EC%B9%98%EB%9E%80.md)

### [***2. Job생성***](https://github.com/jojoldu/spring-batch-in-action/blob/master/2_Job%EC%83%9D%EC%84%B1.md)

Start MySQL with Docker(add `--platform linux/amd64` for Mac with Apple Chip)
```
docker run -d \
  --name mysql-batch-job-repository \
  -p 3306:3306 \
  -e MYSQL_USER=jojoldu \
  -e MYSQL_PASSWORD=jojoldu1 \
  -e MYSQL_ROOT_PASSWORD=jojoldu1 \
  -e MYSQL_DATABASE=spring_batch \
  mysql
```

### [***3. Spring Batch 메타 테이블 엿보기***](https://github.com/jojoldu/spring-batch-in-action/blob/master/3_%EB%A9%94%ED%83%80%ED%85%8C%EC%9D%B4%EB%B8%94%EC%97%BF%EB%B3%B4%EA%B8%B0.md)

### [***4. Spring Batch Job Flow***](https://github.com/jojoldu/spring-batch-in-action/blob/master/4_BATCH_JOB_FLOW.md)

### [***5. Spring Batch Scope & Job Parameter***](https://github.com/jojoldu/spring-batch-in-action/blob/master/5_SCOPE.md)

### [***6. Chunk 지향 처리***](https://github.com/jojoldu/spring-batch-in-action/blob/master/6_CHUNK.md)

`Spring Batch에서의 Chunk란 데이터 덩어리로 작업 할 때 각 커밋 사이에 처리되는 row 수를 얘기합니다.`

![](https://github.com/jojoldu/spring-batch-in-action/blob/master/images/6/chunk-process.png)
`
Setting a fairly large page size and using a commit interval that matches the page size should provide better performance.
`
