FROM golang:1.23.4-alpine

WORKDIR /code

RUN go install github.com/air-verse/air@latest

COPY application/go.mod /code/
COPY application/go.sum /code/
RUN go mod download

CMD ["air", "-c", ".air.toml"]
