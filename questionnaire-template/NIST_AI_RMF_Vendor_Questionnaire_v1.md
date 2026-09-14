# AI Vendor Risk Questionnaire
## Mapped to NIST AI Risk Management Framework (AI RMF 1.0)

**Version:** 1.0  
**Author:** Mike Capela, CISSP  
**License:** CC BY 4.0  

Use this questionnaire to assess any AI vendor's publicly available documentation against the NIST AI RMF. For each question, cite the specific document and section that supports your rating.

---

## Rating scale

| Rating | Definition |
|--------|-----------|
| **Supported** | Public documentation provides clear, specific evidence addressing the question. |
| **Partially Supported** | Evidence exists but is incomplete, general, or lacks specificity. |
| **Unsupported** | A claim is made but no substantiating evidence is publicly available. |
| **Not Addressed** | The topic is not mentioned in publicly available documentation. |
| **Gated** | Evidence is claimed to exist behind a request-access gate; content not independently verified. |

**Before you begin:** Determine your access level (public-only, NDA-protected, or internal audit). If public-only, do not flag the absence of internal governance details as deficiencies — these are scope limitations, not findings.

---

## GOVERN — Organizational governance for AI risk

**G1.** Does the vendor have a published AI governance policy or responsible AI framework?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**G2.** Is there a named AI risk owner or governance body with defined accountability?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**G3.** Does the vendor have documented escalation paths for AI-related incidents or safety concerns?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**G4.** Does the vendor maintain AI-specific policies covering ethics, fairness, and responsible use?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**G5.** Does the vendor conduct and publish AI risk assessments or safety evaluations?  
Rating: ___  
Evidence:  
Gaps / Notes:  

---

## MAP — Context, scope, and known limitations

**M1.** Is the AI system's intended use clearly defined and documented?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**M2.** Are known limitations and failure modes documented?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**M3.** Is training data provenance disclosed?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**M4.** Are third-party model dependencies or foundational-model provenance identified?  
Rating: ___  
Evidence:  
Gaps / Notes:  

---

## MEASURE — Metrics, testing, and monitoring

**ME1.** Does the vendor publish evaluation metrics, benchmarks, or performance data?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**ME2.** Is there documented bias or fairness testing?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**ME3.** Is there a monitoring plan for model drift, degradation, or emergent behavior?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**ME4.** Does the vendor engage independent third-party evaluators?  
Rating: ___  
Evidence:  
Gaps / Notes:  

---

## MANAGE — Risk treatment and response

**MA1.** Is there a documented incident response plan for AI-specific failures?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**MA2.** Are there human-oversight mechanisms for AI system outputs?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**MA3.** Is there a decommissioning, rollback, or model-retirement plan?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**MA4.** Does the vendor have contractual commitments for data deletion and return?  
Rating: ___  
Evidence:  
Gaps / Notes:  

---

## AI SUPPLY CHAIN — Dependencies and concentration risk

**SC1.** Does the vendor disclose subprocessor relationships?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**SC2.** Is there concentration risk in infrastructure or model providers?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**SC3.** Does the vendor have business continuity and disaster recovery commitments?  
Rating: ___  
Evidence:  
Gaps / Notes:  

**SC4.** *(Added in v2)* Can customers contractually restrict data processing to specific geographic regions?  
Rating: ___  
Evidence:  
Gaps / Notes:  

---

## Practitioner notes

Three common LLM error patterns identified during Claude-assisted assessment (encode these in your system prompt if automating):

1. **Wrong audit lens:** If the assessment is public-information-only, the absence of internal governance details is a scope limitation, not a finding. Do not flag it as a deficiency.

2. **Evidence beyond the vendor's own docs:** Search for independent third-party benchmarks, published research, regulatory filings, and news coverage. Do not limit the assessment to uploaded documents.

3. **Boilerplate is not evidence:** Standard contractual language (DPA breach notification, terms of service) is a regulatory floor, not proof of operational capability. Note what would constitute stronger evidence.
4. 
