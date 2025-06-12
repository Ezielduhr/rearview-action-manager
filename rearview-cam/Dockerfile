FROM golang:1.24-alpine

WORKDIR /app

COPY go.mod go.sum ./
RUN go mod download

COPY *.go ./

RUN CGO_ENABLED=0 GOOS=linux go build -o /time-management-tool-api

EXPOSE 8080

CMD ["/time-management-tool-api"]
