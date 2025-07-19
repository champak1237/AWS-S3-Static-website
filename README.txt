📌 How to Host this on AWS S3

1. Go to https://console.aws.amazon.com and login.
2. Create a new S3 bucket (example: college-admission-demo).
3. Uncheck "Block all public access" during bucket creation.
4. Upload index.html to the bucket.
5. Go to "Properties" > Enable Static Website Hosting.
   - Set index document: index.html
6. Go to "Permissions" > Bucket Policy and paste this:

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadForWebsite",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::college-admission-demo/*"
    }
  ]
}

(Note: Replace `college-admission-demo` with your actual bucket name)

7. Get the Website URL under Static Website Hosting section.

✅ Your project is now live!
