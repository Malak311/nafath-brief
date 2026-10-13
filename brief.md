Version: NAFATH-V2
Track: Software

## Overview

Six connected IT fields are needed to provide a reliable 5G service for emergency responders. Software helps manage requests, monitor service performance, and recover from failures. Artificial intelligence (AI) can predict network congestion and help operators act before the service slows down. Mobile applications allow responders to access important information and receive notifications, even when the internet connection is unavailable, if data is stored safely on the device. Networking uses 5G features, such as network slicing, to support the needs of emergency teams. Cybersecurity protects the service from cyberattacks and helps teams respond to security incidents. Data systems organize service information so operators can compare usage across different regions and days. Together, these six fields help keep the service available, protect sensitive information, and support better decisions during emergencies. Understanding safe and idempotent HTTP methods helps developers decide when automatic retries are appropriate.

## Software
When a network request fails, the different properties of HTTP methods are important. A safe method, such as GET, is used to read data without requesting changes to the server. An idempotent method has the same intended effect when the same request is repeated. PUT, for example, is idempotent. These rules help software decide when automatic retries are appropriate and reduce the risk of unwanted changes.

Resource: RFC 9110: HTTP Semantics - https://www.rfc-editor.org/rfc/rfc9110.html#section-9.2

## AI
Overfitting happens when an AI model learns the training data too closely and performs poorly on new data. Cross-validation helps detect this problem by dividing the data into different parts and testing the model several times. The results show whether the model performs consistently on data it has not trained on. For the 5G service, this helps check whether a congestion-prediction model can make reliable predictions.

Resource: Cross-validation: Evaluating Estimator Performance - https://scikit-learn.org/stable/modules/cross_validation.html

## Mobile
Mobile applications for emergency responders should provide important information even when the network connection is lost. An offline-first app stores essential data on the device so users can still access it without internet access. When the connection returns, the app can synchronize local changes with the server and update its information. It should also handle errors and conflicting changes carefully to help keep the data accurate.

Resource: Build an Offline-First App - https://developer.android.com/topic/architecture/data-layer/offline-first

## Networking
5G network slicing allows a mobile network to be divided into separate virtual networks that can support different service needs. An operator can configure a dedicated slice for emergency responders to help meet their communication and reliability requirements. However, a dedicated slice does not guarantee service during every failure or attack. The operator must also monitor network performance, test resilience, and manage resources carefully.

Resource: GSMA: An Introduction to Network Slicing - https://www.gsma.com/solutions-and-impact/technologies/networks/gsma_resources/an-introduction-to-network-slicing/

## Cybersecurity
Incident response helps organizations manage cybersecurity attacks and reduce their impact. The process includes detecting an incident, responding to it, and recovering from its effects. During an attack on the 5G service, the team should identify affected systems, analyze the threat, contain its impact, and restore services safely. After the incident, the team should review what happened and use the lessons learned to improve security and prepare for future incidents.

Resource: NIST SP 800-61 Rev. 3: Incident Response Recommendations and Considerations for Cybersecurity Risk Management - https://csrc.nist.gov/pubs/sp/800/61/r3/final

## Data
A star schema organizes data using a central fact table connected to dimension tables, such as date and region. A snowflake schema divides dimensions into additional related tables. For reports showing 5G usage by region and day, a star schema is often a good choice because it is simpler to understand and query. It helps analysts summarize usage and compare service performance across regions and dates.

Resource: Microsoft Learn: Understand Star Schema and the Importance for Power BI - https://learn.microsoft.com/en-us/power-bi/guidance/star-schema

## Misconception in My Track
A common misconception is that repeating any HTTP request is safe when a network connection fails. However, some requests can cause unwanted changes if they are repeated. According to RFC 9110, safe methods, such as GET, are intended to retrieve information without changing the server's state. Idempotent methods, such as PUT, have the same intended effect when repeated several times. However, this does not mean every response will be identical. Developers should understand these differences before enabling automatic retries. In emergency responders' 5G applications, correct retry handling can help prevent duplicate actions and unwanted changes when connections fail.

Resource: RFC 9110: HTTP Semantics, Sections 9.2.1 and 9.2.2 - https://www.rfc-editor.org/rfc/rfc9110.html

## Open Question
How can developers design automatic retry systems that keep emergency responders' 5G applications reliable without causing duplicate actions or unwanted changes when network connections fail?
