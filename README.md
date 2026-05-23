# Garment-SizeFit-for-WooCommerce
Eliminate size-related returns from your WooCommerce apparel store. A garment size selector with dynamic measurement mapping, modal size chart, and custom tailoring fields — built for the fashion and garment industry.


> **Eliminate size-related returns from your WooCommerce apparel store.**  
> A garment size selector with dynamic measurement mapping, modal size chart, and custom tailoring fields — built for the fashion and garment industry.

---

## 🧩 The Problem This Solves

Online apparel stores face a critical fulfilment challenge: customers ordering garments have no standardised way to communicate their body measurements. This leads to:

- ❌ Wrong-size deliveries
- ❌ High return & exchange rates
- ❌ Customer dissatisfaction and lost revenue
- ❌ Operational overhead managing reverse logistics

**Garment-SizeFit-for-WooCommerce** solves this at the point of purchase — on the product page itself — before the item ever reaches the cart.

---

## ✨ Features

### 🛍️ Customer-Facing (Product Page)
| Feature | Description |
|---|---|
| **Standard Size Chips** | One-click size selection: XS, S, M, L, XL, XXL, XXXL |
| **Auto-fill Measurements** | Selecting a size instantly populates Chest, Waist, Hip & Shoulder fields |
| **Inches / CMS Toggle** | Customers can switch between imperial and metric units; values convert automatically |
| **✏️ Custom Size Option** | Customers with non-standard measurements can enter values manually |
| **Size Chart Modal** | Inline popup with the full industry-standard size chart |
| **How to Measure Guide** | Step-by-step body measurement instructions with visual cues, inside the modal |
| **Tailoring Notes Field** | Optional free-text field for special instructions (e.g., *"Add 1 inch to sleeves"*) |
| **Server-side Validation** | Blocks add-to-cart if measurements or size are missing/invalid |

### 🛒 Cart & Checkout
| Feature | Description |
|---|---|
| **Measurement Summary in Cart** | All entered measurements display as line-item metadata in the cart |
| **Persists Through Checkout** | Data flows seamlessly from cart → checkout → order |
| **Unique Cart Key** | Prevents duplicate cart items from merging incorrectly |

### 🖥️ Admin / Backend
| Feature | Description |
|---|---|
| **Styled Order Meta Panel** | Measurements shown in a clearly formatted green panel on the WooCommerce order edit page |
| **All Fields Visible** | Size, Unit, Chest, Waist, Hip, Shoulder, and Tailoring Note are all shown per line item |
| **Ready for Fulfilment** | Shipping team sees exact measurements alongside each ordered product |

## 📐 Built-in Size Chart (Industry Standard)

| Size | Chest (in) | Waist (in) | Hip (in) | Shoulder (in) |
|------|-----------|-----------|---------|--------------|
| XS   | 31        | 25        | 34      | 13.5         |
| S    | 33        | 27        | 36      | 14.0         |
| M    | 35        | 29        | 38      | 14.5         |
| L    | 37        | 31        | 40      | 15.0         |
| XL   | 39        | 33        | 42      | 15.5         |
| XXL  | 41        | 35        | 44      | 16.0         |
| XXXL | 43        | 37        | 46      | 16.5         |

> All values stored internally in inches. CMS conversion is applied dynamically on the frontend (1 in = 2.54 cm).

---

## ⚙️ Requirements

| Requirement | Version |
|---|---|
| WordPress | 5.8 or higher |
| WooCommerce | 6.0 or higher |
| PHP | 7.4 or higher |
| MySQL | 5.6 or higher |

> No additional plugins, page builders, or libraries required. Zero external dependencies.

---

## 🛡️ Security

- All POST data is sanitised before storage using WordPress native functions:
  - `sanitize_text_field()` for size, unit, and individual measurements
  - `sanitize_textarea_field()` for tailoring notes
- Output is escaped with `esc_html()` everywhere
- Size chart data is encoded with `json_encode()` and `JSON_NUMERIC_CHECK`
- The plugin respects `ABSPATH` check to prevent direct file access
- No database tables created; all data stored in native WooCommerce order meta

---

## 🐛 Known Limitations & Roadmap

### Current Limitations (v2.1)
- Size chart values are hardcoded in PHP; no admin UI to edit them yet
- Single size chart for all products (no per-product or per-category charts)
- Measurements apply to all WooCommerce product types equally

### Planned Features
- [ ] Admin settings page to manage size charts without touching code
- [ ] Per-product or per-category size chart support
- [ ] Export order measurements to CSV for bulk fulfilment workflows
- [ ] Support for variable products (auto-select size chip when variation is chosen)
- [ ] Kids/Children size presets
- [ ] International size standards (UK, EU, US) toggle

---

## 👤 Source

**Author**   : Akhilesh Maurya  
**Company**  : https://designswow.com  
**Emails**   : info@designswow.com | designswowindia@gmail.com
**Download** : 

---

## 🙏 Acknowledgements

- WooCommerce — The eCommerce backbone
- Inspired by size selection UX patterns from Flipkart and Ajio
- Apparel measurement standards based on common Indian & international fashion industry sizing.
  

> 💡 **Tip for store owners:** Pair this plugin with a professional product photography standard that shows the garment on a model — combined with accurate measurements, this dramatically reduces return rates.
