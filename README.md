# Creating a static webiste using Amazon S3
# Description
These steps will show you how to create a static website utilizing the functions of an S3 bucket and a text editor (Atom).  
# Steps
### Creation of S3 bucket
1. Create an S3 bucket (name of bucket must be gloablly unqiue). When creating the bucket, make sure to uncheck the `Block all public access` box and then check the box for acknowleldging the objects within the bucket can be publicly accessible. 
2. After the bucket is created, select the bucket and click on the `Properties` tab. Scroll down to `Static website hosting` and click on `Edit`.
3. Enable static website hosting and further down the page look for `index document` and input "index.html". Next is optional and its for the `error document` where you will input "error.html" and then save the changes made. 
4. Next locate the `Permissions` tab and add in a bucket policy to make your bucket completely publicly accessible. The bucekt policy to allow this can be found in https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteAccessPermissionsReqd.html
5. In the resource line of the bucket policy, the name of your bucket must be included in between the ":" and "/". For example the bold letters in this text - "arn:aws:s3:::**Bucket-Name**/*".

### Creating index and error documents
1. Using Atom, or any other text editor, create an index document like the one seen below. 
[![error-html.png](https://i.postimg.cc/GtFjZ9Q5/error-html.png)](https://postimg.cc/y3N9R12m)
