# AI Vendor Risk Assessment: Anthropic (Claude AI Platform)

**Assessor:** Mike Capela, CISSP  
**Framework:** NIST AI Risk Management Framework (AI RMF 1.0)  
**Date:** September 2026  
**Version:** 2.1 (human-reviewed, error-corrected; errata below)

---

## What this is

A Claude-assisted AI vendor risk assessment of Anthropic, mapped to the NIST AI Risk Management Framework. The assessment evaluates Anthropic's publicly available documentation across 20 questions spanning Govern, Map, Measure, Manage, and AI Supply Chain — then documents where the AI got it right, where it got it wrong, and what that tells us about using LLMs for governance work.

This is a proof of concept, not a product. It demonstrates that LLM-assisted vendor risk assessment is viable as a time-saving tool — provided the human reviewer brings domain expertise and knows where to look for the errors the AI can't catch on its own.

## Why I built it

I spent 20 years in IT security and infrastructure — blue-team defensive security at a major bank (SOX environment), DoD network support with a Secret clearance, and seven years as the third-party vendor with privileged access to dozens of client environments at an MSP. I've sat on both sides of the vendor-assessment table.

I'm now pivoting into AI governance, and I wanted to answer a practical question: can an LLM meaningfully accelerate a vendor risk assessment, or does it just produce confident-sounding noise that a practitioner has to redo from scratch?

The answer is somewhere in between — and the details of *where* it succeeds and fails are more interesting than a simple yes or no.

## Key findings

**What Claude got right:**
- Document inventory — correctly identified which documents were reviewed and which were gated. Zero hallucinated sources.
- Evidence extraction — factual claims about document contents were accurate across all 20 questions. No fabricated citations.
- Framework mapping — NIST AI RMF categorization was appropriate throughout.

**What Claude got wrong (three systematic patterns):**

1. **Wrong audit lens.** Claude applied an internal-audit standard to a public-information assessment, repeatedly flagging the absence of internal governance details (escalation org charts, named risk owners, incident playbooks) as deficiencies. A practitioner recognizes these as expected scope limitations — no vendor publishes this information, and doing so could be a security risk.

2. **Evidence limited to uploaded documents.** Claude only assessed what was directly provided. It did not search for publicly available third-party benchmarks, published vendor research, or independent evaluations. A competent human assessor naturally looks beyond the vendor's own trust center.

3. **Overweighted contractual boilerplate.** Claude cited a DPA's 48-hour breach-notification commitment as meaningful evidence of incident-response capability. Anyone who's handled a real breach knows this is legally required boilerplate — in practice, organizations invoke law enforcement exceptions that delay disclosure indefinitely. The contract says one thing; the industry practice is something else.

**The conclusion:** The AI produced a structurally sound, factually accurate first draft that required human correction primarily in scope judgment, evidence sourcing, and practitioner context — not in factual accuracy. The errors were consistently in areas where operational experience matters more than document analysis.

## What's in this repo

| File | Description |
|------|-------------|
| `AI_Vendor_Risk_Assessment_Anthropic_v2.pdf` | The complete v2 assessment (8 pages) — all 20 questions with ratings, evidence citations, gap notes, summary of findings, and full error analysis with detailed error log. See Errata for corrections not yet reflected in the PDF. |
| `questionnaire-template/NIST_AI_RMF_Vendor_Questionnaire_v1.md` | The reusable questionnaire template (21 questions mapped to NIST AI RMF, including SC4 on data residency added after v2 review) — use it to assess any AI vendor |

## Rating summary (v2.1)

| Rating | Count | Questions |
|--------|-------|-----------|
| Supported | 10 | G1, G3, G4, G5, M1, M4, ME4, MA2, MA4, SC1 |
| Partially Supported | 9 | G2, M2, M3, ME1, ME2, ME3, MA1, SC2, SC3 |
| Not Addressed | 1 | MA3 (under re-review — see Errata) |
| **Total** | **20** | |

## Errata (v2.1, September 2026)

Found during a structured re-review of v2 while building the next version of the method. Recorded here rather than silently corrected — the point of this project is documenting where the process fails.

1. **Question count.** v2.0 stated 18 questions. The assessment rates 20 (G1–G5, M1–M4, ME1–ME4, MA1–MA4, SC1–SC3). The v2.0 summary also listed 9 questions as Partially Supported while stating a count of 7. Correct tally: 10 Supported, 9 Partially Supported, 1 Not Addressed. The PDF still shows the v2.0 counts.
2. **MA3 is a false negative.** v2 rated model retirement/rollback "Not Addressed." Anthropic publicly documents a [model deprecation policy](https://platform.claude.com/docs/en/about-claude/model-deprecations) (defined lifecycle stages; at least 60 days' notice before retirement of publicly released models) and published [commitments on model deprecation and preservation](https://www.anthropic.com/research/deprecation-commitments) (November 2025). Retirement is addressed; rollback is not. MA3 will be re-rated in the next assessment run. This is error pattern #2 (evidence limited to what was supplied) recurring after the v2 correction — which is why the next method version makes a documented search checklist mandatory before any question can be rated Not Addressed.

## Methodology

This assessment was conducted through a structured, Claude-assisted analysis — not an automated workflow. Vendor documentation was uploaded to Claude, which extracted controls and claims, mapped findings to the questionnaire, and flagged gaps. The assessor then reviewed the output against source documents, identified errors, iterated prompts, and documented the error analysis.

**Documents reviewed:** Trust Center, Data Processing Addendum, Usage Policy, Claude's Constitution, Privacy Policy, Responsible Scaling Policy v3.4, Advanced AI Framework, 2025 Type 2 SOC 3 Report, and independent third-party benchmarks (Artificial Analysis).

A future version of this project will automate the analysis as a repeatable agent workflow with web search, scope-aware prompting, and the error-pattern library encoded as system-prompt rules.

## Version history

| Version | Date | Change |
|---------|------|--------|
| 2.1 | September 2026 | Errata: question count corrected to 20, rating tally corrected, MA3 flagged as false negative |
| 2.0 | September 2026 | Human-reviewed, error-corrected assessment with error analysis |
| 1.0 | August 2026 | Claude-assisted first pass |

## About me

Mike Capela — CISSP (endorsed in Risk Management and Vulnerability Management), 20+ years in IT security and infrastructure across financial services (Wells Fargo, SOX environment), defense (Honeywell/AFSCN, Secret clearance), and managed services. U.S. Army veteran. Currently pivoting into AI governance and vendor risk.

- Building AI-assisted assessment tools that encode practitioner judgment
- Studying for the IAPP AIGP certification
- Author — book manuscript submitted to publisher

## License

This assessment and questionnaire template are released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Use them, adapt them, assess your own vendors — just credit the source.
