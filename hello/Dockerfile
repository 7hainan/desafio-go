FROM golang:alpine AS builder

ENV WORKFOLDER_NAME hello
WORKDIR /go/src/hello

COPY . .

RUN CGO_ENABLED=0 go build -o /hello hello.go

FROM scratch
COPY --from=builder /hello /hello
CMD ["/hello"]








