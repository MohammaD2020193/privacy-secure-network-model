# CBTA Secure Network Architecture

This repository contains network architecture diagrams, security assumptions, and supporting materials for the proposed secure infrastructure of CBTA's Course Delivery and Feedback systems. The architecture separates course content and feedback data using AWS Commercial (eu-west-2) and AWS GovCloud (EU-London) regions, respectively.

## Project Overview

- **Course Content**  
  - Hosted in AWS Commercial (eu-west-2)  
  - Uses SSE-S3 encryption (ISO 27001 compliant)  
  - Delivered globally via CloudFront CDN

- **Feedback Data**  
  - Hosted in AWS GovCloud (EU-London)  
  - Uses FIPS 140-2 Level 3 HSM-backed encryption (UK GDPR compliant)  
  - Isolated via dedicated VPC with strict IAM and NSG rules

## Key Features

- TLS 1.3 encrypted communication
- IAM policies with least privilege and explicit deny rules
- Logical and physical data segregation
- Optimized for performance and cost-efficiency

## Use Case

This setup supports secure and compliant storage and transmission of sensitive feedback data while delivering course material efficiently to users across Europe, including the UK.

---

*Part of a Master's-level project on network and data security for educational platforms.*
