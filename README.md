# z(θ) = e^{iθ} + e^{iπθ} Visualization

An interactive complex-plane visualization of the quasi-periodic curve

```
z(θ) = e^{iθ} + e^{iπθ}
```

The two rotating unit phasors have incommensurate angular velocities (1 and π), producing a path that never exactly repeats (within floating precision) and densely explores an annular region inside radius 2.

## Features
- Smooth animation using requestAnimationFrame
- Constant angular resolution (Δθ fixed) with speed controlled by batching steps per frame
- Fading trail / persistent mode toggle
- Dynamic coloring by complex argument
- Live statistics: θ, Δθ, steps per frame, total steps, frame count
- Reset, pause/resume, speed controls

## GitHub Pages Hosting
This project is a single static `index.html` (no build step). You can host it directly with GitHub Pages.

### 1. Create a repository
On GitHub, create a new repository (e.g. `pi-complex-curve`). Leave it public (recommended). Do **not** initialize with README (you already have one locally) if you plan to push from your machine.

### 2. Initialize locally (PowerShell)
From the folder containing `index.html` and this `README.md`:

```powershell
git init
 git add index.html README.md
 git commit -m "Initial commit: complex curve visualization"
 git branch -M main
 git remote add origin https://github.com/<YOUR_USERNAME>/pi-complex-curve.git
 git push -u origin main
```

### 3. (Optional) Add a .nojekyll file
If you later add folders beginning with underscores, GitHub Pages might ignore them. Prevent this by adding a blank `.nojekyll` file now:

```powershell
New-Item -ItemType File -Name .nojekyll
 git add .nojekyll
 git commit -m "Add .nojekyll"
 git push
```

### 4. Enable Pages
In the GitHub repository: Settings → Pages → Build and deployment → Source: **Deploy from a branch**.
Select branch: `main`, folder: `/ (root)`, then Save.

After a short delay (usually < 1 minute), your site will be live at:

```
https://<YOUR_USERNAME>.github.io/pi-complex-curve/
```

(If you use a different repo name, the path changes accordingly.)

### 5. Updating
Just commit and push changes:

```powershell
git add index.html
 git commit -m "Tune visualization parameters"
 git push
```

Deployment happens automatically.

## Custom Domain (Optional)
Add a `CNAME` file in the repo root containing your domain:

```
example.com
```

Then configure DNS (CNAME record pointing to `<YOUR_USERNAME>.github.io`).

## License
Choose a license (e.g. MIT). Create `LICENSE` file:

```text
MIT License
Copyright (c) 2025 <Your Name>
Permission is hereby granted, free of charge, to any person obtaining a copy ...
```

## Ideas / Next Steps
- Export PNG snapshots
- GIF/WebM recording (OffscreenCanvas + encoder lib)
- Switch to WebGL for millions of segments
- Add alternate incommensurate frequency pairs (√2, e, φ)
- Density heatmap accumulation layer

Enjoy exploring the curve!
