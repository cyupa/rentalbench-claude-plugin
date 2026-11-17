# Workflow map

| User task | Tool sequence |
| --- | --- |
| Location stock | `get_account`, `list_products`, `get_product`, `get_product_bookings` |
| Rental units | Product, variant and product item tools, including reversible trash and restore |
| Consumables | Product and variant tools, then `update_consumable_stock` when applicable |
| Customer records | Customer, address, custom field and comment tools |
| Rental order | Resolve the customer and stock, use `create_order`, then the appropriate lifecycle tools |
| Rental return | Read the order items and record the condition and any user-supplied deposit disposition using `return_order` or item transitions |
| Documents | `get_order`, `get_order_document`, `preview_order_document_pdf`, then issue or share if requested |
| Inventory import | Upload in RentalBench, then `list_inventory_imports`, `get_inventory_import`, `preview_inventory_import` and `confirm_inventory_import` |
| Webstore | `get_webstore`, slug and domain checks, create or update settings, and verify an existing attached domain |
| Team and settings | Account context, admin team tools, location settings and custom field definitions |
| Account security | `get_account_security` for secure RentalBench pages |
| Existing billing | `get_billing` for subscription status and invoices, `open_billing_portal` for secure management |

Follow `pagination.has_more` with the next offset until the requested scope is
covered. Use each location's currency and time zone when reporting results.
