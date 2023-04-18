---
title: "Tear down this lab"
date: 2020-04-24T11:16:09-04:00
chapter: false
pre: "<b>5. </b>"
weight: 5
---

{{% common/EventEngineVsOwnAccountCleanup %}}

### Remove AWS CloudFormation provisioned resources

#### How to delete an AWS CloudFormation stack

If you are already familiar with how to delete an AWS CloudFormation stack, then skip to the next section: **Delete workshop CloudFormation stacks**

{{% common/DeleteCloudFormationStack %}}

#### Delete workshop CloudFormation stacks

1. First delete the **HealthCheckLab** CloudFormation stack
1. Wait for the **HealthCheckLab** CloudFormation stack to complete (it will no longer be shown on the list of actice stacks)
1. Then delete the **WebApp1-VPC** CloudFormation stack

### Remove CloudWatch logs

After deletion of the **WebApp1-VPC** CloudFormation stack is complete then delete the CloudWatch Logs:

1. Open the CloudWatch console at [https://console.aws.amazon.com/cloudwatch/](https://console.aws.amazon.com/cloudwatch/).
1. Click **Logs** in the left navigation.
1. Click the radio button on the left of the **WebApp1-VPC-VPCFlowLogGroup-\<some unique ID\>**.
1. Click the **Actions Button** then click **Delete Log Group**.
1. Verify the log group name then click **Yes, Delete**.

---

## References & useful resources

* [Patterns for Resilient Architecture — Part 3](https://medium.com/@adhorn/patterns-for-resilient-architecture-part-3-16e8601c488e)
* Amazon Builders' Library: [Implementing health checks](https://aws.amazon.com/builders-library/implementing-health-checks/)
* [Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/) (see the Reliability pillar)
* [Well-Architected best practices for reliability](https://wa.aws.amazon.com/wat.pillar.reliability.en.html)
* [Health Checks for Your Target Groups](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/target-group-health-checks.html) (for your Application Load Balancer)

{{< prev_next_button link_prev_url="../4_fail_open/" title="Congratulations!" final_step="true" >}}
With completion of this lab you have learned several best practices. Consider how you can implement these, and update the Well-Architected Review for your workloads: [REL 5  How do you design interactions in a distributed system to mitigate or withstand failures?](https://docs.aws.amazon.com/wellarchitected/latest/framework/a-workload-architecture.html) [REL 11  How do you design your workload to withstand component failures?](https://docs.aws.amazon.com/wellarchitected/latest/framework/a-failure-management.html).
{{< /prev_next_button >}}
