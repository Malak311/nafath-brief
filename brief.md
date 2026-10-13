Version: NAFATH-V2
Track: Software

## Overview

Six connected IT fields are needed to provide a reliable 5G service for emergency responders. Software helps manage requests, monitor service performance, and recover from failures. Artificial intelligence (AI) can predict network congestion and help operators take action before the service slows down. Mobile applications allow responders to access important information and receive notifications, even when the internet connection is unavailable, if data is stored safely on the device. Networking uses 5G features, such as network slicing, to support the needs of emergency teams. Cybersecurity protects the service from cyberattacks and helps teams respond to security incidents. Data systems organize service information so operators can compare usage across different regions and days. Together, these six fields help keep the service available, protect sensitive information, and support better decisions during emergencies. Regular testing, monitoring, and coordination help the service remain reliable.

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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
