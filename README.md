# aws-apigateway-api-s3-binary
Sample AWS API Gateway API to download Amazon S3 object with support to multi-part

# Sample Invocations
## Simple file download
`curl https://<apigateway-invoke-url>/<stage>/<bucket>/<filename> --output <filename>`


## Multi-part file download
Downloading parts
```
curl https://<invoke-url>/<stage>/<bucket>/<filename>?partNumber=1 --output <filename_1>
curl https://<invoke-url>/<stage>/<bucket>/<filename>?partNumber=2 --output <filename_2>
curl https://<invoke-url>/<stage>/<bucket>/<filename>?partNumber=n --output <filename_n>
```

Joining the parts
`cat <filename_*> > <filename>`
