FROM golang:1.14-alpine

WORKDIR /app/go-server

ENV GOPROXY=https://goproxy.io

COPY go.* ./
RUN go mod download

COPY . .

RUN GOOS=linux go build -ldflags "-s -w" -o main .

CMD ["./main"]