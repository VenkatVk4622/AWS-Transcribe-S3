# AWS-Transcribe-S3

Source:
Amazon S3

Bucket:Input
venkat-s3-transcribe

Event:
s3:ObjectCreated:*

Destination:
serverless-transcription-trigger


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
