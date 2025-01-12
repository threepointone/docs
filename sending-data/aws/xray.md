---
label: AWS X-Ray Traces
order: -2
---

# AWS X-Ray Traces

[AWS X-Ray](https://aws.amazon.com/xray/) enables developers to generate and collect traces across their distributed services. In order to gain visibility into their applications, developers can use AWS X-Ray to trace requests as they travel through their application, and collect data about the performance of their application.

Baselime enables you to ingest this tracing data and make it available for analysis and troubleshooting.

![AWS X-Ray trace diagram in Baselime](../../assets/images/illustrations/sending-data/xray-diagram.png)
![AWS X-Ray trace waterfall in Baselime](../../assets/images/illustrations/sending-data/xray-waterfall.png)

---

## How it works

Once Baselime is connected to an AWS Account, it will periodically poll your AWS account for new traces and automatically ingest them into your Baselime dataset.

![Sending X-Ray Traces to Baselime](../../assets/images/illustrations/sending-data/xray.png)

---

## Troubleshooting

If you're having trouble sending data from AWS X-Ray to Baselime, here are a few things to check:

- Verify that your AWS account is correctly connected to Baselime and you receive data in other datasets such as [CloudWatch Metrics](./cloudwatch-metrics.md) or [CloudTrail Events](./cloudtrail.md)
- Check that the Baselime IAM user has the appropriate permissions to access AWS X-Ray
- Make sure that your applications emit X-Ray traces and you can view the traces in the X-Ray section of the AWS Console

!!!
Baselime will ingest traces emmitted by the AWS X-ray service. To capture HTTP calls or AWS Service calls, you must manually instrument your code with the AWS X-Ray SDK. Read more in the [AWS X-Ray docs](https://docs.aws.amazon.com/xray/latest/devguide/xray-nodejs.html). 
!!!
