# document-automation-aws
This code is used to automate document text detection as well as extraction of the text in the document by AWS Textract and Comprehend.
It uses 2 Lambda Functions.
lambda-trigger-s3-upload is waiting to be triggered by a file upload to specific S3 bucket which then sends a message to SQS on the second lambda "processSQSMessage".
Which then processes the document no matter if its .pdf .jpeg etc. It processes it trough Textract and Comprehend and gives you the entities and all the information in a structured .json file.

The function is still in progress so i'm happy to take any feedback as i'm new to python.
