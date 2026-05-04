## Kinesis Data Streams vs SQS

| | KDS | SQS |
|---|---|---|
| Real-time | Instant |  Near instant |
| Order guarantee |  Per partition |  (FIFO only) |
| Multiple consumers | Simultaneous |  One at a time |
| Retention | 7 days (max 365) | 14 days |
| Delete after read |  Retained |  Auto deleted |
| Throughput | Very high | High |
| Use case | Stream analytics | Task queue 

## S3 direct input vs Firehose

# Direct
- Need to write a code
- additional error handling
- File format handling
- Thus fits when data(e.g log) are small scale

# Firehose -> S3
- No code
- Automatic bufferig, partitioning
- Fault tolerance

## Why Firehose?

If 1 million logs per second:

**Direct to S3**
- 1 million PUT requests
- S3 cost explodes
- Complex error handling code needed

**Firehose → S3**
- Buffers for 60 seconds then uploads at once
- Minimizes S3 PUT requests
- Fully managed 
