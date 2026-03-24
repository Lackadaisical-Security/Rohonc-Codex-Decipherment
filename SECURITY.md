# SECURITY

## Scope

This is a research archive. There is no running service, no login system, no user data. The attack surface is the data itself and the toolkit scripts.

Security issues relevant to this repo fall into two categories:

1. **Data integrity issues** — corrupted, tampered, or injected content in lexicon files, research logs, or toolkit outputs
2. **Code vulnerabilities** — exploitable bugs in the Rohonc Toolkit scripts (Python decoder, frequency analyzer, etc.)

---

## Reporting a Vulnerability

**Do not open a public issue for security vulnerabilities.**

Report privately:

- **Email:** lackadaisicalresearch@pm.me
- **XMPP+OTR:** thelackadaisicalone@xmpp.jp (preferred for sensitive disclosures)

Include in your report:

- What the issue is, stated plainly
- Which file(s) or script(s) are affected
- Steps to reproduce or trigger the problem
- What you believe the impact is
- If you have a proposed fix, include it

---

## What Happens After You Report

1. Acknowledgement within 7 days if we agree it's a valid issue
2. Assessment of severity and scope
3. Fix developed and tested
4. Fix released with a note in the relevant changelog
5. Credit given to the reporter unless anonymity is requested

No bug bounties. No CVE filings (this is not a product). No coordinated disclosure theater.

If it's real and it matters, it gets fixed. That's the deal.

---

## Data Integrity

The lexicon files and research logs are the primary research outputs. Tampering with these is the highest-severity issue in this repo.

If you find evidence of:
- Unexpected modifications to JSON lexicon files
- Injected or altered content in research phase logs
- Hash mismatches in toolkit outputs

Report it immediately using the contact channels above.

---

## Toolkit Code (rohonc_toolkit.zip)

The toolkit scripts process local files only — no network calls, no external API dependencies, no credential handling. Risk surface is limited to:

- **Path traversal** in file input arguments
- **Malformed input** causing unexpected behavior in the decoder or frequency analyzer
- **Dependency vulnerabilities** in any Python packages used

If you find any of these, report as above. Patches welcome via [CONTRIBUTING.md](CONTRIBUTING.md).

---

## What We Don't Consider a Security Issue

- Disagreements with the decipherment methodology
- Theoretical challenges to the linguistic conclusions
- Criticism of the research approach

Those belong in issues or discussions, not security reports.

---

## Responsible Disclosure

We run a tight operation. If you find something real:

- Give us reasonable time to fix it before going public
- Don't use the vulnerability to access, modify, or distribute data you shouldn't have
- Don't burn the repo just to make a point

In exchange: we'll fix it, credit you, and not waste your time with lawyers.

Fair trade.

---

*"Find it. Report it. Fix it. That's the whole process."*

**Lackadaisical Security - Linguistics Division**
- **Website:** [https://lackadaisical-security.com](https://lackadaisical-security.com)
- **Email:** lackadaisicalresearch@pm.me
