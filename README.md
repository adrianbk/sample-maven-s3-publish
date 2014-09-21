### A simple maven project to publish artifacts to AWS S3

1. Provide an environment variable (or maven property) 'G_S3_BUCKET' with the aws s3 bucket to deploy to


2. Add the following repository servers to `~/.m2/settings.xml`

```xml 
<servers>
    <server>
        <id>gradle-aws-release</id>
        <username><your aws access key></username>
        <password><your aws secret key></password>
    </server>
    <server>
        <id>gradle-aws-snapshot</id>
        <username><your aws access key></username>
        <password><your aws secret key></password>
    </server>
</servers>
```

3. Deploy to s3: `mvn deploy`