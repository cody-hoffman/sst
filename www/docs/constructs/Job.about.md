The `Job` construct is a higher level CDK construct that makes it easy to perform long running jobs.

## Examples

### Creating a Job

```js
import { Job } from "@serverless-stack/resources";

new Job(stack, "MyJob", {
  handler: "src/job.main",
});
```

### Setting additional props

```js
new Job(stack, "MyJob", {
  handler: "job.main",
  srcPath: "services",
  timeout: "30 minutes",
  memorySize: "3 GB",
  config: [STRIPE_KEY, API_URL],
  permissions: ["ses", bucket],
});
```