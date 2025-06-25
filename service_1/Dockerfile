FROM golang:alpine
WORKDIR /app
COPY . .
RUN go build -o service_1
EXPOSE 5000
CMD ["./service_1"]
