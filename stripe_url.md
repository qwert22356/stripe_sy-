## 1 stripe trigger checkout.session.completed   模拟订阅并付款url
```json
[
  {
    "headers": {
      "connection": "upgrade",
      "host": "api.receiptdrop.dev",
      "x-real-ip": "52.15.183.38",
      "x-forwarded-for": "52.15.183.38",
      "content-length": "3429",
      "content-type": "application/json; charset=utf-8",
      "cache-control": "no-cache",
      "user-agent": "Stripe/1.0 (+https://stripe.com/docs/webhooks)",
      "accept": "*/*; q=0.5, application/json",
      "stripe-signature": "t=1753463562,v1=3f87ef77e37459cb3d2e11c8d2d726943d2cb41e87d60e6eb216a86a99319c91,v0=809064b56f89c806ab80f02b365ace7b6dbb180d17d67aa422a23d486c66f321"
    },
    "params": {},
    "query": {},
    "body": {
      "id": "evt_1RopAj08MTe1bJmc6urfmtTK",
      "object": "event",
      "api_version": "2025-05-28.basil",
      "created": 1753463561,
      "data": {
        "object": {
          "id": "cs_test_a1AiZLTUecpdBdEdFQHPUuU5kyj0MHkGtPzluErlxP1kRiieLFISbQr5eu",
          "object": "checkout.session",
          "adaptive_pricing": {
            "enabled": true
          },
          "after_expiration": null,
          "allow_promotion_codes": null,
          "amount_subtotal": 3000,
          "amount_total": 3000,
          "automatic_tax": {
            "enabled": false,
            "liability": null,
            "provider": null,
            "status": null
          },
          "billing_address_collection": null,
          "cancel_url": "https://httpbin.org/post",
          "client_reference_id": null,
          "client_secret": null,
          "collected_information": null,
          "consent": null,
          "consent_collection": null,
          "created": 1753463559,
          "currency": "usd",
          "currency_conversion": null,
          "custom_fields": [],
          "custom_text": {
            "after_submit": null,
            "shipping_address": null,
            "submit": null,
            "terms_of_service_acceptance": null
          },
          "customer": null,
          "customer_creation": "if_required",
          "customer_details": {
            "address": {
              "city": "South San Francisco",
              "country": "US",
              "line1": "354 Oyster Point Blvd",
              "line2": null,
              "postal_code": "94080",
              "state": "CA"
            },
            "email": "stripe@example.com",
            "name": "Jenny Rosen",
            "phone": null,
            "tax_exempt": "none",
            "tax_ids": []
          },
          "customer_email": null,
          "discounts": [],
          "expires_at": 1753549959,
          "invoice": null,
          "invoice_creation": {
            "enabled": false,
            "invoice_data": {
              "account_tax_ids": null,
              "custom_fields": null,
              "description": null,
              "footer": null,
              "issuer": null,
              "metadata": {},
              "rendering_options": null
            }
          },
          "livemode": false,
          "locale": null,
          "metadata": {},
          "mode": "payment",
          "origin_context": null,
          "payment_intent": "pi_3RopAi08MTe1bJmc1MMrv98y",
          "payment_link": null,
          "payment_method_collection": "if_required",
          "payment_method_configuration_details": {
            "id": "pmc_1RYOCx08MTe1bJmcJVKneFOR",
            "parent": null
          },
          "payment_method_options": {
            "card": {
              "request_three_d_secure": "automatic"
            }
          },
          "payment_method_types": [
            "card",
            "link",
            "paypal"
          ],
          "payment_status": "paid",
          "permissions": null,
          "phone_number_collection": {
            "enabled": false
          },
          "recovered_from": null,
          "saved_payment_method_options": null,
          "setup_intent": null,
          "shipping_address_collection": null,
          "shipping_cost": null,
          "shipping_options": [],
          "status": "complete",
          "submit_type": null,
          "subscription": null,
          "success_url": "https://httpbin.org/post",
          "total_details": {
            "amount_discount": 0,
            "amount_shipping": 0,
            "amount_tax": 0
          },
          "ui_mode": "hosted",
          "url": null,
          "wallet_options": null
        }
      },
      "livemode": false,
      "pending_webhooks": 1,
      "request": {
        "id": null,
        "idempotency_key": null
      },
      "type": "checkout.session.completed"
    },
    "webhookUrl": "http://localhost:5678/webhook/stripe",
    "executionMode": "production"
  }
]
```
## 2 模拟首次订阅账单付款成功 stripe trigger invoice.payment_succeeded
```json
[
  {
    "headers": {
      "connection": "upgrade",
      "host": "api.receiptdrop.dev",
      "x-real-ip": "3.18.12.63",
      "x-forwarded-for": "3.18.12.63",
      "content-length": "5047",
      "content-type": "application/json; charset=utf-8",
      "cache-control": "no-cache",
      "user-agent": "Stripe/1.0 (+https://stripe.com/docs/webhooks)",
      "accept": "*/*; q=0.5, application/json",
      "stripe-signature": "t=1753463643,v1=0470249cd6f8e3835819692120adba4adf7dc15a63b864fa91adb8d1afc3c385,v0=81c1f2189cad834558e97f5f8374d6eeff49b5f13f7c7f81bef281080e05b94c"
    },
    "params": {},
    "query": {},
    "body": {
      "id": "evt_1RopC308MTe1bJmcvQd5GtfN",
      "object": "event",
      "api_version": "2025-05-28.basil",
      "created": 1753463642,
      "data": {
        "object": {
          "id": "in_1RopBz08MTe1bJmcG0frvPtq",
          "object": "invoice",
          "account_country": "ES",
          "account_name": "ReceiptDrop sandbox",
          "account_tax_ids": null,
          "amount_due": 2000,
          "amount_overpaid": 0,
          "amount_paid": 2000,
          "amount_remaining": 0,
          "amount_shipping": 0,
          "application": null,
          "attempt_count": 1,
          "attempted": true,
          "auto_advance": false,
          "automatic_tax": {
            "disabled_reason": null,
            "enabled": false,
            "liability": null,
            "provider": null,
            "status": null
          },
          "automatically_finalizes_at": null,
          "billing_reason": "manual",
          "collection_method": "charge_automatically",
          "created": 1753463639,
          "currency": "usd",
          "custom_fields": null,
          "customer": "cus_SkJpM5HnXQpBkY",
          "customer_address": null,
          "customer_email": null,
          "customer_name": null,
          "customer_phone": null,
          "customer_shipping": null,
          "customer_tax_exempt": "none",
          "customer_tax_ids": [],
          "default_payment_method": null,
          "default_source": null,
          "default_tax_rates": [],
          "description": "(created by Stripe CLI)",
          "discounts": [],
          "due_date": null,
          "effective_at": 1753463640,
          "ending_balance": 0,
          "footer": null,
          "from_invoice": null,
          "hosted_invoice_url": "https://invoice.stripe.com/i/acct_1RYOCP08MTe1bJmc/test_YWNjdF8xUllPQ1AwOE1UZTFiSm1jLF9Ta0pwUFhNSTNqR09mclhhTTlRVVdISDY0cEpMUEQ5LDE0NDAwNDQ0Mw0200j0YQbbdG?s=ap",
          "invoice_pdf": "https://pay.stripe.com/invoice/acct_1RYOCP08MTe1bJmc/test_YWNjdF8xUllPQ1AwOE1UZTFiSm1jLF9Ta0pwUFhNSTNqR09mclhhTTlRVVdISDY0cEpMUEQ5LDE0NDAwNDQ0Mw0200j0YQbbdG/pdf?s=ap",
          "issuer": {
            "type": "self"
          },
          "last_finalization_error": null,
          "latest_revision": null,
          "lines": {
            "object": "list",
            "data": [
              {
                "id": "il_1RopBz08MTe1bJmcdjo4eq2X",
                "object": "line_item",
                "amount": 2000,
                "currency": "usd",
                "description": "(created by Stripe CLI)",
                "discount_amounts": [],
                "discountable": true,
                "discounts": [],
                "invoice": "in_1RopBz08MTe1bJmcG0frvPtq",
                "livemode": false,
                "metadata": {},
                "parent": {
                  "invoice_item_details": {
                    "invoice_item": "ii_1RopBz08MTe1bJmcS23w6lch",
                    "proration": false,
                    "proration_details": {
                      "credited_items": null
                    },
                    "subscription": null
                  },
                  "subscription_item_details": null,
                  "type": "invoice_item_details"
                },
                "period": {
                  "end": 1753463639,
                  "start": 1753463639
                },
                "pretax_credit_amounts": [],
                "pricing": {
                  "price_details": {
                    "price": "price_1Ronir08MTe1bJmcgsIJM0rV",
                    "product": "prod_SkIJPeNYXYBrql"
                  },
                  "type": "price_details",
                  "unit_amount_decimal": "2000"
                },
                "quantity": 1,
                "taxes": []
              }
            ],
            "has_more": false,
            "total_count": 1,
            "url": "/v1/invoices/in_1RopBz08MTe1bJmcG0frvPtq/lines"
          },
          "livemode": false,
          "metadata": {},
          "next_payment_attempt": null,
          "number": "N3HZL44E-0005",
          "on_behalf_of": null,
          "parent": null,
          "payment_settings": {
            "default_mandate": null,
            "payment_method_options": null,
            "payment_method_types": null
          },
          "period_end": 1753463639,
          "period_start": 1753463639,
          "post_payment_credit_notes_amount": 0,
          "pre_payment_credit_notes_amount": 0,
          "receipt_number": null,
          "rendering": {
            "amount_tax_display": null,
            "pdf": {
              "page_size": "letter"
            },
            "template": null,
            "template_version": null
          },
          "shipping_cost": null,
          "shipping_details": null,
          "starting_balance": 0,
          "statement_descriptor": null,
          "status": "paid",
          "status_transitions": {
            "finalized_at": 1753463640,
            "marked_uncollectible_at": null,
            "paid_at": 1753463640,
            "voided_at": null
          },
          "subtotal": 2000,
          "subtotal_excluding_tax": 2000,
          "test_clock": null,
          "total": 2000,
          "total_discount_amounts": [],
          "total_excluding_tax": 2000,
          "total_pretax_credit_amounts": [],
          "total_taxes": [],
          "webhooks_delivered_at": 1753463639
        }
      },
      "livemode": false,
      "pending_webhooks": 1,
      "request": {
        "id": "req_dFvPaqwJsSZe5L",
        "idempotency_key": "8655491b-68dd-4698-bcfd-9197e613a1e8"
      },
      "type": "invoice.paid"
    },
    "webhookUrl": "http://localhost:5678/webhook/stripe",
    "executionMode": "production"
  }
]
```
## 3 模拟创建订阅对象（会分开发送2条过来）stripe trigger customer.subscription.created
- 第一条
```json
[
  {
    "headers": {
      "connection": "upgrade",
      "host": "api.receiptdrop.dev",
      "x-real-ip": "3.130.192.231",
      "x-forwarded-for": "3.130.192.231",
      "content-length": "5257",
      "content-type": "application/json; charset=utf-8",
      "cache-control": "no-cache",
      "user-agent": "Stripe/1.0 (+https://stripe.com/docs/webhooks)",
      "accept": "*/*; q=0.5, application/json",
      "stripe-signature": "t=1753463712,v1=61ef0d66047126cdd2ed4debcd13be34a979606862941815ee5435446354a426,v0=8beec5404c6226ca69d3b79aba0c8d8b4162d22e4a7824beca35d0b96184e547"
    },
    "params": {},
    "query": {},
    "body": {
      "id": "evt_1RopDA08MTe1bJmcAk4cUhHZ",
      "object": "event",
      "api_version": "2025-05-28.basil",
      "created": 1753463711,
      "data": {
        "object": {
          "id": "sub_1RopD708MTe1bJmc4Z0NpbeM",
          "object": "subscription",
          "application": null,
          "application_fee_percent": null,
          "automatic_tax": {
            "disabled_reason": null,
            "enabled": false,
            "liability": null
          },
          "billing_cycle_anchor": 1753463709,
          "billing_cycle_anchor_config": null,
          "billing_mode": {
            "type": "classic"
          },
          "billing_thresholds": null,
          "cancel_at": null,
          "cancel_at_period_end": false,
          "canceled_at": null,
          "cancellation_details": {
            "comment": null,
            "feedback": null,
            "reason": null
          },
          "collection_method": "charge_automatically",
          "created": 1753463709,
          "currency": "usd",
          "customer": "cus_SkJqpBcslIPSdj",
          "days_until_due": null,
          "default_payment_method": null,
          "default_source": null,
          "default_tax_rates": [],
          "description": null,
          "discounts": [],
          "ended_at": null,
          "invoice_settings": {
            "account_tax_ids": null,
            "issuer": {
              "type": "self"
            }
          },
          "items": {
            "object": "list",
            "data": [
              {
                "id": "si_SkJqbWyQE58V1x",
                "object": "subscription_item",
                "billing_thresholds": null,
                "created": 1753463709,
                "current_period_end": 1756142109,
                "current_period_start": 1753463709,
                "discounts": [],
                "metadata": {},
                "plan": {
                  "id": "price_1RopD608MTe1bJmc7qFodK65",
                  "object": "plan",
                  "active": true,
                  "amount": 1500,
                  "amount_decimal": "1500",
                  "billing_scheme": "per_unit",
                  "created": 1753463708,
                  "currency": "usd",
                  "interval": "month",
                  "interval_count": 1,
                  "livemode": false,
                  "metadata": {},
                  "meter": null,
                  "nickname": null,
                  "product": "prod_SkJq7HMHs5DdRM",
                  "tiers_mode": null,
                  "transform_usage": null,
                  "trial_period_days": null,
                  "usage_type": "licensed"
                },
                "price": {
                  "id": "price_1RopD608MTe1bJmc7qFodK65",
                  "object": "price",
                  "active": true,
                  "billing_scheme": "per_unit",
                  "created": 1753463708,
                  "currency": "usd",
                  "custom_unit_amount": null,
                  "livemode": false,
                  "lookup_key": null,
                  "metadata": {},
                  "nickname": null,
                  "product": "prod_SkJq7HMHs5DdRM",
                  "recurring": {
                    "interval": "month",
                    "interval_count": 1,
                    "meter": null,
                    "trial_period_days": null,
                    "usage_type": "licensed"
                  },
                  "tax_behavior": "unspecified",
                  "tiers_mode": null,
                  "transform_quantity": null,
                  "type": "recurring",
                  "unit_amount": 1500,
                  "unit_amount_decimal": "1500"
                },
                "quantity": 1,
                "subscription": "sub_1RopD708MTe1bJmc4Z0NpbeM",
                "tax_rates": []
              }
            ],
            "has_more": false,
            "total_count": 1,
            "url": "/v1/subscription_items?subscription=sub_1RopD708MTe1bJmc4Z0NpbeM"
          },
          "latest_invoice": "in_1RopD708MTe1bJmcHAXjEg2o",
          "livemode": false,
          "metadata": {},
          "next_pending_invoice_item_invoice": null,
          "on_behalf_of": null,
          "pause_collection": null,
          "payment_settings": {
            "payment_method_options": null,
            "payment_method_types": null,
            "save_default_payment_method": "off"
          },
          "pending_invoice_item_interval": null,
          "pending_setup_intent": null,
          "pending_update": null,
          "plan": {
            "id": "price_1RopD608MTe1bJmc7qFodK65",
            "object": "plan",
            "active": true,
            "amount": 1500,
            "amount_decimal": "1500",
            "billing_scheme": "per_unit",
            "created": 1753463708,
            "currency": "usd",
            "interval": "month",
            "interval_count": 1,
            "livemode": false,
            "metadata": {},
            "meter": null,
            "nickname": null,
            "product": "prod_SkJq7HMHs5DdRM",
            "tiers_mode": null,
            "transform_usage": null,
            "trial_period_days": null,
            "usage_type": "licensed"
          },
          "quantity": 1,
          "schedule": null,
          "start_date": 1753463709,
          "status": "active",
          "test_clock": null,
          "transfer_data": null,
          "trial_end": null,
          "trial_settings": {
            "end_behavior": {
              "missing_payment_method": "create_invoice"
            }
          },
          "trial_start": null
        }
      },
      "livemode": false,
      "pending_webhooks": 1,
      "request": {
        "id": "req_TQKlshEUVhX9hy",
        "idempotency_key": "8e658186-9f85-4dd2-9d9e-8d7a3f6eb41a"
      },
      "type": "customer.subscription.created"
    },
    "webhookUrl": "http://localhost:5678/webhook/stripe",
    "executionMode": "production"
  }
]
```
- 第二条
```json
[
  {
    "headers": {
      "connection": "upgrade",
      "host": "api.receiptdrop.dev",
      "x-real-ip": "3.18.12.63",
      "x-forwarded-for": "3.18.12.63",
      "content-length": "5157",
      "content-type": "application/json; charset=utf-8",
      "cache-control": "no-cache",
      "user-agent": "Stripe/1.0 (+https://stripe.com/docs/webhooks)",
      "accept": "*/*; q=0.5, application/json",
      "stripe-signature": "t=1753463712,v1=bb7862b84d5cc8c80c31cf8ffa2925e2d889aa0e59e07b6ec5c914b38558ed7f,v0=68fd63d9a7007bc96c86b9b417b681f59967fac3605fbe6d2a399c83d75752f3"
    },
    "params": {},
    "query": {},
    "body": {
      "id": "evt_1RopDA08MTe1bJmcbY5Ypfl3",
      "object": "event",
      "api_version": "2025-05-28.basil",
      "created": 1753463711,
      "data": {
        "object": {
          "id": "in_1RopD708MTe1bJmcHAXjEg2o",
          "object": "invoice",
          "account_country": "ES",
          "account_name": "ReceiptDrop sandbox",
          "account_tax_ids": null,
          "amount_due": 1500,
          "amount_overpaid": 0,
          "amount_paid": 1500,
          "amount_remaining": 0,
          "amount_shipping": 0,
          "application": null,
          "attempt_count": 1,
          "attempted": true,
          "auto_advance": false,
          "automatic_tax": {
            "disabled_reason": null,
            "enabled": false,
            "liability": null,
            "provider": null,
            "status": null
          },
          "automatically_finalizes_at": null,
          "billing_reason": "subscription_create",
          "collection_method": "charge_automatically",
          "created": 1753463709,
          "currency": "usd",
          "custom_fields": null,
          "customer": "cus_SkJqpBcslIPSdj",
          "customer_address": null,
          "customer_email": null,
          "customer_name": null,
          "customer_phone": null,
          "customer_shipping": null,
          "customer_tax_exempt": "none",
          "customer_tax_ids": [],
          "default_payment_method": null,
          "default_source": null,
          "default_tax_rates": [],
          "description": null,
          "discounts": [],
          "due_date": null,
          "effective_at": 1753463709,
          "ending_balance": 0,
          "footer": null,
          "from_invoice": null,
          "hosted_invoice_url": "https://invoice.stripe.com/i/acct_1RYOCP08MTe1bJmc/test_YWNjdF8xUllPQ1AwOE1UZTFiSm1jLF9Ta0pxRzhqdTN0QmRGU1BIMGRDTlhpSE1Pd0JGNUg1LDE0NDAwNDUxMg0200ba1e08If?s=ap",
          "invoice_pdf": "https://pay.stripe.com/invoice/acct_1RYOCP08MTe1bJmc/test_YWNjdF8xUllPQ1AwOE1UZTFiSm1jLF9Ta0pxRzhqdTN0QmRGU1BIMGRDTlhpSE1Pd0JGNUg1LDE0NDAwNDUxMg0200ba1e08If/pdf?s=ap",
          "issuer": {
            "type": "self"
          },
          "last_finalization_error": null,
          "latest_revision": null,
          "lines": {
            "object": "list",
            "data": [
              {
                "id": "il_1RopD708MTe1bJmcpENDLGbd",
                "object": "line_item",
                "amount": 1500,
                "currency": "usd",
                "description": "1 × myproduct (at $15.00 / month)",
                "discount_amounts": [],
                "discountable": true,
                "discounts": [],
                "invoice": "in_1RopD708MTe1bJmcHAXjEg2o",
                "livemode": false,
                "metadata": {},
                "parent": {
                  "invoice_item_details": null,
                  "subscription_item_details": {
                    "invoice_item": null,
                    "proration": false,
                    "proration_details": {
                      "credited_items": null
                    },
                    "subscription": "sub_1RopD708MTe1bJmc4Z0NpbeM",
                    "subscription_item": "si_SkJqbWyQE58V1x"
                  },
                  "type": "subscription_item_details"
                },
                "period": {
                  "end": 1756142109,
                  "start": 1753463709
                },
                "pretax_credit_amounts": [],
                "pricing": {
                  "price_details": {
                    "price": "price_1RopD608MTe1bJmc7qFodK65",
                    "product": "prod_SkJq7HMHs5DdRM"
                  },
                  "type": "price_details",
                  "unit_amount_decimal": "1500"
                },
                "quantity": 1,
                "taxes": []
              }
            ],
            "has_more": false,
            "total_count": 1,
            "url": "/v1/invoices/in_1RopD708MTe1bJmcHAXjEg2o/lines"
          },
          "livemode": false,
          "metadata": {},
          "next_payment_attempt": null,
          "number": "N3HZL44E-0006",
          "on_behalf_of": null,
          "parent": {
            "quote_details": null,
            "subscription_details": {
              "metadata": {},
              "subscription": "sub_1RopD708MTe1bJmc4Z0NpbeM"
            },
            "type": "subscription_details"
          },
          "payment_settings": {
            "default_mandate": null,
            "payment_method_options": null,
            "payment_method_types": null
          },
          "period_end": 1753463709,
          "period_start": 1753463709,
          "post_payment_credit_notes_amount": 0,
          "pre_payment_credit_notes_amount": 0,
          "receipt_number": null,
          "rendering": null,
          "shipping_cost": null,
          "shipping_details": null,
          "starting_balance": 0,
          "statement_descriptor": null,
          "status": "paid",
          "status_transitions": {
            "finalized_at": 1753463709,
            "marked_uncollectible_at": null,
            "paid_at": 1753463709,
            "voided_at": null
          },
          "subtotal": 1500,
          "subtotal_excluding_tax": 1500,
          "test_clock": null,
          "total": 1500,
          "total_discount_amounts": [],
          "total_excluding_tax": 1500,
          "total_pretax_credit_amounts": [],
          "total_taxes": [],
          "webhooks_delivered_at": 1753463709
        }
      },
      "livemode": false,
      "pending_webhooks": 1,
      "request": {
        "id": "req_TQKlshEUVhX9hy",
        "idempotency_key": "8e658186-9f85-4dd2-9d9e-8d7a3f6eb41a"
      },
      "type": "invoice.paid"
    },
    "webhookUrl": "http://localhost:5678/webhook/stripe",
    "executionMode": "production"
  }
]
```
## 4 模拟用户取消订阅 stripe trigger customer.subscription.deleted
- 第一条
```json
[
  {
    "headers": {
      "connection": "upgrade",
      "host": "api.receiptdrop.dev",
      "x-real-ip": "3.130.192.231",
      "x-forwarded-for": "3.130.192.231",
      "content-length": "5257",
      "content-type": "application/json; charset=utf-8",
      "cache-control": "no-cache",
      "user-agent": "Stripe/1.0 (+https://stripe.com/docs/webhooks)",
      "accept": "*/*; q=0.5, application/json",
      "stripe-signature": "t=1753463771,v1=d2b307d5a06230ec76de4c54211bedb5af2831c0952c04298854bb2a01ed7387,v0=993ae24e476b4a45e63a73beb9dbccbe5bcc794fa1a890fed81db867a350a72a"
    },
    "params": {},
    "query": {},
    "body": {
      "id": "evt_1RopE708MTe1bJmcRa2r7BcV",
      "object": "event",
      "api_version": "2025-05-28.basil",
      "created": 1753463771,
      "data": {
        "object": {
          "id": "sub_1RopE508MTe1bJmcVyjGTTHz",
          "object": "subscription",
          "application": null,
          "application_fee_percent": null,
          "automatic_tax": {
            "disabled_reason": null,
            "enabled": false,
            "liability": null
          },
          "billing_cycle_anchor": 1753463768,
          "billing_cycle_anchor_config": null,
          "billing_mode": {
            "type": "classic"
          },
          "billing_thresholds": null,
          "cancel_at": null,
          "cancel_at_period_end": false,
          "canceled_at": null,
          "cancellation_details": {
            "comment": null,
            "feedback": null,
            "reason": null
          },
          "collection_method": "charge_automatically",
          "created": 1753463768,
          "currency": "usd",
          "customer": "cus_SkJrttJich3Kv0",
          "days_until_due": null,
          "default_payment_method": null,
          "default_source": null,
          "default_tax_rates": [],
          "description": null,
          "discounts": [],
          "ended_at": null,
          "invoice_settings": {
            "account_tax_ids": null,
            "issuer": {
              "type": "self"
            }
          },
          "items": {
            "object": "list",
            "data": [
              {
                "id": "si_SkJrHJLlWwq5HH",
                "object": "subscription_item",
                "billing_thresholds": null,
                "created": 1753463769,
                "current_period_end": 1756142168,
                "current_period_start": 1753463768,
                "discounts": [],
                "metadata": {},
                "plan": {
                  "id": "price_1RopE408MTe1bJmc68SrRvGe",
                  "object": "plan",
                  "active": true,
                  "amount": 1500,
                  "amount_decimal": "1500",
                  "billing_scheme": "per_unit",
                  "created": 1753463768,
                  "currency": "usd",
                  "interval": "month",
                  "interval_count": 1,
                  "livemode": false,
                  "metadata": {},
                  "meter": null,
                  "nickname": null,
                  "product": "prod_SkJrHVcH0qRU3a",
                  "tiers_mode": null,
                  "transform_usage": null,
                  "trial_period_days": null,
                  "usage_type": "licensed"
                },
                "price": {
                  "id": "price_1RopE408MTe1bJmc68SrRvGe",
                  "object": "price",
                  "active": true,
                  "billing_scheme": "per_unit",
                  "created": 1753463768,
                  "currency": "usd",
                  "custom_unit_amount": null,
                  "livemode": false,
                  "lookup_key": null,
                  "metadata": {},
                  "nickname": null,
                  "product": "prod_SkJrHVcH0qRU3a",
                  "recurring": {
                    "interval": "month",
                    "interval_count": 1,
                    "meter": null,
                    "trial_period_days": null,
                    "usage_type": "licensed"
                  },
                  "tax_behavior": "unspecified",
                  "tiers_mode": null,
                  "transform_quantity": null,
                  "type": "recurring",
                  "unit_amount": 1500,
                  "unit_amount_decimal": "1500"
                },
                "quantity": 1,
                "subscription": "sub_1RopE508MTe1bJmcVyjGTTHz",
                "tax_rates": []
              }
            ],
            "has_more": false,
            "total_count": 1,
            "url": "/v1/subscription_items?subscription=sub_1RopE508MTe1bJmcVyjGTTHz"
          },
          "latest_invoice": "in_1RopE508MTe1bJmcBD6dOpHU",
          "livemode": false,
          "metadata": {},
          "next_pending_invoice_item_invoice": null,
          "on_behalf_of": null,
          "pause_collection": null,
          "payment_settings": {
            "payment_method_options": null,
            "payment_method_types": null,
            "save_default_payment_method": "off"
          },
          "pending_invoice_item_interval": null,
          "pending_setup_intent": null,
          "pending_update": null,
          "plan": {
            "id": "price_1RopE408MTe1bJmc68SrRvGe",
            "object": "plan",
            "active": true,
            "amount": 1500,
            "amount_decimal": "1500",
            "billing_scheme": "per_unit",
            "created": 1753463768,
            "currency": "usd",
            "interval": "month",
            "interval_count": 1,
            "livemode": false,
            "metadata": {},
            "meter": null,
            "nickname": null,
            "product": "prod_SkJrHVcH0qRU3a",
            "tiers_mode": null,
            "transform_usage": null,
            "trial_period_days": null,
            "usage_type": "licensed"
          },
          "quantity": 1,
          "schedule": null,
          "start_date": 1753463768,
          "status": "active",
          "test_clock": null,
          "transfer_data": null,
          "trial_end": null,
          "trial_settings": {
            "end_behavior": {
              "missing_payment_method": "create_invoice"
            }
          },
          "trial_start": null
        }
      },
      "livemode": false,
      "pending_webhooks": 1,
      "request": {
        "id": "req_kc4TtC0NqTr5Nk",
        "idempotency_key": "0efaf64e-dbc1-403b-8a68-ca1b2b09f63d"
      },
      "type": "customer.subscription.created"
    },
    "webhookUrl": "http://localhost:5678/webhook/stripe",
    "executionMode": "production"
  }
]
```
- 第二条
```json
[
  {
    "headers": {
      "connection": "upgrade",
      "host": "api.receiptdrop.dev",
      "x-real-ip": "3.130.192.231",
      "x-forwarded-for": "3.130.192.231",
      "content-length": "5157",
      "content-type": "application/json; charset=utf-8",
      "cache-control": "no-cache",
      "user-agent": "Stripe/1.0 (+https://stripe.com/docs/webhooks)",
      "accept": "*/*; q=0.5, application/json",
      "stripe-signature": "t=1753463772,v1=b7fa82377efdc57da3421ffb6b5ad4b04fdaa5181c1b2600cfad61fbbf60c815,v0=2cbe4616838901d3b1c7beb596f900d1506054e63e5b6551d9437ffff6abab2c"
    },
    "params": {},
    "query": {},
    "body": {
      "id": "evt_1RopE808MTe1bJmcCCk6gWZU",
      "object": "event",
      "api_version": "2025-05-28.basil",
      "created": 1753463771,
      "data": {
        "object": {
          "id": "in_1RopE508MTe1bJmcBD6dOpHU",
          "object": "invoice",
          "account_country": "ES",
          "account_name": "ReceiptDrop sandbox",
          "account_tax_ids": null,
          "amount_due": 1500,
          "amount_overpaid": 0,
          "amount_paid": 1500,
          "amount_remaining": 0,
          "amount_shipping": 0,
          "application": null,
          "attempt_count": 1,
          "attempted": true,
          "auto_advance": false,
          "automatic_tax": {
            "disabled_reason": null,
            "enabled": false,
            "liability": null,
            "provider": null,
            "status": null
          },
          "automatically_finalizes_at": null,
          "billing_reason": "subscription_create",
          "collection_method": "charge_automatically",
          "created": 1753463769,
          "currency": "usd",
          "custom_fields": null,
          "customer": "cus_SkJrttJich3Kv0",
          "customer_address": null,
          "customer_email": null,
          "customer_name": null,
          "customer_phone": null,
          "customer_shipping": null,
          "customer_tax_exempt": "none",
          "customer_tax_ids": [],
          "default_payment_method": null,
          "default_source": null,
          "default_tax_rates": [],
          "description": null,
          "discounts": [],
          "due_date": null,
          "effective_at": 1753463769,
          "ending_balance": 0,
          "footer": null,
          "from_invoice": null,
          "hosted_invoice_url": "https://invoice.stripe.com/i/acct_1RYOCP08MTe1bJmc/test_YWNjdF8xUllPQ1AwOE1UZTFiSm1jLF9Ta0pycnFmRTlxbXpEMUhubVc3Z3V3NWZoT2F2UG5nLDE0NDAwNDU3Mg02006v8hA8ya?s=ap",
          "invoice_pdf": "https://pay.stripe.com/invoice/acct_1RYOCP08MTe1bJmc/test_YWNjdF8xUllPQ1AwOE1UZTFiSm1jLF9Ta0pycnFmRTlxbXpEMUhubVc3Z3V3NWZoT2F2UG5nLDE0NDAwNDU3Mg02006v8hA8ya/pdf?s=ap",
          "issuer": {
            "type": "self"
          },
          "last_finalization_error": null,
          "latest_revision": null,
          "lines": {
            "object": "list",
            "data": [
              {
                "id": "il_1RopE508MTe1bJmcY62XSwLD",
                "object": "line_item",
                "amount": 1500,
                "currency": "usd",
                "description": "1 × myproduct (at $15.00 / month)",
                "discount_amounts": [],
                "discountable": true,
                "discounts": [],
                "invoice": "in_1RopE508MTe1bJmcBD6dOpHU",
                "livemode": false,
                "metadata": {},
                "parent": {
                  "invoice_item_details": null,
                  "subscription_item_details": {
                    "invoice_item": null,
                    "proration": false,
                    "proration_details": {
                      "credited_items": null
                    },
                    "subscription": "sub_1RopE508MTe1bJmcVyjGTTHz",
                    "subscription_item": "si_SkJrHJLlWwq5HH"
                  },
                  "type": "subscription_item_details"
                },
                "period": {
                  "end": 1756142168,
                  "start": 1753463768
                },
                "pretax_credit_amounts": [],
                "pricing": {
                  "price_details": {
                    "price": "price_1RopE408MTe1bJmc68SrRvGe",
                    "product": "prod_SkJrHVcH0qRU3a"
                  },
                  "type": "price_details",
                  "unit_amount_decimal": "1500"
                },
                "quantity": 1,
                "taxes": []
              }
            ],
            "has_more": false,
            "total_count": 1,
            "url": "/v1/invoices/in_1RopE508MTe1bJmcBD6dOpHU/lines"
          },
          "livemode": false,
          "metadata": {},
          "next_payment_attempt": null,
          "number": "N3HZL44E-0007",
          "on_behalf_of": null,
          "parent": {
            "quote_details": null,
            "subscription_details": {
              "metadata": {},
              "subscription": "sub_1RopE508MTe1bJmcVyjGTTHz"
            },
            "type": "subscription_details"
          },
          "payment_settings": {
            "default_mandate": null,
            "payment_method_options": null,
            "payment_method_types": null
          },
          "period_end": 1753463768,
          "period_start": 1753463768,
          "post_payment_credit_notes_amount": 0,
          "pre_payment_credit_notes_amount": 0,
          "receipt_number": null,
          "rendering": null,
          "shipping_cost": null,
          "shipping_details": null,
          "starting_balance": 0,
          "statement_descriptor": null,
          "status": "paid",
          "status_transitions": {
            "finalized_at": 1753463769,
            "marked_uncollectible_at": null,
            "paid_at": 1753463768,
            "voided_at": null
          },
          "subtotal": 1500,
          "subtotal_excluding_tax": 1500,
          "test_clock": null,
          "total": 1500,
          "total_discount_amounts": [],
          "total_excluding_tax": 1500,
          "total_pretax_credit_amounts": [],
          "total_taxes": [],
          "webhooks_delivered_at": 1753463769
        }
      },
      "livemode": false,
      "pending_webhooks": 1,
      "request": {
        "id": "req_kc4TtC0NqTr5Nk",
        "idempotency_key": "0efaf64e-dbc1-403b-8a68-ca1b2b09f63d"
      },
      "type": "invoice.paid"
    },
    "webhookUrl": "http://localhost:5678/webhook/stripe",
    "executionMode": "production"
  }
]
```
-第三条
```json

[
  {
    "headers": {
      "connection": "upgrade",
      "host": "api.receiptdrop.dev",
      "x-real-ip": "3.130.192.231",
      "x-forwarded-for": "3.130.192.231",
      "content-length": "5257",
      "content-type": "application/json; charset=utf-8",
      "cache-control": "no-cache",
      "user-agent": "Stripe/1.0 (+https://stripe.com/docs/webhooks)",
      "accept": "*/*; q=0.5, application/json",
      "stripe-signature": "t=1753463773,v1=6bb6dcaa9172b9cf78b1809f4401b58808b2233d33947de56c5596c1c9f193a7,v0=369ed85171420cd8f34b6d07a4b060745ef2a94c0ccbf451ef6cb23c1df672d5"
    },
    "params": {},
    "query": {},
    "body": {
      "id": "evt_1RopE908MTe1bJmcZNPg8DL1",
      "object": "event",
      "api_version": "2025-05-28.basil",
      "created": 1753463773,
      "data": {
        "object": {
          "id": "sub_1RopE508MTe1bJmcVyjGTTHz",
          "object": "subscription",
          "application": null,
          "application_fee_percent": null,
          "automatic_tax": {
            "disabled_reason": null,
            "enabled": false,
            "liability": null
          },
          "billing_cycle_anchor": 1753463768,
          "billing_cycle_anchor_config": null,
          "billing_mode": {
            "type": "classic"
          },
          "billing_thresholds": null,
          "cancel_at": null,
          "cancel_at_period_end": false,
          "canceled_at": 1753463772,
          "cancellation_details": {
            "comment": null,
            "feedback": null,
            "reason": "cancellation_requested"
          },
          "collection_method": "charge_automatically",
          "created": 1753463768,
          "currency": "usd",
          "customer": "cus_SkJrttJich3Kv0",
          "days_until_due": null,
          "default_payment_method": null,
          "default_source": null,
          "default_tax_rates": [],
          "description": null,
          "discounts": [],
          "ended_at": 1753463772,
          "invoice_settings": {
            "account_tax_ids": null,
            "issuer": {
              "type": "self"
            }
          },
          "items": {
            "object": "list",
            "data": [
              {
                "id": "si_SkJrHJLlWwq5HH",
                "object": "subscription_item",
                "billing_thresholds": null,
                "created": 1753463769,
                "current_period_end": 1756142168,
                "current_period_start": 1753463768,
                "discounts": [],
                "metadata": {},
                "plan": {
                  "id": "price_1RopE408MTe1bJmc68SrRvGe",
                  "object": "plan",
                  "active": true,
                  "amount": 1500,
                  "amount_decimal": "1500",
                  "billing_scheme": "per_unit",
                  "created": 1753463768,
                  "currency": "usd",
                  "interval": "month",
                  "interval_count": 1,
                  "livemode": false,
                  "metadata": {},
                  "meter": null,
                  "nickname": null,
                  "product": "prod_SkJrHVcH0qRU3a",
                  "tiers_mode": null,
                  "transform_usage": null,
                  "trial_period_days": null,
                  "usage_type": "licensed"
                },
                "price": {
                  "id": "price_1RopE408MTe1bJmc68SrRvGe",
                  "object": "price",
                  "active": true,
                  "billing_scheme": "per_unit",
                  "created": 1753463768,
                  "currency": "usd",
                  "custom_unit_amount": null,
                  "livemode": false,
                  "lookup_key": null,
                  "metadata": {},
                  "nickname": null,
                  "product": "prod_SkJrHVcH0qRU3a",
                  "recurring": {
                    "interval": "month",
                    "interval_count": 1,
                    "meter": null,
                    "trial_period_days": null,
                    "usage_type": "licensed"
                  },
                  "tax_behavior": "unspecified",
                  "tiers_mode": null,
                  "transform_quantity": null,
                  "type": "recurring",
                  "unit_amount": 1500,
                  "unit_amount_decimal": "1500"
                },
                "quantity": 1,
                "subscription": "sub_1RopE508MTe1bJmcVyjGTTHz",
                "tax_rates": []
              }
            ],
            "has_more": false,
            "total_count": 1,
            "url": "/v1/subscription_items?subscription=sub_1RopE508MTe1bJmcVyjGTTHz"
          },
          "latest_invoice": "in_1RopE508MTe1bJmcBD6dOpHU",
          "livemode": false,
          "metadata": {},
          "next_pending_invoice_item_invoice": null,
          "on_behalf_of": null,
          "pause_collection": null,
          "payment_settings": {
            "payment_method_options": null,
            "payment_method_types": null,
            "save_default_payment_method": "off"
          },
          "pending_invoice_item_interval": null,
          "pending_setup_intent": null,
          "pending_update": null,
          "plan": {
            "id": "price_1RopE408MTe1bJmc68SrRvGe",
            "object": "plan",
            "active": true,
            "amount": 1500,
            "amount_decimal": "1500",
            "billing_scheme": "per_unit",
            "created": 1753463768,
            "currency": "usd",
            "interval": "month",
            "interval_count": 1,
            "livemode": false,
            "metadata": {},
            "meter": null,
            "nickname": null,
            "product": "prod_SkJrHVcH0qRU3a",
            "tiers_mode": null,
            "transform_usage": null,
            "trial_period_days": null,
            "usage_type": "licensed"
          },
          "quantity": 1,
          "schedule": null,
          "start_date": 1753463768,
          "status": "canceled",
          "test_clock": null,
          "transfer_data": null,
          "trial_end": null,
          "trial_settings": {
            "end_behavior": {
              "missing_payment_method": "create_invoice"
            }
          },
          "trial_start": null
        }
      },
      "livemode": false,
      "pending_webhooks": 1,
      "request": {
        "id": "req_FiNuKLP6cWeotE",
        "idempotency_key": null
      },
      "type": "customer.subscription.deleted"
    },
    "webhookUrl": "http://localhost:5678/webhook/stripe",
    "executionMode": "production"
  }
]
```
