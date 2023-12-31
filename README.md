🔑 MinIO Keygenerator
===

[![Go Report Card](https://goreportcard.com/badge/github.com/iwittkau/minio-keygen)](https://goreportcard.com/report/github.com/iwittkau/minio-keygen)

This is a simple [MinIO](https://min.io) Access and Secret Key generator.

# Why?

Minio stopped auto-generating these secrets, so I wrote this little tool.

# Security

The generator is very simple, any security flaw should be obvious. If you have any concerns, please open an issue.

This generator uses Go's `crypto/rand` which implements a cryptographically secure random number generator.

# Installation

```
go install github.com/iwittkau/minio-keygen@latest
```

# Usage

```
$ minio-keygen
MINIO_ROOT_USER=PLEASE-DONT-USE-THIS
MINIO_ROOT_PASSWORD=thisIsOnlyAnExampleYouShouldUseTheActualOutput
```

You can also create an `.env` file from the output with:

```
$ minio-keygen > .env
```
