FROM 192.168.1.45:80/noval/java:8
USER root
ENV TZ Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
ADD ./target/novel-admin-3.5.4.jar /root
ENV dburl=""
ENV username=""
ENV	password=""
ENTRYPOINT ["sh","-c","java -Dspring.datasource.url=${dburl} -Dspring.datasource.username=${username} -Dspring.datasource.password=${password} -jar novel-admin-3.5.4.jar"]
