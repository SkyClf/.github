<div align="center">

<img src="https://github.com/SkyClf.png" width="200" height="200" alt="SkyClf Logo"/>

# SkyClf

**Classify the sky — one frame at a time.**

**SkyClf** is a lightweight, self-hosted system for **classifying all-sky camera images** <br />
and exposing a simple, reliable **“current sky state”** API for observatories.

[Report Bug](https://github.com/SkyClf/SkyClf/issues) · [Request Feature](https://github.com/SkyClf/SkyClf/issues)

</div>

---

### ✨ What is SkyClf?

SkyClf continuously fetches the **latest all-sky image**, lets you **label frames** and serves the result via a clean HTTP API. It is designed for **local training**, because no two skies — or cameras — are the same.

**Supported States:**
`clear` · `light_clouds` · `heavy_clouds` · `precipitation` · `unknown`

---

### 🧩 Projects

| Project | Stack | Description | Last Update |
| :--- | :--- | :--- | :--- |
| **[SkyClf](https://github.com/SkyClf/SkyClf)** | Go, Docker | **Core Application.** Handles fetching, labeling, API, and model inference. | ![GitHub last commit](https://img.shields.io/github/last-commit/SkyClf/SkyClf?style=flat-square&label=updated&color=blue) |
| **[SkyClf-Trainer](https://github.com/SkyClf/SkyClf-Trainer)** | Python | **Training Pipeline.** Reads local labels → trains a model → exports versioned models. | ![GitHub last commit](https://img.shields.io/github/last-commit/SkyClf/SkyClf-Trainer?style=flat-square&label=updated&color=blue) |

---

### 🌍 Why local models?

All-sky setups vary wildly regarding optics, sensors, light pollution, and horizon obstructions. SkyClf embraces this by making **user-trained models first-class**, not an afterthought.

---

### 📚 Resources & Contributing

* **API Entry Point:** `GET /api/latest`
* **Contribute:** PRs are welcome! New classes or tasks should include clear labeling rules.

---

<div align="center">
<i>Clear nights are rare — so we spend a lot of time training on clouds. ☁️</i>
</div>
