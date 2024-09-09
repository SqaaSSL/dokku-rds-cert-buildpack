# dokku-rds-cert-buildpack

complete custom buildpack that downloads and installs the RDS CA certificate during the build phase

# Dokku RDS Certificate Buildpack

This buildpack downloads the Amazon RDS CA certificate and sets the `NODE_EXTRA_CA_CERTS` environment variable for use in Node.js applications deployed on Dokku.

## Usage

1. Add this buildpack to your Dokku application:

```
dokku buildpacks:add your-app-name https://github.com/your-username/dokku-rds-cert-buildpack.git
```

2. Ensure this buildpack runs before your main buildpack (e.g., the Node.js buildpack).

3. Deploy your application as usual.

The RDS CA certificate will be downloaded during the build process and the `NODE_EXTRA_CA_CERTS` environment variable will be set automatically.
