# AWS-Transcribe-S3

Source:
Amazon S3

Bucket:Input
venkat-s3-transcribe

Event:
s3:ObjectCreated:*

Destination:
serverless-transcription-trigger

## AWS Services Used

- Amazon S3
  - Input audio storage
  - Transcription output storage

- AWS Lambda
  - Event-driven processing
  - Python runtime

- Amazon Transcribe
  - Speech-to-text transcription

- AWS IAM
  - Lambda execution role
  - Least-privilege permissions

- Amazon CloudWatch
  - Lambda execution logs
  - Troubleshooting and monitoring

Architecture:

Audio Upload
     │
     ▼
venkat-s3-transcribe
     │
     │ s3:ObjectCreated:*
     ▼
AWS Lambda
serverless-transcription-trigger
     │
     │ StartTranscriptionJob
     ▼
Amazon Transcribe
     │
     ▼
venkat-s3-transcribe-output
     │
     ▼
Transcript JSON
