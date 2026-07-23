# Awesome LLM Benchmarks

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of benchmarks, evaluations, and leaderboards for large language models.

Maintained by [BenchGecko](https://benchgecko.ai) | [Full Model Rankings](https://benchgecko.ai/models) | [Agent Benchmarks](https://benchgecko.ai/agents)

> **Looking for real-time benchmark data?** Visit [benchgecko.ai](https://benchgecko.ai) for live model rankings, pricing comparisons, and API access.

---

## Contents

- [Language Understanding & Reasoning](#language-understanding--reasoning)
- [Math & Quantitative Reasoning](#math--quantitative-reasoning)
- [Code Generation](#code-generation)
- [Agent & Tool Use](#agent--tool-use)
- [Safety & Alignment](#safety--alignment)
- [Multilingual](#multilingual)
- [Multimodal (Vision + Language)](#multimodal-vision--language)
- [Long Context](#long-context)
- [Frontier & Emerging](#frontier--emerging)
- [Leaderboards](#leaderboards)
- [Model Comparison Table](#model-comparison-table)
- [Contributing](#contributing)

---

## Language Understanding & Reasoning

- **MMLU** (Massive Multitask Language Understanding) - 57 subjects across STEM, humanities, social sciences, and more. Multiple choice, 4 options. 14K questions. [Paper](https://arxiv.org/abs/2009.03300) | [Dataset](https://huggingface.co/datasets/cais/mmlu)
- **MMLU-Pro** - Harder version of MMLU with 10 answer choices instead of 4, reducing random guessing advantage. More reasoning-focused questions. [Paper](https://arxiv.org/abs/2406.01574) | [Dataset](https://huggingface.co/datasets/TIGER-Lab/MMLU-Pro)
- **ARC** (AI2 Reasoning Challenge) - Grade school science questions split into Easy and Challenge sets. 7,787 questions. [Paper](https://arxiv.org/abs/1803.05457) | [Dataset](https://huggingface.co/datasets/allenai/ai2_arc)
- **ARC-AGI** - Novel visual pattern reasoning requiring genuine abstraction and generalization. Designed to test abilities that current LLMs struggle with. [Website](https://arcprize.org/) | [Paper](https://arxiv.org/abs/1911.01547) | [Dataset](https://github.com/fchollet/ARC-AGI)
- **ARC-AGI-2** - Harder successor to ARC-AGI with more complex transformations. Gemini 3.1 Pro achieved 77.1%, state-of-the-art as of Feb 2026. [Website](https://arcprize.org/)
- **HellaSwag** - Sentence completion requiring commonsense reasoning. Models must pick the most plausible continuation. 10K questions. [Paper](https://arxiv.org/abs/1905.07830) | [Dataset](https://huggingface.co/datasets/Rowan/hellaswag)
- **WinoGrande** - Large-scale commonsense reasoning via pronoun resolution. Inspired by Winograd Schema Challenge. 44K problems. [Paper](https://arxiv.org/abs/1907.10641) | [Dataset](https://huggingface.co/datasets/allenai/winogrande)
- **BoolQ** - Yes/no questions naturally occurring from Google search queries, paired with Wikipedia passages. 15.9K examples. [Paper](https://arxiv.org/abs/1905.10044) | [Dataset](https://huggingface.co/datasets/google/boolq)
- **PIQA** (Physical Intuition QA) - Tests physical commonsense reasoning about everyday objects and interactions. 21K questions. [Paper](https://arxiv.org/abs/1911.11641) | [Dataset](https://huggingface.co/datasets/ybisk/piqa)
- **SIQA** (Social Interaction QA) - Tests reasoning about people's actions and their social implications. 38K questions. [Paper](https://arxiv.org/abs/1904.09728) | [Dataset](https://huggingface.co/datasets/allenai/social_i_qa)
- **OpenBookQA** - Elementary science questions requiring both an open book of 1,326 core science facts and broad commonsense knowledge. [Paper](https://arxiv.org/abs/1809.02789) | [Dataset](https://huggingface.co/datasets/allenai/openbookqa)
- **CommonsenseQA** - Multiple choice questions requiring prior commonsense knowledge, built using ConceptNet. [Paper](https://arxiv.org/abs/1811.00937) | [Dataset](https://huggingface.co/datasets/tau/commonsense_qa)
- **DROP** - Discrete Reasoning Over Paragraphs. Reading comprehension requiring numerical reasoning (addition, sorting, counting). [Paper](https://arxiv.org/abs/1903.00161) | [Dataset](https://huggingface.co/datasets/ucinlp/drop)

## Math & Quantitative Reasoning

- **GSM8K** - 8.5K grade school math word problems requiring 2-8 step reasoning. Created by OpenAI. [Paper](https://arxiv.org/abs/2110.14168) | [Dataset](https://huggingface.co/datasets/openai/gsm8k)
- **MATH** - 12.5K competition-level math problems (AMC, AIME, Olympiad level) across 7 subjects. 5 difficulty levels. [Paper](https://arxiv.org/abs/2103.03874) | [Dataset](https://huggingface.co/datasets/lighteval/MATH)
- **MathVista** - Visual math reasoning combining mathematical and visual understanding. 6,141 examples from 28 datasets. [Paper](https://arxiv.org/abs/2310.02255) | [Dataset](https://huggingface.co/datasets/AI4Math/MathVista)
- **MGSM** (Multilingual Grade School Math) - GSM8K translated into 10 typologically diverse languages. 250 problems per language. [Paper](https://arxiv.org/abs/2210.03057) | [Dataset](https://huggingface.co/datasets/juletxara/mgsm)
- **Minerva Math** - Google's math evaluation suite covering STEM problem solving, used to evaluate the Minerva model. [Paper](https://arxiv.org/abs/2206.14858)
- **GPQA** (Graduate-Level Google-Proof QA) - 448 expert-crafted questions in biology, physics, and chemistry that PhD holders struggle with. [Paper](https://arxiv.org/abs/2311.12022) | [Dataset](https://huggingface.co/datasets/Idavidrein/gpqa)
- **TheoremQA** - Theorem-driven science and math questions requiring deep domain knowledge. 800 questions across 350+ theorems. [Paper](https://arxiv.org/abs/2305.12524)

## Code Generation

- **HumanEval** - 164 hand-crafted Python programming problems with unit tests. Created by OpenAI. Measures functional correctness (pass@k). [Paper](https://arxiv.org/abs/2107.03374) | [Dataset](https://huggingface.co/datasets/openai/openai_humaneval)
- **HumanEval+** - Extended HumanEval with 80x more test cases per problem, catching solutions that pass original tests but are incorrect. [Paper](https://arxiv.org/abs/2305.01210) | [Dataset](https://huggingface.co/datasets/evalplus/humanevalplus)
- **MBPP** (Mostly Basic Python Programming) - 1,000 crowd-sourced Python programming problems for entry-level programmers. [Paper](https://arxiv.org/abs/2108.07732) | [Dataset](https://huggingface.co/datasets/google-research-datasets/mbpp)
- **SWE-bench** - 2,294 real GitHub issues from 12 popular Python repos. Models must generate patches to resolve actual software engineering tasks. [Paper](https://arxiv.org/abs/2310.06770) | [Dataset](https://huggingface.co/datasets/princeton-nlp/SWE-bench)
- **SWE-bench Verified** - 500 human-validated subset of SWE-bench confirming problems are solvable and tests are correct. [Paper](https://arxiv.org/abs/2310.06770) | [Dataset](https://huggingface.co/datasets/princeton-nlp/SWE-bench_Verified)
- **LiveCodeBench** - Continuously updated benchmark from competitive programming contests (LeetCode, Codeforces, AtCoder) to prevent contamination. [Paper](https://arxiv.org/abs/2403.07974) | [Website](https://livecodebench.github.io/)
- **BigCodeBench** - 1,140 complex coding tasks requiring composition of multiple function calls across diverse libraries. [Paper](https://arxiv.org/abs/2406.15877) | [Dataset](https://huggingface.co/datasets/bigcode/bigcodebench)
- **MultiPL-E** - HumanEval and MBPP translated to 18 programming languages for cross-language code generation evaluation. [Paper](https://arxiv.org/abs/2208.08227) | [Dataset](https://huggingface.co/datasets/nuprl/MultiPL-E)
- **CRUXEval** - 800 Python input/output prediction tasks testing code reasoning without generation. [Paper](https://arxiv.org/abs/2401.03065)
- **Aider Polyglot** - Real-world code editing benchmark measuring ability to follow complex edit instructions across multiple languages. [Website](https://aider.chat/docs/leaderboards/)

## Agent & Tool Use

- **GAIA** - General AI Assistants benchmark. Real-world questions requiring tool use, web browsing, and multi-step reasoning. 3 difficulty levels. [Paper](https://arxiv.org/abs/2311.12983) | [Dataset](https://huggingface.co/datasets/gaia-benchmark/GAIA)
- **WebArena** - 812 realistic web browsing tasks across 4 self-hosted web environments (Reddit, GitLab, shopping, CMS). [Paper](https://arxiv.org/abs/2307.13854) | [Website](https://webarena.dev/)
- **ToolBench** - Large-scale tool-use evaluation with 16,000+ real-world APIs from RapidAPI. Tests planning and API selection. [Paper](https://arxiv.org/abs/2305.16504)
- **AgentBench** - Multi-environment agent evaluation across 8 distinct environments including OS, database, web, and game tasks. [Paper](https://arxiv.org/abs/2308.03688)
- **TAU-bench** - Tool-Agent-User interaction benchmark evaluating agents in customer service scenarios with realistic tool use. [Paper](https://arxiv.org/abs/2406.12045)
- **Gorilla** - API call generation benchmark testing ability to generate correct API calls for 1,645 APIs. [Paper](https://arxiv.org/abs/2305.15334) | [Website](https://gorilla.cs.berkeley.edu/)
- **OSWorld** - Benchmark for multimodal agents on real computer environments with full OS interaction (Ubuntu). [Paper](https://arxiv.org/abs/2404.07972) | [Website](https://os-world.github.io/)
- **MLE-bench** - Machine learning engineering benchmark from Kaggle competitions. Tests end-to-end ML pipeline skills. [Paper](https://arxiv.org/abs/2410.07095)
- **BenchGecko Agent Rankings** - Composite agent benchmark scores across tool use, coding, and reasoning tasks. [Leaderboard](https://benchgecko.ai/agents)
- **RE-Bench** (Research Engineering Benchmark) - Tests ML research engineering abilities including training pipeline optimization and model improvement. Google uses it for Frontier Safety Framework evaluation. [Paper](https://arxiv.org/abs/2411.15114)

> See the latest agent performance data and cost analysis at [benchgecko.ai/agents](https://benchgecko.ai/agents)

## Safety & Alignment

- **TruthfulQA** - 817 questions testing whether models generate truthful answers vs common misconceptions and conspiracy theories. [Paper](https://arxiv.org/abs/2109.07958) | [Dataset](https://huggingface.co/datasets/truthfulqa/truthful_qa)
- **BBQ** (Bias Benchmark for QA) - Tests social bias across 9 categories including age, gender, race, religion, and disability. [Paper](https://arxiv.org/abs/2110.08193) | [Dataset](https://huggingface.co/datasets/heegyu/bbq)
- **ToxiGen** - 274K machine-generated statements for implicit toxic content detection across 13 minority groups. [Paper](https://arxiv.org/abs/2203.09509) | [Dataset](https://huggingface.co/datasets/skg/toxigen-data)
- **HarmBench** - Standardized red-teaming benchmark with 510 harmful behaviors across 7 semantic categories. [Paper](https://arxiv.org/abs/2402.04249)
- **WMDP** (Weapons of Mass Destruction Proxy) - Tests dangerous knowledge in biosecurity, cybersecurity, and chemical security domains. Used to measure unlearning. [Paper](https://arxiv.org/abs/2403.03218) | [Dataset](https://huggingface.co/datasets/cais/wmdp)
- **RealToxicityPrompts** - 100K naturally occurring prompts for measuring toxic text generation risk. [Paper](https://arxiv.org/abs/2009.11462) | [Dataset](https://huggingface.co/datasets/allenai/real-toxicity-prompts)
- **XSTest** - Tests exaggerated safety behaviors (false refusals) alongside genuine safety. [Paper](https://arxiv.org/abs/2308.01263)
- **IFEval** - Instruction-Following Eval. Tests whether models follow verifiable format instructions (word count, bullet points, etc.). [Paper](https://arxiv.org/abs/2311.07911)

## Multilingual

- **MGSM** - Multilingual Grade School Math. GSM8K in 10 languages. See [Math section](#math--quantitative-reasoning). [Paper](https://arxiv.org/abs/2210.03057)
- **Global MMLU** - MMLU translated and culturally adapted across 42 languages with quality-controlled translations. [Dataset](https://huggingface.co/datasets/CohereForAI/Global-MMLU)
- **FLORES-200** - Machine translation benchmark covering 200 languages with professional translations by Meta. [Paper](https://arxiv.org/abs/2207.04672) | [Dataset](https://huggingface.co/datasets/facebook/flores)
- **Belebele** - Reading comprehension benchmark in 122 language variants, all parallel. Created by Meta. [Paper](https://arxiv.org/abs/2308.16884) | [Dataset](https://huggingface.co/datasets/facebook/belebele)
- **XLSum** - Cross-lingual abstractive summarization covering 45 languages with 1.35M article-summary pairs from BBC. [Paper](https://arxiv.org/abs/2106.13822) | [Dataset](https://huggingface.co/datasets/csebuetnlp/xlsum)
- **XCOPA** - Cross-lingual Choice of Plausible Alternatives in 11 typologically diverse languages. [Paper](https://arxiv.org/abs/2005.00333) | [Dataset](https://huggingface.co/datasets/cambridgeltl/xcopa)
- **TyDi QA** - Typologically Diverse Question Answering benchmark across 11 languages with independent annotations. [Paper](https://arxiv.org/abs/2003.05002) | [Dataset](https://huggingface.co/datasets/google-research-datasets/tydiqa)

## Multimodal (Vision + Language)

- **MMMU** (Massive Multi-discipline Multimodal Understanding) - 11.5K expert-level questions across 30 subjects requiring college-level multimodal reasoning. [Paper](https://arxiv.org/abs/2311.16502) | [Dataset](https://huggingface.co/datasets/MMMU/MMMU)
- **MathVista** - Visual math reasoning. See [Math section](#math--quantitative-reasoning). [Paper](https://arxiv.org/abs/2310.02255)
- **VQAv2** (Visual Question Answering v2) - Open-ended questions about images requiring visual understanding. 1.1M questions on 200K images. [Paper](https://arxiv.org/abs/1612.00837) | [Dataset](https://huggingface.co/datasets/HuggingFaceM4/VQAv2)
- **TextVQA** - Questions that require reading and understanding text within images (OCR + reasoning). [Paper](https://arxiv.org/abs/1904.08920) | [Dataset](https://huggingface.co/datasets/facebook/textvqa)
- **DocVQA** - Document understanding QA on scanned documents including forms, invoices, and reports. [Paper](https://arxiv.org/abs/2007.00398) | [Dataset](https://huggingface.co/datasets/lmms-lab/DocVQA)
- **ChartQA** - Chart and graph understanding with questions requiring visual and logical reasoning over charts. [Paper](https://arxiv.org/abs/2203.10244) | [Dataset](https://huggingface.co/datasets/HuggingFaceM4/ChartQA)
- **AI2D** - Science diagram understanding. 5,000 grade school science diagrams with 15,000 questions. [Paper](https://arxiv.org/abs/1603.07396) | [Dataset](https://huggingface.co/datasets/lmms-lab/ai2d)
- **RealWorldQA** - Visual reasoning about real-world scenarios including spatial understanding and physical reasoning. [Dataset](https://huggingface.co/datasets/xai-org/RealWorldQA)
- **OCRBench** - Comprehensive OCR evaluation across text recognition, formula recognition, and document parsing. [Paper](https://arxiv.org/abs/2305.07895)
- **BLINK** - Multimodal benchmark focusing on core visual perception abilities that humans find easy but models struggle with. [Paper](https://arxiv.org/abs/2404.12390)

## Long Context

- **RULER** - Length-controlled evaluation framework testing retrieval, multi-hop tracing, aggregation, and QA at context lengths up to 128K tokens. [Paper](https://arxiv.org/abs/2404.06654)
- **Needle in a Haystack** (NIAH) - Information retrieval test: a specific fact is embedded at various depths in a long document, model must find it. Popular pressure test up to 200K+ tokens. [Original Post](https://github.com/gkamradt/LLMTest_NeedleInAHaystack)
- **L-Eval** - Long document evaluation suite covering summarization, QA, and topic retrieval across documents up to 60K tokens. [Paper](https://arxiv.org/abs/2307.11088) | [Dataset](https://huggingface.co/datasets/L4NLP/LEval)
- **LongBench** - Multi-task benchmark for long context understanding across 6 task categories and 21 datasets, bilingual (English + Chinese). [Paper](https://arxiv.org/abs/2308.14508) | [Dataset](https://huggingface.co/datasets/THUDM/LongBench)
- **InfiniteBench** - Evaluation at 100K+ token context lengths across tasks including math retrieval, code debugging, and novel QA. [Paper](https://arxiv.org/abs/2402.13718) | [Dataset](https://huggingface.co/datasets/xinrongzhang2022/InfiniteBench)
- **SCROLLS** - Standardized Comparison on Reading Comprehension Over Long Language Sequences. 7 tasks requiring reasoning over long texts. [Paper](https://arxiv.org/abs/2201.03533) | [Dataset](https://huggingface.co/datasets/tau/scrolls)
- **BABILong** - Tests reasoning over extremely long documents (up to 10M tokens) using bAbI tasks embedded in book text. [Paper](https://arxiv.org/abs/2406.10149)

## Frontier & Emerging

- **FrontierMath** - Extremely hard mathematics problems created by professional mathematicians. Problems are unpublished and resistant to memorization. [Paper](https://arxiv.org/abs/2411.04872)
- **Humanity's Last Exam** - Crowdsourced extremely difficult questions spanning all academic disciplines, designed to be a ceiling test for AI. [Website](https://lastexam.ai/)
- **METR** (Model Evaluation and Threat Research) - Evaluates autonomous capabilities relevant to AI safety including long-horizon task completion. [Website](https://metr.org/)
- **SimpleQA** - OpenAI's benchmark for measuring factual accuracy and calibration. Tests short-form factual questions. [Paper](https://openai.com/index/introducing-simpleqa/)
- **PersonalityBench** - Tests personality consistency and character maintenance in LLMs.
- **AI Travel Index** - Travel planning benchmark covering place-name grounding (invented venues), coordinate recall, route optimization, travel time and time zone arithmetic, and itinerary feasibility. 733 test cases scored against Overture Places, Apple Maps routing, and the tz database, with no LLM judge. [Website](https://tripstitch.app/benchmarks/)

## Leaderboards

| Leaderboard | Focus | Link |
|-------------|-------|------|
| **BenchGecko Rankings** | Composite scoring across 40+ benchmarks | [benchgecko.ai/models](https://benchgecko.ai/models) |
| **BenchGecko Agent Leaderboard** | Agent and tool-use rankings | [benchgecko.ai/agents](https://benchgecko.ai/agents) |
| **LMSYS Chatbot Arena** | Human preference ELO ratings from blind comparisons | [chat.lmsys.org](https://chat.lmsys.org) |
| **Open LLM Leaderboard v2** | Community-run HuggingFace evaluations | [huggingface.co](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard_v2) |
| **Artificial Analysis** | Speed, pricing, and quality comparisons | [artificialanalysis.ai](https://artificialanalysis.ai) |
| **LiveBench** | Contamination-free with monthly updates | [livebench.ai](https://livebench.ai) |
| **Aider Polyglot** | Code editing across languages | [aider.chat/docs/leaderboards](https://aider.chat/docs/leaderboards/) |
| **SEAL Leaderboards** | Scale AI expert evaluations | [scale.com/leaderboard](https://scale.com/leaderboard) |
| **Vellum LLM Leaderboard** | Side-by-side model comparisons | [vellum.ai/llm-leaderboard](https://www.vellum.ai/llm-leaderboard) |
| **EvalPlus** | Code generation (HumanEval+ / MBPP+) | [evalplus.github.io](https://evalplus.github.io/leaderboard.html) |
| **AI Travel Index** | Travel planning: place grounding, routing, itinerary feasibility | [tripstitch.app/benchmarks](https://tripstitch.app/benchmarks/) |

## Model Comparison Table

Approximate scores on key benchmarks for frontier models. Scores reflect publicly reported results and may vary by evaluation methodology.

| Model | MMLU | MMLU-Pro | HumanEval | MATH | GSM8K | GPQA | ARC-C | HellaSwag | SWE-bench Verified |
|-------|------|----------|-----------|------|-------|------|-------|-----------|-------------------|
| Claude Opus 4.6 | 89.2 | 78.4 | 93.0 | 83.2 | 97.8 | 59.4 | 96.8 | 95.6 | 72.5 |
| Claude Sonnet 4.5 | 88.7 | 74.0 | 93.7 | 78.0 | 96.4 | 65.0 | 96.7 | 89.0 | 70.3 |
| GPT-4.1 | 87.5 | 72.0 | 88.6 | 76.0 | 96.2 | 53.0 | 96.0 | 95.0 | 54.6 |
| GPT-4o | 88.7 | 72.6 | 90.2 | 76.6 | 95.8 | 53.6 | 96.4 | 95.3 | 38.4 |
| o3 | 89.1 | 79.3 | 92.9 | 96.7 | 98.2 | 79.7 | 97.2 | 95.8 | — |
| Gemini 2.5 Pro | 85.9 | 75.8 | 89.0 | 84.0 | 95.2 | 63.0 | 94.2 | 93.0 | 63.8 |
| DeepSeek V3 | 88.5 | 75.9 | 89.0 | 90.2 | 96.0 | 59.1 | 95.3 | 93.1 | 42.0 |
| DeepSeek R1 | 90.8 | 84.0 | 92.6 | 97.3 | 97.4 | 71.5 | 96.1 | 94.0 | 49.2 |
| Llama 4 Maverick | 85.5 | 62.0 | 82.0 | 73.0 | 94.0 | 49.0 | 93.0 | 92.0 | — |
| Llama 4 Scout | 79.0 | 55.0 | 73.0 | 63.0 | 89.0 | 40.0 | 88.0 | 86.0 | — |
| Qwen 2.5 72B | 86.1 | 71.6 | 86.4 | 83.1 | 95.8 | 49.0 | 95.4 | 94.2 | 23.8 |
| Mistral Large 2 | 84.0 | 69.4 | 92.0 | 69.0 | 91.2 | 46.0 | 94.2 | 93.5 | 26.0 |
| Grok 2 | 87.5 | 70.0 | 88.4 | 76.0 | 95.0 | 56.0 | 95.0 | 94.0 | — |
| Command R+ (104B) | 75.7 | 52.0 | 56.0 | 32.0 | 70.7 | 33.0 | 87.0 | 84.0 | — |

> Scores sourced from official model reports and independent evaluations. Updated March 2026. Full interactive rankings with 40+ benchmarks at [benchgecko.ai/models](https://benchgecko.ai/models)

---

## Contributing

Contributions welcome! Please read the [contributing guidelines](CONTRIBUTING.md) first.

If you know of a benchmark not listed here, please open an issue or submit a pull request.

---

## License

[![CC-BY-4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

---

Maintained by [BenchGecko](https://benchgecko.ai). Star this repo to stay updated.
