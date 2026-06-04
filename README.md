# GPU Upgrade Calculator Widget

[![Stars](https://img.shields.io/github/stars/nebylba/gpu-upgrade-calculator-widget?style=social)](https://github.com/nebylba/gpu-upgrade-calculator-widget)
[![License](https://img.shields.io/github/license/nebylba/gpu-upgrade-calculator-widget)](LICENSE)
[![upgrade-gpu.com](https://img.shields.io/badge/Powered_by-upgrade--gpu.com-00e5ff)](https://www.upgrade-gpu.com)

A free embeddable widget powered by [upgrade-gpu.com](https://www.upgrade-gpu.com) — the GPU price-to-performance tracker with live Amazon prices and 200+ GPU models.

Drop one `<iframe>` on your page and visitors can instantly find out whether upgrading their GPU is worth it.

---

## Live demo & embed page

👉 **[upgrade-gpu.com/us/embed/](https://www.upgrade-gpu.com/us/embed/)** — interactive demo, all use-case snippets, and copy-button embed codes

---

## Try it on CodePen

- [Default widget](https://codepen.io/E-BLYN/pen/OPbvVeZ) — drops into any page
- [Pre-set to RTX 3080](https://codepen.io/E-BLYN/pen/MYbGjGm) — for RTX 3080 review pages
- [Pre-set to GTX 1080 Ti](https://codepen.io/E-BLYN/pen/VYmxKxg) — for legacy upgrade content

---

## Quick start

```html
<iframe
  src="https://www.upgrade-gpu.com/us/widget/"
  width="100%"
  height="640"
  style="border:none;border-radius:8px;display:block"
  title="GPU Upgrade Calculator — upgrade-gpu.com"
  loading="lazy">
</iframe>
```

That's it. No API key, no sign-up, no JavaScript to load.

See [`example.html`](example.html) for a complete, copy-paste-ready page.

---

## What it does

Users pick their current GPU from a list of **200+ models** (NVIDIA, AMD, Intel — from RTX 5090 down to GTX 900 series) and instantly see:

| Column | Description |
|---|---|
| **Perf Gain %** | How much faster the upgrade is vs. their current card |
| **Value Score** | Performance-per-dollar rating |
| **Price** | Live price from Amazon |
| **Brand / Model** | GPU name with brand badge |
| **VRAM** | Video memory in GB |
| **Condition** | New or Used |
| **Check on Amazon** | Direct affiliate buy link |

Results are sorted by **Value Score** by default (best upgrade value first). Users can re-sort by Perf Gain or Price, and filter with the search box.

---

## Customisation

All customisation is done through the `<iframe>` `src` attribute — no config files needed.

### Pre-select a GPU

Append the GPU slug to the widget URL to open it with a GPU already selected:

```html
<iframe
  src="https://www.upgrade-gpu.com/us/widget/rtx-3080/"
  width="100%"
  height="640"
  style="border:none;border-radius:8px;display:block"
  title="GPU Upgrade Calculator — RTX 3080"
  loading="lazy">
</iframe>
```

Useful if your page is already about a specific card — readers land straight on the upgrade comparison.

**Popular pre-selections:**

| GPU | src URL |
|---|---|
| RTX 4060 | `/us/widget/rtx-4060/` |
| RTX 3080 | `/us/widget/rtx-3080/` |
| RTX 3070 | `/us/widget/rtx-3070/` |
| RTX 3060 Ti | `/us/widget/rtx-3060-ti/` |
| RTX 2080 Ti | `/us/widget/rtx-2080-ti/` |
| RX 7800 XT | `/us/widget/rx-7800-xt/` |
| RX 6800 XT | `/us/widget/rx-6800-xt/` |
| GTX 1080 Ti | `/us/widget/gtx-1080-ti/` |
| GTX 1070 | `/us/widget/gtx-1070/` |

### Size

```html
<!-- Recommended default -->
<iframe src="..." width="100%" height="640" ...>

<!-- Compact (sidebar or narrow column) -->
<iframe src="..." width="100%" height="580" ...>

<!-- Tall (show more results without scrolling) -->
<iframe src="..." width="100%" height="800" ...>
```

### Sort order

```html
<!-- Sort by lowest price -->
<iframe src="https://www.upgrade-gpu.com/us/widget/?sort=price" ...>

<!-- Sort by performance gain -->
<iframe src="https://www.upgrade-gpu.com/us/widget/?sort=gain" ...>
```

Value score is the default — no parameter needed.

### Combine parameters

```html
<iframe
  src="https://www.upgrade-gpu.com/us/widget/gtx-1080-ti/?sort=value"
  width="100%"
  height="640"
  style="border:none;border-radius:8px;display:block"
  title="GPU Upgrade Calculator — GTX 1080 Ti"
  loading="lazy">
</iframe>
```

### UK market

```html
<iframe src="https://www.upgrade-gpu.com/uk/widget/" ...>
```

Shows Amazon UK prices in GBP. US and UK are currently available; more markets coming soon.

---

## Responsive setup

The widget is mobile-friendly but works best at **600 px wide or more**. For fully responsive pages:

```html
<div style="width:100%;min-width:320px;overflow:hidden;border-radius:8px">
  <iframe
    src="https://www.upgrade-gpu.com/us/widget/"
    width="100%"
    height="640"
    style="border:none;display:block"
    title="GPU Upgrade Calculator — upgrade-gpu.com"
    loading="lazy">
  </iframe>
</div>
```

---

## Performance methodology

- **Perf Index** = `0.70 × (TimeSpy ÷ 360) + 0.30 × (TFLOPs ÷ 1.65)`  
  Blends real gaming benchmark (3DMark TimeSpy) with raw compute (FP32 TFLOPs).
- **Perf Gain %** = `(upgrade Perf Index ÷ current Perf Index − 1) × 100`
- **Value Score** = cost per % gain (lower = better value)
- Prices are scraped from **Amazon daily** and served live

Full methodology: [upgrade-gpu.com/us/faq/](https://www.upgrade-gpu.com/us/faq/)

---

## Attribution

This widget is **free to use** on any site. It is powered by [upgrade-gpu.com](https://www.upgrade-gpu.com). A small "Powered by upgrade-gpu.com" credit appears in the widget footer.

Please do not attempt to hide or remove the attribution inside the iframe.

---

## Affiliate disclosure

Buy links inside the widget are Amazon affiliate links. Purchases made through these links support [upgrade-gpu.com](https://www.upgrade-gpu.com) at no extra cost to the buyer. See [upgrade-gpu.com/us/privacy/](https://www.upgrade-gpu.com/us/privacy/) for full disclosure.

---

## Who's using this?

[Open a PR or issue to add your site.](https://github.com/nebylba/gpu-upgrade-calculator-widget/issues)

---

## Issues & feedback

Open an issue in this repo or email [contact@upgrade-gpu.com](mailto:contact@upgrade-gpu.com).

---

*Prices and availability are sourced from Amazon and may vary. Widget content © [upgrade-gpu.com](https://www.upgrade-gpu.com).*
