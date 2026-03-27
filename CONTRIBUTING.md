# Contributing to Awesome LLM Benchmarks

Thank you for your interest in contributing! This list is maintained by [BenchGecko](https://benchgecko.ai) and the community.

## Guidelines

### Adding a Benchmark

To add a benchmark, please ensure it meets the following criteria:

1. **Publicly available** - The benchmark must be publicly accessible (paper, dataset, or leaderboard).
2. **Actively used** - The benchmark should be used by at least a few research groups or model providers.
3. **Well-documented** - There should be a paper, technical report, or detailed documentation describing the methodology.
4. **Relevant** - The benchmark should evaluate large language models or closely related systems (multimodal models, agents, etc.).

### How to Submit

1. Fork this repository.
2. Add your benchmark to the appropriate section in `README.md`.
3. Follow the existing format:
   ```
   - **Name** - Brief description. [Paper](url) | [Dataset](url)
   ```
4. Keep descriptions concise (one line preferred).
5. Include links to the paper (arXiv preferred) and dataset (HuggingFace preferred) when available.
6. Submit a pull request with a clear title (e.g., "Add BenchmarkName to Code Generation section").

### Updating Scores

If you notice outdated or incorrect scores in the model comparison table:

1. Provide a source for the corrected score (official paper, blog post, or leaderboard).
2. Note that scores can vary by evaluation methodology -- include context if the difference is due to different eval settings.

### Suggesting New Sections

If you think a new category of benchmarks deserves its own section, open an issue first to discuss.

## Quality Standards

- No promotional or paid content.
- Benchmarks must be peer-reviewed or from established research institutions/companies.
- Self-nominations are fine if the benchmark meets all criteria above.

## Code of Conduct

Be respectful and constructive. We follow the [Contributor Covenant](https://www.contributor-covenant.org/version/2/1/code_of_conduct/).

## Questions?

- Open a GitHub issue for questions about this list.
- Visit [BenchGecko](https://benchgecko.ai) for model rankings and benchmark analysis.
