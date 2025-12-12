## Hi there 👋

**SkyClf** builds a lightweight, self-hosted toolkit to **classify all-sky camera images** and expose a simple **“current sky state”** API for dashboards and observatory automation.

### What we’re building
- **SkyClf** – Go server + web UI  
  - fetches the latest all-sky image
  - lets you label frames (`skystate`: clear / light_clouds / heavy_clouds / precipitation / unknown + optional meteor)
  - serves a stable endpoint like `GET /api/latest`
- **SkyClf Trainer** – Python trainer (separate repo)  
  - reads your local labels + images
  - trains/fine-tunes a model for *your* camera/site
  - exports versioned models (e.g. ONNX)

### Why “local training”?
All-sky setups differ a lot (lens, exposure, light pollution, horizon obstructions). SkyClf is designed so each user can label a few frames and train a model that fits their environment.

### Repositories
- `skyclf` — main app (server + UI + compose)
- `skyclf-trainer` — training pipeline (Python → model export)

### Get involved
- Open issues for bugs/feature requests
- PRs welcome (small, focused changes are easiest to review)
- If you’re adding a new class/task, include a short note on labeling rules

### Resources
- Docs: see each repo’s `README.md`
- API: `GET /api/latest` (and dataset/label endpoints in the main repo)

### Fun fact
We love clear skies — but we test on cloudy ones. ☁️✨
