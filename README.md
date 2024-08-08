# Mtjree Store

**Mtjree Store** is a company specializing in electronic payments for freelancers.

## Getting Started

### If You Are Using WordPress

1. Download our plugin [here](#).
2. Contact us [here](#) to get started.

That's all! It's that simple.

### If You Have a Custom-Built Website and Want to Integrate

1. First, contact us [here](#) to get set up within our system.
2. After you are set up, you can start sending requests to our API.

### API Integration

When sending data, make sure the request is a `POST` request and the body contains the following fields (each on a new line):

- `order_id`
- `total`
- `shop_type`
- `shop_url`
- `currency` (3-letter format)
- `email`
- `first_name`
- `last_name`
- `country` (2-letter uppercase code)
- `city`
- `billing_address`
- `postcode`
- `hookUrl` (must be on the same domain as `shop_url`)
- `customer_id`
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
