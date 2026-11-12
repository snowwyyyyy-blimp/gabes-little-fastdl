# TF2 FastDL Repository

Host your TF2 dedicated server's downloadable content here (maps, models, materials, sounds, etc.) so clients download quickly from Cloudflare Pages instead of your game server.

## Folder Structure

```
fastdl/
└── tf/
    └── maps/
        └── tfdb_indoor_tennis_b1a.bsp
```

## How to Use

1. Push this repo to GitHub
2. Connect the repo to **Cloudflare Pages**
3. Note your Pages URL (e.g. `https://tf2-fastdl.pages.dev`)
4. Add this to your TF2 server's `server.cfg`:

```
sv_downloadurl "https://YOUR-PAGES-URL/tf"
sv_allowdownload 1
sv_allowupload 0
```

Replace `YOUR-PAGES-URL` with your actual Cloudflare Pages domain.

## Adding More Files

Drop any additional FastDL content into the appropriate subfolders:

- `fastdl/tf/maps/` — `.bsp` map files
- `fastdl/tf/materials/` — custom materials
- `fastdl/tf/models/` — custom models
- `fastdl/tf/sound/` — custom sounds
- `fastdl/tf/particles/` — custom particles

Then commit and push — Cloudflare Pages will redeploy automatically.
