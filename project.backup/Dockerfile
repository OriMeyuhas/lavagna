FROM maven:3.8.6-openjdk-8 as builder
WORKDIR /app
COPY . .

FROM openjdk:8-jre-alpine
COPY --from=builder /app/target /app/target
WORKDIR /app/target
ENTRYPOINT [ "./entrypoint.sh" ]