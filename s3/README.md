TO PERFORM CRUD OPERATIONS ON S3 USING BOTO3 LIBRARY:

PYTHON :(python --version ): Python 3.8.10

INSTALL BOTO3,S3FS  LIBRARIES :

	pip3 install boto3

	pip3 install s3fs

CREATING SECRET KEY,ACCESS KEY:

	Sign in using user account and in security credentials 

Click on create access key and download the generated csv file consisting of access key and secret key

Through .env file access those keys;

To upload csv into s3 bucket using upload_file():
Syntax: 

s3.Bucket(‘bucket name’).upload_file(filename,key(name of file in bucket))

s3.Bucket('buck81221').upload_file(Filename='Empdata.csv', Key='Empdata.csv')

To upload the file directly from local to s3 :

Syntax: s3.Bucket(‘bucket name’).upload_file(filepath,key(file name in s3))

s3.Bucket('buck81221').upload_file('/home/lenovo/Downloads/input1.txt','input1.txt')

To download object directly into local system :

s3.Bucket(bucketname).download_file(key(name of s3 object),filename(to name file into local system))


