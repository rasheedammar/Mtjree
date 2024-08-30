# Mtjree Store

**Mtjree Store** is a company specializing in electronic payments for freelancers.

## Getting Started

### If You Are Using WordPress

1. Download our plugin [here](https://github.com/rasheedammar/Mtjree/blob/main/mtjree_store.zip).
2. Contact us [here](#) to get started.

That's all! It's that simple.

### If You Have a Custom-Built Website and Want to Integrate

1. First, contact us [here](#) to get set up within our system.
2. After you are set up, you can start sending requests to our API.

### API Integration

When sending data, make sure the request is a `POST` request and the body contains the following fields (each on a new line):

| Field            | Type                        |
|------------------|-----------------------------|
| `order_id`       | `number` or `string`        |
| `email`          | `string`                    |
| `shop_type`      | `string`                    |
| `shop_url`       | `string`                    |
| `currency`       | `string` (3-letter format)  |
| `total`          | `number`                    |
| `first_name`     | `string`                    |
| `last_name`      | `string`                    |
| `country`        | `string` (2-letter code)    |
| `city`           | `string`                    |
| `billing_address`| `string`                    |
| `postcode`       | `number`                    |
| `hookUrl`        | `string`                    |
| `customer_id`    | `number` or `string`        |
| `timestamp`      | `string` (16 characters)    |
| `phone`          | `string`                    |

- `timestamp` (A unique 16-character alphanumeric value, e.g., generate it like this:
    ```php
    $bytes = random_bytes(8);
    $timestamp = bin2hex($bytes);
    ```
- `phone`

### Send Your Request To:

`https://mtjree.link/wp-json/custom/v1/proxy`

---

**Note:** Ensure that the `hookUrl` is on the same domain as `shop_url` to maintain security and data integrity.

For any questions or support, please don't hesitate to contact us.
