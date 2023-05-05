FROM golang:latest AS builder
WORKDIR /app
COPY execute.go /app
RUN go build -o app execute.go


FROM scratch
COPY --from=builder /app .
CMD ["./app"]
