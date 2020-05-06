# minio-client
- refs: git@github.com:tshst/golang.git

## download and setting

```
cd minio-client
GO111MODULE=on go get github.com/minio/minio-go/v6
go mod init minio-client

### you should to change the following settings in file-uploader.go. 
endpoint := "10.102.26.149:9001"
accessKeyID := "minio"
secretAccessKey := "minio123"
```

## file upload to minio

```
zip golden-oldies.zip ./golden-oldies
go run file-uploader.go
```

## check to access minio
- refs: https://github.com/minio/mc#example---minio-cloud-storage

```
./mc config host add minio http://10.102.26.149:9001 minio minio123
./mc ls minio/mymusic
```

- Make sure the file you created has been uploaded.
