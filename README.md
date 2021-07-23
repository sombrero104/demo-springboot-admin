
# Spring Boot Admin

<br/>

## 1. Admin
- Admin URL: http://localhost:8080

어드민 서버에 의존성을 추가해준다.

    <dependencies>
        <dependency>
            <groupId>de.codecentric</groupId>
            <artifactId>spring-boot-admin-starter-server</artifactId>
            <version>2.4.0</version>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
            <version>2.4.0</version>
        </dependency>
    </dependencies>
    
아래 클라이언트 설정까지 한 후 어드민 URL로 접속하면 대시보드를 확인할 수 있다. 
<br/><br/>

## 2. Client 
- Client URL: http://localhost

클라이언트에는 클라이언트 의존성을 추가해준다.

    <dependencies>
        <dependency>
            <groupId>de.codecentric</groupId>
            <artifactId>spring-boot-admin-starter-client</artifactId>
            <version>2.4.0</version>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
            <version>2.4.0</version>
        </dependency>
    </dependencies>
<br/>

클라이언트의 application.properties 파일을 만들고 아래와 같이 설정한다.<br/>
클라이언트의 포트를 80으로 바꾸고, 접근을 오픈할 어드민 URL을 설정한다.  <br/>
<pre>
server.port=80

management.endpoints.web.exposure.include=*
spring.boot.admin.client.url=http://localhost:8080
</pre>

<br/><br/><br/><br/>
