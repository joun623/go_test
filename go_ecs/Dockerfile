FROM golang:1.13-alpine3.12 as build

ENV GOPATH /go

RUN apk add --update --no-cache git

COPY . /go/src
WORKDIR /go/src

RUN go build -o go-container-test .

FROM alpine:3.12

RUN mkdir /app
WORKDIR /app
COPY --from=build /go/src/go-container-test /app/go-container-test

CMD ["/app/go-container-test"]