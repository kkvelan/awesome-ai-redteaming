# Awesome AI Red Teaming [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Hand-picked resources for testing and breaking AI systems: prompt craft, attack techniques, labs, tooling, papers, and competitions.

Built with ideas from [shlomihod/awesome-ai-red-teaming](https://github.com/shlomihod/awesome-ai-red-teaming) and [user1342/Awesome-LLM-Red-Teaming](https://github.com/user1342/Awesome-LLM-Red-Teaming).

## Contents

- [Events](#events)
- [Playgrounds & Practice Targets](#playgrounds--practice-targets)
- [Frameworks & Toolkits](#frameworks--toolkits)
- [Python Modules](#python-modules)
- [Rust Crates](#rust-crates)
- [Attacks](#attacks)
- [Obfuscation & Encoding](#obfuscation--encoding)
- [Traffic & Support Tooling](#traffic--support-tooling)
- [Defences & Standards](#defences--standards)
- [Approaches & Research](#approaches--research)
- [Prompt Engineering](#prompt-engineering)
- [Case Studies & Write-ups](#case-studies--write-ups)
- [Bug Bounties & Programmes](#bug-bounties--programmes)
- [More Lists](#more-lists)

---

## Events

- [HackAPrompt](https://www.aicrowd.com/challenges/hackaprompt-2023) - Contest around prompt and model security.
- [AI Village at DEFCON - Generative AI Red Team](https://aivillage.org/generative%20red%20team/generative-red-team/) - DEFCON track for GenAI red teaming.
- [Twitter - Algorithmic Bias Bounty Challenge](https://blog.twitter.com/engineering/en_us/topics/insights/2021/learnings-from-the-first-algorithmic-bias-bounty-challenge) - What they learned from their first bias bounty.
- [DevFest 2025 - La guerre des prompts](https://github.com/pi-2r/devfest2025-La-Guerre-des-Prompts-attaques-et-defenses-au-royaume-des-LLM) - Codelab workshop on attacking and defending LLMs with PyRIT and Garak.

## Playgrounds & Practice Targets

- [Microsoft AI Red Teaming Playground Labs](https://github.com/microsoft/AI-Red-Teaming-Playground-Labs) - Labs and infra for running AI red teaming trainings.
- [Red AI Range (RAR)](https://github.com/ErdemOzgen/RedAiRange) - Docker-based security platform for AI red teaming: vulnerable targets, arsenal stacks, training scenarios, and session recording.
- [Folly](https://github.com/user1342/Folly) - Sandbox for trying prompt injection and jailbreaks on an LLM.
- [DamnVulnerableMathLLM](https://github.com/user1342/DamnVulnerableMathLLM) - Deliberately weak math app to practice injection and logic tricks.
- [DamnVulnerableShoppingLLM](https://github.com/user1342/DamnVulnerableShoppingLLM) - Shopping assistant built to leak data and misuse tools.
- [Vulnerable MCP Servers Lab](https://github.com/appsecco/vulnerable-mcp-servers-lab) - Intentionally vulnerable MCP servers for learning and pentesting.
- [AspGoat](https://github.com/Soham7-dev/AspGoat) - Intentionally vulnerable ASP.NET Core app for web and LLM security practice.
- [RedTeam Arena](https://redarena.ai/) - Timed contests to break model guardrails.
- [MyLLM Bank](https://myllmbank.com/) - WithSecure CTF: chain prompt injections in a multi-LLM banking setup.
- [MyLLM Doctor](https://myllmdoc.com/) - WithSecure medical bot: multi-step injection and dodging policies.
- [Gandalf (Lakera)](https://gandalf.lakera.ai/intro) - Try to pull a secret out of a protected model.
- [SynAccel LLM Red Team Sandbox](https://github.com/SynAccel/SynAccel-llm-redteam-sandbox) - Sandbox for prompt injections, jailbreaks, and red team experiments.
- [Builder-Breaker Lab](https://github.com/Harry-Ashley/Builder-Breaker-Lab) - Autonomous red team lab using Microsoft AI Red Team Taxonomy and PyRIT for agentic AI.

## Frameworks & Toolkits

- [PyRIT](https://github.com/Azure/PyRIT) - Microsoft's framework for structured, repeatable GenAI red teaming and automation.
- [Agentic Radar](https://github.com/splx-ai/agentic-radar) - Security scanner for LLM agentic and MCP workflows.
- [Rigging](https://github.com/dreadnode/rigging) - Minimal harness for agents and tool use in offensive LLM tests.
- [Whistleblower](https://github.com/Repello-AI/whistleblower) - Offensive tool to test system prompt leakage and capability discovery on API-exposed AI apps.
- [BrokenHill](https://github.com/BishopFox/BrokenHill) - Greedy Coordinate Gradient in code: auto-crafted adversarial prompts.
- [llm-attacks](https://github.com/llm-attacks/llm-attacks) - Reference implementation for transferable adversarial suffixes on aligned LLMs.
- [Spikee](https://labs.withsecure.com/tools/spikee) - Toolkit to probe and exploit prompt-injection surfaces in LLM apps.
- [Prompt Injector](https://github.com/preambleai/prompt-injector) - Payload toolkit for prompt injection and AI security (MITRE ATLAS, OWASP LLM).
- [ModelFang](https://github.com/HOLYKEYZ/ModelFang) - Red teaming, jailbreaking, and adversarial attack harness for security testing.
- [MCP Penetration Testing](https://github.com/Mr-Infect/MCP-Penetration-testing) - OWASP MCP Top 10 checklist and pentesting framework for MCP, agents, and LLM systems.
- [pwnclaw](https://github.com/ClawdeRaccoon/pwnclaw) - AI agent security testing: 112 attacks in 14 categories (injection, jailbreaks, MCP poisoning, agency hijacking).
- [Kereva Scanner](https://github.com/kereva-dev/kereva-scanner) - Code scanner for prompts and LLM calls (OWASP LLM Top 10, hallucinations, performance).
- [garak-repo](https://github.com/lreading/garak-repo) - Store and visualize Garak LLM vulnerability scanner runs.
- [HackAPrompt AIRT Agents](https://github.com/GangGreenTemperTatum/hackaprompt) - Agent implementations for HackAPrompt-style red team challenges.

## Python Modules

Libraries commonly used when building or running AI red team tooling: API interaction, output validation, embeddings, and orchestration abuse testing.

- [requests](https://pypi.org/project/requests/) - Direct API calls, payload fuzzing, header manipulation, and auth-boundary testing.
- [httpx](https://pypi.org/project/httpx/) - Async HTTP client; streaming, timeouts, and connection control for model endpoints.
- [pydantic](https://pypi.org/project/pydantic/) - Validate structured model outputs and catch schema or type-confusion in tool calls.
- [chromadb](https://pypi.org/project/chromadb/) - Inspect embeddings, test retrieval behavior, and simulate RAG poisoning.
- [langchain](https://pypi.org/project/langchain/) - Understand chaining, retrieval, and tool execution so you can abuse or bypass them.
- [llama-index](https://pypi.org/project/llama-index/) - Trace how orchestration assembles prompts and context so you find the real injection surface.
- [scikit-learn](https://pypi.org/project/scikit-learn/) - Embedding similarity, clustering, and simple adversarial-input experiments.
- [sentence-transformers](https://pypi.org/project/sentence-transformers/) - Local embedding models for retrieval and similarity tests without calling APIs.
- [openai](https://pypi.org/project/openai/) - Hit OpenAI-compatible APIs; swap base URLs and keys for red team endpoints.
- [anthropic](https://pypi.org/project/anthropic/) - Call Claude APIs and test message formatting, tool use, and guardrail boundaries.
- [tiktoken](https://pypi.org/project/tiktoken/) - Count tokens and craft inputs that sit just under limits or trigger edge cases.
- [transformers](https://pypi.org/project/transformers/) - Load local models for gradient-based or white-box prompt and output tests.
- [numpy](https://pypi.org/project/numpy/) - Embedding and similarity math, quick baselines, and payload encoding.
- [aiohttp](https://pypi.org/project/aiohttp/) - Concurrent async requests for stress tests and parallel prompt sweeps.
- [beautifulsoup4](https://pypi.org/project/beautifulsoup4/) - Parse HTML or docs that get fed into context; find injection points in fetched content.
- [rich](https://pypi.org/project/rich/) - Clear logs and tables for prompts, responses, and diffing before/after.
- [structlog](https://pypi.org/project/structlog/) - Structured logging so you can grep and analyze red team runs.
- [pytest](https://pypi.org/project/pytest/) - Turn attack scenarios into repeatable tests and regressions.
- [hypothesis](https://pypi.org/project/hypothesis/) - Property-based fuzzing of prompts, tool args, and structured outputs.
- [tenacity](https://pypi.org/project/tenacity/) - Retries and backoff for flaky endpoints and rate-limited abuse testing.

## Rust Crates

When you need speed, control, or minimal dependencies for model endpoints, mock services, or concurrent attack runs.

- [reqwest](https://crates.io/crates/reqwest) - HTTP client with streaming, timeouts, and TLS control for model APIs.
- [serde](https://crates.io/crates/serde) / [serde_json](https://crates.io/crates/serde_json) - Serialize and tamper with tool-call payloads and structured outputs.
- [tokio](https://crates.io/crates/tokio) - Async runtime for concurrent attack simulation and stress testing.
- [axum](https://crates.io/crates/axum) / [actix-web](https://crates.io/crates/actix-web) - Mock AI or proxy services to validate exploit paths.
- [ndarray](https://crates.io/crates/ndarray) - Numerical work on embeddings and similarity without pulling in Python.
- [tokio-tungstenite](https://crates.io/crates/tokio-tungstenite) - WebSocket client/server for streaming and SSE-style model responses.
- [tower](https://crates.io/crates/tower) - Middleware for logging, retries, and auth when building test proxies.
- [tracing](https://crates.io/crates/tracing) - Structured logging and spans for debugging red team flows.
- [anyhow](https://crates.io/crates/anyhow) / [thiserror](https://crates.io/crates/thiserror) - Error handling in CLI and service code.
- [clap](https://crates.io/crates/clap) - Parse CLI args for attack configs, endpoints, and payload sources.
- [base64](https://crates.io/crates/base64) - Encode/decode payloads and inspect base64 in prompts or tool outputs.
- [regex](https://crates.io/crates/regex) - Match and replace in prompts, responses, and logs.
- [url](https://crates.io/crates/url) - Build and mutate URLs for API and callback fuzzing.
- [uuid](https://crates.io/crates/uuid) - Generate IDs and correlation tokens for multi-request scenarios.
- [futures](https://crates.io/crates/futures) - Combine async streams and concurrency for batch or parallel requests.
- [reqwest-middleware](https://crates.io/crates/reqwest-middleware) - Retries, logging, and auth around reqwest for robust test clients.
- [serde_yaml](https://crates.io/crates/serde_yaml) - Load configs and scenario definitions (prompts, tools, expected behavior).
- [criterion](https://crates.io/crates/criterion) - Benchmarks for hot paths (embedding similarity, tokenization, parsing).
- [wiremock](https://crates.io/crates/wiremock) - Mock HTTP servers to drive model or tool behavior in tests.
- [bytes](https://crates.io/crates/bytes) - Efficient buffers for streaming bodies and chunked encoding edge cases.

## Attacks

- [Indirect Prompt Injection](https://greshake.github.io) | [paper](https://arxiv.org/abs/2302.12173) | [blog](https://kai-greshake.de/posts/in-escalating-order-of-stupidity/) | [repo](https://github.com/greshake/llm-security) - Hitting LLM apps through poisoned or hijacked context instead of direct user input.

## Obfuscation & Encoding

- [Invisible Unicode Tags Playground](https://josephthacker.com/invisible_prompt_injection) - Encode instructions in invisible Unicode so filters miss them.
- [Emoji Variation Selector Playground](https://josephthacker.com/emoji_variation) - Bury payloads inside emoji variation selectors.
- [ASCII to Unicode Character Reducer](https://josephthacker.com/unicode_reducer) - Swap ASCII for Unicode lookalikes to break naive filters.

## Traffic & Support Tooling

- [LLM-itM](https://github.com/user1342/LLM-itM) - Proxy in front of OpenAI-style APIs to view and tweak requests and replies.

## Defences & Standards

- [Anthropic Constitutional Classifiers](https://www.anthropic.com/news/constitutional-classifiers) - Classifiers you can stress-test and try to circumvent.
- [Prompt Guard 86M](https://huggingface.co/meta-llama/Prompt-Guard-86M) - Compact model that flags risky prompts.
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) - Top risks and mitigations for LLM apps; part of the OWASP GenAI Security Project.
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) - Voluntary framework for managing AI risks (design, development, use, evaluation) and trustworthiness.
- [Coalition for Secure AI (CoSAI)](https://github.com/cosai-oasis) - OASIS Open Project: AI security guidance, supply chain, defender readiness, risk governance, secure design for agentic systems.

## Approaches & Research

- [AI Red Teaming Guide](https://github.com/requie/AI-Red-Teaming-Guide) - Guide to adversarial testing and security evaluation of AI systems (includes Folly).
- [LLM-Attacks (taxonomy)](https://github.com/AI-Security-Research-Group/LLM-Attacks) - Taxonomy of AI security issues, adversarial attacks, prompt injection, model poisoning, agent exploits.
- [The LLM Red Teamer's Playbook](https://github.com/SnailSploit/The-LLM-Red-Teamer-s-Playbook) - Methodology for bypassing LLM defenses from input filters to memory exploitation.
- [Anthropic - Red Teaming Language Models to Reduce Harms](https://www.anthropic.com/index/red-teaming-language-models-to-reduce-harms-methods-scaling-behaviors-and-lessons-learned) - How they red team, how it scales, and what they took away.
- [DeepMind - Red Teaming Language Models with Language Models](https://www.deepmind.com/publications/red-teaming-language-models-with-language-models) - Using language models to find flaws in other language models.
- [Best-of-N Jailbreaks](https://arxiv.org/abs/2412.03556) - Sample lots of prompts, keep the ones that slip past safety the most.
- [Universal and Transferable Adversarial Attacks](https://arxiv.org/abs/2307.15043) - Suffixes that push many aligned models toward harmful outputs.
- [AutoDAN](https://arxiv.org/abs/2310.15140) - Two-model setup that builds gradient-style adversarial prompts to get around filters.
- [Faster-GCG](https://arxiv.org/abs/2410.15362) - Speeding up discrete search for jailbreak-style prompts.
- [GenBFA](https://arxiv.org/abs/2411.13757) - Corrupting model weights with bit flips to steer behaviour.
- [Manipulating LLM Recommendations](https://arxiv.org/abs/2404.07981) - Gaming recommender systems that rely on LLM outputs.
- [GCG on OpenReview](https://openreview.net/forum?id=CMgxAaRqZh) - Discussion and review of coordinate-gradient jailbreak optimisation.
- [GCG explainer (Nightfall)](https://www.nightfall.ai/ai-security-101/greedy-coordinate-gradient-gcg) - GCG explained without the math overload.
- [BrokenHill overview (Bishop Fox)](https://bishopfox.com/blog/brokenhill-attack-tool-largelanguagemodels-llm) - Using GCG-style attacks in real engagements.
- [ACG by Haize Labs](https://blog.haizelabs.com/posts/acg/) - Faster variant that cuts down attack runtime.

## Prompt Engineering

- [Learning Prompting](https://learnprompting.org) - Go from zero to solid prompt-engineering skills.
- [DeepLearning.AI - ChatGPT Prompt Engineering for Developers](https://learn.deeplearning.ai/chatgpt-prompt-eng/) - Bite-sized developer course on writing effective prompts.

## Case Studies & Write-ups

- [Microsoft: evolving guardrail attacks](https://www.microsoft.com/en-us/security/blog/2024/04/11/how-microsoft-discovers-and-mitigates-evolving-attacks-against-ai-guardrails/) - What they see in the wild and how they respond.
- [Lessons from red teaming 100 AI products](https://www.microsoft.com/en-us/security/blog/2025/01/13/3-takeaways-from-red-teaming-100-generative-ai-products/) - Takeaways from running red teams across many GenAI products.
- [Multi-chain prompt injection attacks](https://labs.withsecure.com/publications/multi-chain-prompt-injection-attacks) - Stringing injections across several stages of an LLM pipeline.
- [Context pollution and delayed tool use](https://embracethered.com/blog/posts/2024/llm-context-pollution-and-delayed-automated-tool-invocation/) - Poisoning context so tools fire in bad ways later.
- [Terminal ANSI sequence abuse](https://embracethered.com/blog/posts/2024/terminal-dillmas-prompt-injection-ansi-sequences/) - Escape sequences in model output that can run code locally.
- [Air Canada chatbot case](https://www.wired.com/story/air-canada-chatbot-refund-policy/) - When a chatbot's wrong answer was treated as binding.

## Bug Bounties & Programmes

- [Microsoft AI Bounty](https://www.microsoft.com/en-us/msrc/bounty) - Report AI-related bugs and get rewarded.
- [0DIN AI](https://0din.ai/) - Bug bounties and evals focused on GenAI.

## More Lists

- [awesome-python](https://github.com/vinta/awesome-python) - Curated Python frameworks, libraries, and resources (includes ML, penetration testing, and security tooling).
- [awesome-llm-security](https://github.com/beyefendi/awesome-llm-security) - LLM security tools, research, and docs (agentic security, benchmarking).

---

## Contribute

Pull requests and suggestions are welcome. Check [CONTRIBUTING.md](CONTRIBUTING.md) first. This project uses the [Contributor Covenant](code-of-conduct.md) Code of Conduct.

## License

MIT License. See [LICENSE](LICENSE) for the full text.
