# aws-apigateway-api-s3-binary
AWS API Gateway API supporting multi-part download from Amazon S3

# Sample Invocations
## Simple file download
`curl https://<apigateway-invoke-url>/<stage>/<bucket>/<filename> --output <filename>`


## Multi-part file download
Downloading parts
```
curl "https://<invoke-url>/<stage>/<bucket>/<filename>?partNumber=1" --output <filename>_1
curl "https://<invoke-url>/<stage>/<bucket>/<filename>?partNumber=2" --output <filename>_2
curl "https://<invoke-url>/<stage>/<bucket>/<filename>?partNumber=n" --output <filename>_n
```

Joining the parts
`cat <filename_*> > <filename>`
