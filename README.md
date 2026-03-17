# GPU Upgrade Calculator Widget

A free embeddable widget powered by [best-gpu.com](https://www.best-gpu.com) — the GPU price-to-performance tracker using live Amazon US prices.

Drop one `<iframe>` on your page and your visitors can instantly find out whether upgrading their GPU is worth it.

---

## Live demo

👉 [best-gpu.com/widget](https://www.best-gpu.com/widget/)

---

## Embed code

Copy and paste this snippet wherever you want the widget to appear:

```html
<iframe
  src="https://www.best-gpu.com/widget/"
  width="100%"
  height="620"
  style="border:none;border-radius:6px;display:block"
  title="GPU Upgrade Calculator — best-gpu.com"
  loading="lazy"
  allow="clipboard-write">
</iframe>
```

That's it. No API key, no sign-up, no JavaScript to load.

---

## What it does

Users pick their current GPU from a list of **200+ models** (NVIDIA, AMD, Intel — from RTX 5090 down to GTX 900 series) and instantly see:

| Column | Description |
|---|---|
| **Perf Gain %** | How much faster the upgrade is vs. their current card |
| **Value Score** | Performance-per-dollar rating |
| **Price** | Live price from Amazon US |
| **Brand / Model** | GPU name with brand badge |
| **VRAM** | Video memory in GB |
| **Condition** | New or Used |
| **Check on Amazon** | Direct affiliate buy link |

Results are sorted by **Perf Gain** by default (best upgrade value first). Users can re-sort by Value Score or Price, and filter with the search box.

---

## Customisation

All customisation is done through the `<iframe>` attributes — no config needed.

### Size

```html
<!-- Fixed height (recommended for sidebars) -->
<iframe src="https://www.best-gpu.com/widget/" width="100%" height="600" ...>

<!-- Taller for more visible results -->
<iframe src="https://www.best-gpu.com/widget/" width="100%" height="800" ...>
```

### Pre-select a GPU

Add a `gpu` query parameter to open the widget with a GPU already selected:

```html
<iframe
  src="https://www.best-gpu.com/widget/?gpu=RTX+3080"
  width="100%"
  height="620"
  ...>
</iframe>
```

Useful if your page is already about a specific card — your readers land straight on the upgrade comparison.

**Popular pre-selections:**

| GPU | URL parameter |
|---|---|
| RTX 3080 | `?gpu=RTX+3080` |
| RTX 3070 | `?gpu=RTX+3070` |
| RTX 2080 Ti | `?gpu=RTX+2080+Ti` |
| RX 6800 XT | `?gpu=RX+6800+XT` |
| GTX 1080 Ti | `?gpu=GTX+1080+Ti` |
| GTX 1070 | `?gpu=GTX+1070` |

### Default sort

```html
<!-- Sort by best value score -->
<iframe src="https://www.best-gpu.com/widget/?sort=value" ...>

<!-- Sort by lowest price -->
<iframe src="https://www.best-gpu.com/widget/?sort=price" ...>

<!-- Sort by perf gain (default) -->
<iframe src="https://www.best-gpu.com/widget/?sort=gain" ...>
```

### Combine parameters

```html
<iframe
  src="https://www.best-gpu.com/widget/?gpu=GTX+1080+Ti&sort=value"
  width="100%"
  height="620"
  style="border:none;border-radius:6px;display:block"
  title="GPU Upgrade Calculator — best-gpu.com"
  loading="lazy">
</iframe>
```

---

## Responsive setup

The widget is mobile-friendly but works best at **600 px wide or more**. For responsive pages:

```html
<div style="width:100%;min-width:320px;overflow:hidden;border-radius:6px">
  <iframe
    src="https://www.best-gpu.com/widget/"
    width="100%"
    height="620"
    style="border:none;display:block"
    title="GPU Upgrade Calculator — best-gpu.com"
    loading="lazy">
  </iframe>
</div>
```

---

## Example page

See [`example.html`](example.html) in this repo for a full ready-to-use HTML page with the widget embedded.

---

## Performance methodology

- **Perf Index** = `0.70 × (TimeSpy ÷ 360) + 0.30 × (TFLOPs ÷ 1.65)`
  Blends real gaming benchmark (3DMark TimeSpy) with raw compute (FP32 TFLOPs).
- **Perf Gain %** = `(upgrade Perf Index ÷ current Perf Index − 1) × 100`
- **Value Score** = proprietary algorithm weighing performance per dollar
- Prices are scraped from **Amazon US daily** and served live

Full methodology: [best-gpu.com/faq.php](https://www.best-gpu.com/faq.php)

---

## Attribution

This widget is **free to use** on any site. It is powered by [best-gpu.com](https://www.best-gpu.com).
A small "Powered by best-gpu.com" credit is shown inside the widget footer.

Please **do not** attempt to hide or remove the attribution inside the iframe.

---

## Affiliate disclosure

Buy links inside the widget are Amazon affiliate links. Purchases made through these links support [best-gpu.com](https://www.best-gpu.com) at no extra cost to the buyer.
See [best-gpu.com/privacy.php](https://www.best-gpu.com/privacy.php) for full disclosure.

---

## Issues & feedback

Open an issue in this repo or email [contact@best-gpu.com](mailto:contact@best-gpu.com).

---

*Prices and availability are sourced from Amazon US and may vary. Widget content © [best-gpu.com](https://www.best-gpu.com).*
