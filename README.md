# Shravan AI

**An independent, mobile-first research and answer-engine experiment.**

Shravan AI currently runs fully in the browser. It uses the SAGE retrieval prototype (Signal-Adaptive Grounded Evidence) to rank a curated knowledge pack and present grounded summaries with source references.

## Current capabilities

- Responsive research workspace for mobile and desktop
- SAGE hybrid retrieval: term relevance, title and tag boosts, phrase matching, character n-gram similarity and a confidence gate
- Evidence-linked answers from the bundled knowledge pack
- Research and quick-answer modes
- Topic focus, follow-up prompts and source cards
- Saved answers and recent search history using browser local storage
- Dark/light theme, installable PWA manifest and basic offline shell caching
- No external AI API, account system, analytics or tracking

## Important limitations

This is a local knowledge prototype, not a live web search engine and not a trained large language model. Its answers are limited to the included knowledge entries. The displayed match score is a retrieval relevance estimate, not a factual accuracy probability. Always open the cited original sources for important decisions.

## Run locally

Open index.html in a modern browser. For service-worker/PWA testing, serve the repository over localhost or HTTPS.

## Deploy to GitHub Pages

The workflow in .github/workflows/pages.yml publishes the repository on pushes to main.

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **GitHub Actions** as the source and save.
3. Push to main, or run **Deploy Shravan AI to GitHub Pages** from the Actions tab.
4. After the workflow succeeds, the site will be available at:

   https://shravan-info.github.io/shravan-ai/

## Roadmap

1. Expand the verified knowledge corpus with clear provenance and update dates.
2. Add a browser-side inverted index and BM25-style scoring for larger collections.
3. Add import/export for personal research collections.
4. Add a self-hosted crawler and index only when a reliable, maintainable infrastructure is available.
5. Evaluate retrieval quality with a small, transparent test set before adding any trained neural model.

## Project principles

- Evidence before confident-sounding answers
- Clear disclosure of what is local, indexed and not searched
- No fabricated citations or fake live-search results
- Privacy-first, browser-local personal data
