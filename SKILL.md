---
name: uk-legal-mcp-skill
description: Official United Kingdom (UK) legislation, multi-tier court precedent research, and citation verification skill.
version: 2.0.0
author: JurisAtlas
license: MIT
---

# United Kingdom Legal Research & Multi-Tier Case Law Skill (`uk-legal-mcp`)

Use this skill whenever the user asks a legal question, drafts a pleading or contract, or researches case law across any judicial instance in **United Kingdom (UK)**.

## Verification & Research Rules

1. **Citation Verification:** Never fabricate a statutory provision or case citation. Query `search_legislation`, `search_case_law`, `search_tiered_court_decisions`, or `verify_citation` before citing any authority (e.g., `[2024] UKSC 12 or UKPGA 2018/12`).
2. **Multi-Tier Judicial Coverage:**
   - **First Instance (Trial / Municipal / District):** County Court, Crown Court, High Court of Justice (EWHC — King's Bench, Chancery, Family, Commercial, Administrative) & First-tier Tribunals (FTT)
   - **Second Instance (Cantonal / Regional / Appellate):** Court of Appeal of England & Wales (EWCA Civil & Criminal Divisions), Inner House of the Court of Session (Scotland), Court of Appeal in Northern Ireland & Upper Tribunals (UKUT / EAT)
   - **Supreme & Constitutional Instance:** United Kingdom Supreme Court (UKSC) & Judicial Committee of the Privy Council (JCPC)
   - **Primary Tiered Database:** The National Archives Find Case Law (caselaw.nationalarchives.gov.uk) & BAILII (`https://caselaw.nationalarchives.gov.uk`)
