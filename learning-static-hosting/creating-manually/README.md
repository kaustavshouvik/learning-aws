1. Create a S3 bucket, default settings.
2. Upload the `index.html` file.
3. Create CloudFront distribution.
   1. Use original access control.
4. Copy bucket policy to s3.
5. Go to URL provided by the CloudFront distribution.
   1. Since public access is not allowed in S3, the URL should be used with the object path -> `<cf-dist-id>.cloudfront.net/index.html`.

---

### Testing directories

Objective: If I upload two different directories `dir-a` and `dir-b` both having an `index.html`. I should be able to view those two rendered pages using URLs `dir-a/index.html` and `dir-b/index.html` respectively.

#### Steps followed:

1. Uploaded the 2 directories to S3.

#### Conclusion:

Worked as expected. I was able to visit `<cf-dist-id>.cloudfront.net/dir-a/index.html` and got rendered html for dir-a's index.html.
