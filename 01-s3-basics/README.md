# 1.1 — S3 Basics

Created my first S3 bucket, uploaded an object, and verified the default
security model.

## What I built
- Bucket: `hashir-networked-foundation-2026` (region: us-east-1)
- Type: General purpose, global namespace
- Uploaded a test object (`hello.txt`)
- Left all security defaults ON

## Key concepts learned
- **Bucket names are globally unique** — because each bucket maps to a public
  DNS address (`bucket.s3.amazonaws.com`). Unlike EC2/VPC, which are
  account+region scoped.
- **Objects are private by default.** Access = *identity of requester* ×
  *permissions granted*. The object existing says nothing about who can read it.
- **Block Public Access** is a categorical safety wall at the bucket level —
  the reason S3 leaks are always misconfiguration, never a default.
- **Default encryption (SSE-S3)** — every object encrypted at rest, AWS-managed keys.
- **S3 has no real folders** — the "key" is the full path; slashes just look
  like folders in the console.
- **Three ways to address an object:** Object URL (browser), S3 URI (CLI/SDK),
  ARN (IAM policies).

## The security test
Copied the object's public URL into a browser → received `AccessDenied` (XML).
Proof the object is stored but not publicly readable — exactly as intended.

## Deliberately skipped (revisit later)
- Bucket versioning → own sub-project
- Bucket policies / static website hosting → later S3 work
- SSE-KMS encryption → when covering KMS
- Lifecycle rules + storage classes → cost optimization
- Tags → cost tracking across resources
