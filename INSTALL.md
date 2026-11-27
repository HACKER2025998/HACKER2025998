# 🚀 Setup — xhackerip profile README

Your profile README lives in the special repo **`HACKER2025998/HACKER2025998`** (it already exists and holds your old "Hi there 👋").

## What's in the pack

```
README.md                              ← the profile
assets/hero.svg                        ← banner (matrix rain, glitch, radar, scanline)
assets/terminal.svg                    ← animated Kali terminal (whoami, nmap of your skills)
assets/pipeline.svg                    ← animated DevSecOps pipeline + feedback loop
assets/network.svg                     ← live network topology (packets, ACL DENY, SIEM alert)
assets/timeline.svg                    ← animated education & experience path
assets/divider.svg · assets/footer.svg ← section dividers + closing waves
profile/*.svg                          ← stats / languages / snake cards (placeholders, regenerated daily)
.github/workflows/profile-cards.yml    ← GitHub Action that generates the cards
```

## 1. Push the files

**Option A — command line (recommended)**

```bash
git clone https://github.com/HACKER2025998/HACKER2025998.git
cd HACKER2025998
# copy EVERYTHING from the pack here (including the hidden .github folder)
cp -r /path/to/xhackerip-readme/. .
rm -f INSTALL.md
git add -A
git commit -m "feat: profile README v2 — animated"
git push
```

**Option B — GitHub website**
Open the repo → **Add file → Upload files** → drop `README.md`, `assets/` and `profile/` → Commit.
The `.github` folder is hidden on most systems: create the file by hand instead with **Add file → Create new file**, name it `.github/workflows/profile-cards.yml` and paste its content.

## 2. Start the telemetry (one time only)

1. **Actions** tab of the repo → **Profile cards** workflow → **Run workflow**.
2. Wait ~1 minute: the `profile/*.svg` placeholders get replaced by your real stats and the snake.
3. From then on, it **refreshes itself every day**.

> If the job fails on `git push` (403): **Settings → Actions → General → Workflow permissions → Read and write permissions** → Save, then re-run.

## 3. Customize

| You want to change… | Where |
|:--|:--|
| The typed text under the banner | the `lines=` parameter of the `readme-typing-svg` URL in `README.md` (lines separated by `;`, spaces as `+`) |
| Terminal lines / pipeline / topology / timeline | edit the text directly inside the `.svg` files (they're plain text) |
| Colors | cyan `00F0FF` · magenta `FF2E97` · green `39FF88` · amber `FFB800` · background `05070F` |
| Add a project | copy a `<td>…</td>` block in the `PROJECTS` section |

## Notes

- All the "wow" animations are **SVGs hosted in your own repo**: no external dependency, they can't go down.
- The only external widgets left are the typing text, the streak card, the activity graph and the view counter. If one of them doesn't show up some day, that service is overloaded — the rest of the profile isn't affected.
- Your phone number is intentionally **not** in the README (a GitHub profile is public and indexed). Your portfolio stays the contact point.
