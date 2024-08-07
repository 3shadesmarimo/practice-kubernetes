FROM openjdk:11 AS buildstage
COPY . /app
WORKDIR /app
RUN javac hello.java

FROM openjdk:11-jre-slim
COPY --from=buildstage /app/hello.class /app/
WORKDIR /app
CMD java hello