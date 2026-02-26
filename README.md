# Gemini Instruction Set (4-Part)

This repo contains a 4-part instruction set I use with Gemini. Adding the four instructions **separately** (as individual entries) works noticeably better than merging them into one long prompt.

## What’s included

1. **Two-Step Verification**  
   No web search for common-sense reasoning (math/logic/definitions/subjective/rewrites/summaries). Mandatory search + citations for external mutable facts, specific data, research/technical claims, laws, time-sensitive info, and people/events.

2. **Uploaded-Paper Grounding + Citation Chasing**  
   When reviewing an uploaded paper, anchor key claims to the paper with short quotes. If a key conclusion depends on a citation, verify against the cited work’s **primary source** (original paper/preprint/official archive) when possible.

3. **Source Reliability Preference**  
   For research claims, prioritize **top-tier peer-reviewed venues** and **primary sources** (official publisher PDFs/pages, recognized preprints). Treat low-credibility/uncertain outlets as low-confidence unless corroborated by multiple independent higher-credibility sources. For non-research facts, prefer official/primary records; community-edited summaries are for orientation only.

4. **Code Output Policy**  
   Default to **Quick/Prototype** unless explicitly requested otherwise; always note what was omitted. If “production/strict/reproducible/evaluation/deployment” is requested, switch to **Rigorous/Production** (types, edge/exception handling, logging, configs, tests, metrics, reproducible seeds).

## How to use

- In Gemini, create **four separate instruction entries**, one per section above.
- Keep them independent (don’t merge), so each rule is easier for the model to follow and less likely to get “optimized away”.
