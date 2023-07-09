build:
	GOARCH=amd64 GOOS=linux go build -o artifact/go-container-test
.PHONY: build

test:
	go test ./...
.PHONY: test

clean:
	rm -rf artifact
.PHONY: clean
