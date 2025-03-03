## Okta Provider

The CloudQuery Okta provider pulls configuration out of Okta resources, normalizes them and stores them in PostgreSQL
database.

### Install

```shell
cloudquery init okta
```

### Authentication

To [authenticate](https://developer.okta.com/docs/guides/create-an-api-token/overview/d) cloudquery with your Okta
account you need to set `OKTA_API_TOKEN` environment variable or add it the configuration.

### Configuration

The following configuration section can be automatically generated by `cloudquery init okta`:

```hcl
provider "okta" {
  configuration {
    // Optional. Okta Token to access API, you can set this with OKTA_API_TOKEN env variable
    // token = <YOUR_OKTA_TOKEN>
    // Required. You okta domain name
    // domain =  https://<CHANGE_THIS_TO_YOUR_OKTA_DOMAIN>.okta.com
  }
}
```

- `domain` (Required) - Specify the okta domain you are fetching from see
  this [link](https://developer.okta.com/docs/guides/find-your-domain/findorg/) to find your okta domain.
- `token` (Optional) - Okta Token to access API, you can set this with OKTA_API_TOKEN env variable