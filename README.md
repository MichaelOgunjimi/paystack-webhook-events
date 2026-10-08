# Paystack webhook events

One JSON file with a sample payload for every Paystack webhook event: [`paystack_webhook_events.json`](paystack_webhook_events.json).

Paystack documents these samples across many separate pages, so it is hard to see them together. This puts all 24 in one place so you can search a field name or copy a payload into a test.

- Events covered: `charge.success`, `charge.dispute.*`, `refund.*`, `transfer.*`, `subscription.*`, `invoice.*`, `paymentrequest.*`, `customeridentification.*`, `dedicatedaccount.assign.*`.
- Each entry has `event`, `display_name`, `category`, `description` and the `payload` Paystack sends in `data`.
- The values are Paystack's own placeholder samples, not captured traffic. Use them for field names and shapes, not amounts, timing or ordering.
- Source: <https://paystack.com/docs/payments/webhooks/>. Check there for anything newer. This repo is not affiliated with Paystack.
- To verify real webhooks, check the `x-paystack-signature` header (HMAC SHA512 of the raw body with your secret key) before trusting any payload.
