# Optimized Recon Automation

A streamlined Bash script for web reconnaissance in cybersecurity assessments. It automates URL collection from multiple sources, live probing, sensitive pattern detection, and JavaScript enumeration using tools like gau, httpx, LinkFinder, and Nuclei.

## Features
- **URL Discovery**: Gathers historical/current URLs via gau, waybackurls, katana, cariddi.
- **Live Probing**: Uses httpx to filter active endpoints.
- **Sensitive Files/Endpoints**: Greps for .env, .git, tokens, admin panels, etc.
- **JS Analysis**: Extracts, probes JS files, and runs LinkFinder, SecretFinder, Mantra, jsleak, Nuclei for endpoints/secrets.

## Requirements
- Bash 4+.
- Install tools: `gau`, `waybackurls`, `katana`, `cariddi`, `httpx`, `mantra`, `jsleak`, `nuclei`.
- Python tools: Clone LinkFinder and SecretFinder to `/home/tools/` (adjust paths in script).
- Nuclei templates: Download to `~/.local/nuclei-templates/`.
- Create `live.txt` with one domain/subdomain per line (e.g., example.com).

## Installation
1. Clone this repo: `git clone https://github.com/yourusername/optimized-recon-automation.git`
2. `cd optimized-recon-automation`
3. Make executable: `chmod +x main.sh`
4. Add targets to `live.txt`.
5. Run: `./main.sh`

Outputs go to `./results/` (add to .gitignore for temp runs).

## Usage Example
