# Jeremy Lancaster

**Principal software engineer. I build production AI systems that are reliable, observable, and running on infrastructure you control.**

20+ years shipping backend systems: carrier integrations handling 180K–200K+ requests a minute, a data pipeline that crawls half a million organizations a month, and LLM pipelines running on hardware I own. I care most about the parts of AI work that don't demo well: validation, retries, observability, and a clear answer to "what happens when this breaks?"

Charlotte, NC area · Remote (US) · [consultjl.com](https://consultjl.com)

## Selected work

Most of what I've built lives in private repos that belong to employers and clients. The write-ups are the best window into it:

- **[Technographic pipeline, 515K organizations a month](https://consultjl.com/case-studies/technographic-pipeline)** — why v2 threw out its own queue system. Five stages, files as state, an 18-feature Random Forest matcher at 92% held-out accuracy.
- **[Multilingual video platform on owned GPUs](https://consultjl.com/case-studies/multilingual-video-platform)** — Whisper, vLLM, and llama.cpp in two deliberate pipelines, with deterministic checks between the LLM and anything published. 5,522 translation jobs in one night, zero permanent failures.
- **[Contract-driven hybrid semantic search](https://consultjl.com/case-studies/semantic-search-architecture)** — pgvector and lexical retrieval fused by reciprocal-rank fusion, fed by one contract across three ingest paths. Search went from ~2.2 s to ~140 ms.

## A few receipts

- Tripled throughput and cut CPU ~70% on a high-volume Python carrier service: WSGI runtime migration, asyncio fixes, hard timeouts, backpressure-aware circuit breakers.
- Diagnosed and resolved a production UPS rate-limiting crisis: found the request amplification in rate shopping, built hybrid fallback routing and multi-account round-robin, and worked the capacity increase with UPS engineering.
- Took a stalled batch transcription job from under 2,500 videos in a month to saturating the NIC and the GPU in separate phases.
- Found a 24× llama.cpp speedup hiding behind one missing flag, on line 7 of a boot log.

## What I'm building now

- **Edwin** — an agent runtime in Go for production AI workflows.
- **Shepherd's Study** — a research RAG tool over commentaries, public-domain sermons, and theological literature.
- **LLM-JEPA for theological reasoning** — Meta's Joint Embedding Predictive Architecture applied to Reformed catechism corpora, with a 546-pair evaluation set (TheoBench). Full paper draft done.
- **Distributed speculative decoding** across a DGX Spark and an RTX 4090 workstation. Write-up in progress.

## How I build

- Match the primitive to the workload. A queue isn't architecture if there's no variance to buffer.
- Put deterministic code between the LLM and the user. The model doesn't get to grade itself.
- Read the boot logs of every component you don't own.
- When the system is guessing, tell the user.

## Stack

Python · Go · Ruby · TypeScript · PostgreSQL + pgvector · Redis · Kafka · vLLM · llama.cpp · Whisper · Kubernetes · Docker · AWS · Cloudflare

## Work with me

I take on a small number of consulting engagements at a time through RSA Industries.

[Book a 30-minute call](https://calendar.app.google/kBu7AzEUFejB6QBq9) · [consultjl.com](https://consultjl.com) · [LinkedIn](https://www.linkedin.com/in/jeremy-lancaster-rsa-tech/) · jeremy@consultjl.com
