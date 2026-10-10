# GitHub Trending CLI

A small Python command-line project I built for the [GitHub Trending CLI challenge on roadmap.sh](https://roadmap.sh/projects/github-trending-cli).

It searches public repositories created within a chosen time range and displays the most-starred results, including the repository name, language, description, and URL. It uses GitHub's repository search API; it does not reproduce GitHub's separate Trending page ranking.

## Setup

Requires Python 3.9 or newer. Install the one dependency:

```bash
python -m pip install -r requirements.txt
```

## Usage

```bash
python script.py
python script.py --duration day --limit 5
python script.py --duration month --limit 20
```

On Windows, `github-trending.bat` runs the same script from any working directory. Add this folder to `PATH` if you want to invoke `github-trending --duration month --limit 20` from anywhere, like my GitHub Activity CLI project.

`--duration` accepts `day`, `week`, `month`, or `year` (default: `week`). `--limit` accepts a number from 1 to 100 (default: 10).

The CLI uses the public GitHub API without a token. GitHub may rate-limit unauthenticated requests; request or API errors are reported in the terminal.

## Project source

This is my implementation of the [roadmap.sh project brief](https://roadmap.sh/projects/github-trending-cli), not an official GitHub Trending client.
