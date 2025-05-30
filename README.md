# BLackBucks_DEVOPS
🚀 Hosting a Static Website Using AWS S3 — DevOps Overview
📌 What is it?
Hosting a static website on Amazon S3 (Simple Storage Service) involves storing and serving static content (HTML, CSS, JS, images, etc.) directly from an S3 bucket over the web — no server required.

🧱 Components Involved
Component	Description
S3 Bucket	Stores website files. The bucket must be public (or configured with a CloudFront distribution).
Bucket Policy	Grants public read access to objects (unless using CloudFront with OAI or signed URLs).
Static Website Hosting	An S3 feature that serves your files as a static website, with index and error documents.
Optional: Route 53	To map a custom domain (e.g., example.com) to your S3-hosted site.
Optional: CloudFront	A CDN to improve performance and add HTTPS support.


Optional DevOps Enhancements:
CI/CD Automation: Use GitHub Actions, GitLab CI, or AWS CodePipeline to deploy on every push.

Custom Domain: Use Route 53 or any DNS service to point your domain to the S3 endpoint.

HTTPS + CDN: Use CloudFront with a custom domain and SSL certificate (via ACM).

🔐 Security Considerations
Avoid making S3 buckets public unless necessary — prefer CloudFront + signed URLs.

Store only static content (no server-side code).

📦 Example Use Cases
Portfolio websites

Documentation (like Docusaurus, Hugo, MkDocs)

Frontends for SPAs (e.g., React, Angular)

