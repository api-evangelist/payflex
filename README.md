# Payflex

Payflex is a South African Buy Now Pay Later (BNPL) platform that enables
merchants to offer interest-free installment payment options at checkout.
Consumers can split purchases into up to four payments over six weeks, with the
first 25% paid upfront. Payflex settles the full order amount to merchants
upfront (less commission) and assumes all credit and fraud risk.

## API

The Payflex Merchant API is a REST API secured with OAuth2 Client Credentials.
It supports both hosted (redirect) and embedded (iFrame) checkout flows and
covers the full order lifecycle.

**Production base URL:** `https://api.payflex.co.za`  
**Sandbox base URL:** `https://api.uat.payflex.co.za`  
**Authentication:** `POST https://auth.payflex.co.za/auth/merchant`

### Key Endpoints

| Method | Path | Description |
|--------|------|-------------|
| POST | `/order/productSelect` | Create an order and initiate checkout |
| GET | `/order/{orderId}` | Retrieve order status and details |
| POST | `/order/{orderId}/refund` | Issue a full or partial refund |
| GET | `/configuration` | Retrieve merchant payment limits |

### Authentication

Payflex uses the OAuth2 Client Credentials flow. Submit `client_id`,
`client_secret`, `audience`, and `grant_type=client_credentials` to the
auth endpoint to receive a bearer token. Credentials are issued by the Payflex
merchant team during onboarding.

## Platform Integrations

Payflex provides official plugins and modules for:

- [WooCommerce](https://github.com/PayFlexSA/payflex-woocommerce-plugin)
- [Magento 2.4](https://github.com/PayFlexSA/payflex-magento-2-4-module)
- [OpenCart 3](https://github.com/PayFlexSA/payflex-opencart-3-extension)
- [OpenCart 4](https://github.com/PayFlexSA/payflex-opencart-4-extension)
- [PrestaShop 8](https://github.com/PayFlexSA/payflex-prestashop-8-module)

## Links

- Website: https://payflex.co.za/
- Developer Docs: https://docs.payflex.co.za/
- Merchant Portal: https://merchant.payflex.co.za/login
- Merchant Hub: https://payflex.co.za/merchant/
- Support: https://payflex.co.za/support/
- GitHub: https://github.com/PayFlexSA

## APIs.json

This repository is an [APIs.json 0.19](https://apisjson.org/) profile for
Payflex, maintained by [API Evangelist](https://apievangelist.com).
