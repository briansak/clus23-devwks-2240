---
layout: page
title: Importing a Workflow From Github
permalink: /import-workflow/
nav_order: 3
---

### Importing a workflow from Github

> **SHARED ENVIRONMENT ALERT** <br />
> Make sure you uniquely name your workflow after importing!

1. Click back to Workflows and choose the **Import** button.

<img width="1440" alt="image" src="https://user-images.githubusercontent.com/10421515/173710672-bd66daf1-d85d-4586-880c-3007e300f821.png">

2. Choose, Import from **Git** --> **DEVWKS-2240** for Git Repository, **sxo-aws-ir** for File Name, **Updated Keys** for Git Version, and finally **Import as a New Workflow** and click **Import**.

<img width="608" alt="image" src="https://user-images.githubusercontent.com/10421515/216683454-c86c3b07-d757-43be-a77a-bae18d4bf574.png">

3. After importing, it will show up as **Copy(1)-AWS Incident Response**.  Open this newly created workflow.

<img width="1440" alt="image" src="https://user-images.githubusercontent.com/10421515/173711264-43a14855-cc98-45f9-85c6-b1c559343c77.png">

4. Name your workflow **Pod X - AWS Incident Response** replacing the pod number with yours.
<img width="1440" alt="image" src="https://user-images.githubusercontent.com/10421515/173711715-1849e6ac-150d-4a34-9e1e-dbb02ea800fe.png">

5. Replace the variable for **'observable_value'** with the IP address for your pod from the table below.

<img width="1440" alt="observable" src="https://user-images.githubusercontent.com/10421515/217571825-0aa28061-3290-4bfd-a3e5-79fb2094439d.png">

|     |     |
| --- | --- |
| Pod 1: 172.31.22.192 | Pod 11: 172.31.4.177 |
| Pod 2: 172.31.19.34 | Pod 12: 172.31.9.192 |
| Pod 3: 172.31.28.79 | Pod 13: 172.31.2.170 |
| Pod 4: 172.31.7.175 | Pod 14: 172.31.6.32 |
| Pod 5: 172.31.11.48 | Pod 15: 172.31.11.139 |
| Pod 6: 172.31.14.141 | Pod 16: 172.31.5.13 |
| Pod 7: 172.31.9.110 | Pod 17: 172.31.2.231 |
| Pod 8: 172.31.5.98 | Pod 18: 172.31.4.105 |
| Pod 9: 172.31.6.146 | Pod 19: 172.31.0.150 |
| Pod 10: 172.31.13.208 | Pod 20: 172.31.7.250 |

Replace the value for your pod and click save.

<img width="602" alt="observable2" src="https://user-images.githubusercontent.com/10421515/217571749-e5cdd295-e06f-47c6-bdce-2fbf20664553.png">

Note the activites in this workflow that automate many of the steps outlined in the AWS EC2 Incident Response Guide.

> * Enables Termination Protection on the instance
> * Sets a restricted Security Group limiting access
> * Removes it from any Auto Scaling Groups
> * Removes it from any Elastic Load Balancers
> * Snapshots connected Elastic Block Storage devices
> * Tags the instance with IR details

6. Run your imported workflow.

<img width="1440" alt="image" src="https://user-images.githubusercontent.com/10421515/173712097-05b9094c-e06f-422f-aadf-c88a004e4e52.png">

7. Return to your previously created workflow **Pod X - AWS Workflow** that pulls instance details and run the workflow again.

8. Click on the **Extract EC2 Details** activty and note that after running the incident response workflow, the Security Group has been changed to move the impacted host to an isolated security group (Isolate_SG) and our condition now matches and the additional tagging activity has been run to identify the host as isolated.

<img width="1440" alt="third run" src="https://user-images.githubusercontent.com/10421515/217574158-8c1c3073-d447-45ac-bd5d-e1ff5611a231.png">

[jekyll-organization]: https://github.com/jekyll
