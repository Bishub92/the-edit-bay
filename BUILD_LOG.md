# Creator Tools — Build Log

Brand: **The Edit Bay** — "Free calculators & tools for video creators" (working title; Sam can rename).
Stack: hand-written static HTML/CSS/JS. No build step, no frameworks, no analytics, no cookies, no accounts. Deployable to GitHub Pages as-is.

## Built (2026-10-01) — v1: 10 tools + 5 pages
Pages: index (home), tools/index, about, gear (dormant affiliate structure), resources.
Tools:
1. bitrate-calculator — target size → video bitrate (VBR target) and reverse; audio + 2% container overhead accounted
2. recording-time — storage → record time and reverse; codec presets (ProRes 422 HQ/422/LT, XAVC S, H.264, H.265)
3. rate-calculator — salary goal → day/half-day/hourly rate with expenses + margin over billable days
4. file-size — bitrate + duration → estimated file size (decimal GB/MB)
5. aspect-ratio — ratio converter with encoder-safe even snapping + common platform sizes table
6. timecode — frames ↔ HH:MM:SS:FF at 23.976/24/25/29.97/30/50/59.94/60 (non-drop-frame)
7. loudness — LUFS/true-peak targets per platform + "will my mix be turned down?" checker
8. white-balance — interactive Kelvin slider (1500–10000K) with black-body swatch + source table
9. export-settings — cheat sheet: YouTube long-form, Shorts/TikTok/Reels, X/Twitter
10. budget-estimator — editable line-item production budget with contingency

Specs verified 2026-10-01 via web search: YouTube upload bitrates (8/12 Mbps 1080p, 35–45/53–68 4K SDR), TikTok (1080×1920 H.264 8–15 Mbps), IG Reels (1080×1920 8–12 Mbps), LUFS targets (YT/Spotify −14, Apple −16, TikTok/IG ≈−14, ATSC A/85 −24, EBU R128 −23, Netflix −27 dialogue-gated), ProRes 422 HQ 1080p = 220 Mbps (Apple spec).

## Next 10 tools (backlog)
1. Upload time calculator (file size ÷ connection speed → upload duration)
2. Data transfer time (GB/TB over USB/SATA/network speeds)
3. Shutter angle ↔ shutter speed converter
4. Crop factor / equivalent focal length
5. Depth-of-field estimator (simplified)
6. Subtitle reading-speed checker (CPS validator)
7. Video ad-revenue estimator (views × niche RPM ranges)
8. Render-time estimator (timeline length × render ratio)
9. Storage RAID usable-capacity calculator
10. Podcast loudness checker (−16 LUFS stereo / −19 mono quick reference)

## Content/SEO expansion ideas
- One deep guide per tool ("The complete guide to video bitrate") — long-form pages rank and earn backlinks
- Glossary: codec, container, GOP, chroma subsampling, etc.
- Update export-settings twice a year (platforms change specs quietly)
- Gear page: 2–3 picks per category with real testing notes before any affiliate link goes live

## Deploy steps (when Sam's GitHub account exists — ~5 min)
1. `cd creator_tools && git init && git add . && git commit -m "v1"`
2. Create repo on GitHub (public), `git remote add origin <url>`, `git push -u origin main`
3. Repo Settings → Pages → deploy from `main` branch → site live at `https://<user>.github.io/creator_tools/`
4. Replace `YOUR-USERNAME` in sitemap.xml + robots.txt with the real username, commit, push
5. (Optional, later) Submit sitemap to Google Search Console — needs a Google account; Sam decides
