# Cássio Gabriel's personal website

The site uses the **Hugo static site generator** (to build HTML) hosted in an **AWS S3 bucket**, distributed globally through **Amazon CloudFront** (CDN with HTTPS via **AWS Certificate Manager**).
The domain was purchased from **Registro.br**, where the **DNS** points the `www` subdomain (CNAME) to CloudFront.

Deployment is automated via **GitHub Actions**, which builds the Hugo site and uploads it to S3 using an **IAM user** with restricted permissions.

A **mirror site of the original site** is also pushed to a **GitHub Pages** repository, serving as a public backup and alternative hosting source, which you can see [here](https://cassivsgabriellis.github.io/).

This setup ensures performance, TLS security, continuous deployment, and redundancy between AWS and GitHub Pages.