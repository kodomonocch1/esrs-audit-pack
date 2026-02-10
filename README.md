### ESRS Audit Pack — Public Demo (No Source Code)

[![Release](https://img.shields.io/github/v/release/kodomonocch1/esrs-audit-pack)](https://github.com/kodomonocch1/esrs-audit-pack/releases)
[![Discussions](https://img.shields.io/github/discussions/kodomonocch1/esrs-audit-pack?label=Q%26A%20%2F%20Repro)](https://github.com/kodomonocch1/esrs-audit-pack/discussions/categories/q-a)

**Download a demo ZIP → open the generated ESRS-style report (DOCX/PDF) → verify proof logs (sanitized).**

This repository intentionally ships **no implementation source code**.  
Instead, it ships **generated artifacts + sanitized proof logs + integrity hashes** so evaluators can review outcomes safely.

<p>
  <a href="https://github.com/kodomonocch1/esrs-audit-pack/releases/tag/v0.1.0"><b>① Download (Release v0.1.0)</b></a>
  &nbsp;•&nbsp;
  <a href="#quick-start"><b>② Quick start</b></a>
  &nbsp;•&nbsp;
  <a href="#proof--logs"><b>③ Proof & Logs</b></a>
  &nbsp;•&nbsp;
  <a href="#preview"><b>④ Report preview</b></a>
  &nbsp;•&nbsp;
  <a href="#contact"><b>⑤ Contact</b></a>
</p>

---

## What’s in the Release ZIP

The Release asset contains a folder like:

- `outputs/`
  - `report_draft.docx` (generated)
  - `report_draft.pdf`  (generated)
- `logs/`
  - `last_computed.json` (single source of truth: inputs → computed → coverage)
  - `legal_manifest.json` (legal kit manifest)
  - `legal_quality_proof.public.json` (legal checks result; paths sanitized)
  - `esrs_anchor_injection_stats.public.json` (DOCX anchor injection stats; paths sanitized)
- `evidence/`
  - `proof.zip`
  - `audit.zip`
- `SHA256SUMS.txt` (integrity)
- `README_FIRST.txt` (bundle instructions)

---

## Quick start <a id="quick-start"></a>

### 1) Download the demo bundle
Release v0.1.0 (Assets):  
https://github.com/kodomonocch1/esrs-audit-pack/releases/tag/v0.1.0

Download the **Asset ZIP** (not “Source code (zip/tar.gz)”).

### 2) Unzip and open outputs
- Open: `outputs/report_draft.docx`
- Open: `outputs/report_draft.pdf`

### 3) Verify integrity (optional)
In PowerShell (inside the unzipped demo folder):

```powershell
Get-Content .\SHA256SUMS.txt
Get-FileHash -Algorithm SHA256 .\outputs\report_draft.docx
Get-FileHash -Algorithm SHA256 .\outputs\report_draft.pdf
````

---

## Proof & Logs <a id="proof--logs"></a>

This demo includes **sanitized logs** to show the outputs came from a **DOCX-based pipeline**:

* `logs/esrs_anchor_injection_stats.public.json`
  Counts of anchor injections / heading normalization / cleanup stats.
* `logs/last_computed.json`
  Canonical runtime snapshot: computed values + ESRS coverage (“single source of truth”).
* `logs/legal_quality_proof.public.json`
  Legal-kit checklist results (paths sanitized; safe to publish).

Privacy note:

* Public logs remove local absolute paths (e.g., `C:\Users\...`).
* If you need deeper evaluation, contact via LinkedIn or X (NDA policy TBD).

---

## Contact <a id="contact"></a>

For questions / evaluation requests:

* GitHub Discussions (Q&A / Repro):
  [https://github.com/kodomonocch1/esrs-audit-pack/discussions/categories/q-a](https://github.com/kodomonocch1/esrs-audit-pack/discussions/categories/q-a)
* LinkedIn:
  [https://www.linkedin.com/in/tetsuro-kawamoto-114907388/](https://www.linkedin.com/in/tetsuro-kawamoto-114907388/)
* X (Twitter):
  [https://x.com/kamikakusi0001](https://x.com/kamikakusi0001)
  
---

## Report preview <a id="preview"></a>

Below are screenshots from the generated report (DOCX/PDF).
(Displayed in a stable 2-column grid for readability.)

<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/5e697bd3-9297-40fb-a764-d2cab53a4188" width="420" /></td>
    <td><img src="https://github.com/user-attachments/assets/d268de51-7d29-4f95-88e0-f3f561060010" width="420" /></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/b3112783-e2c2-410b-9f44-e45a5f0973ca" width="420" /></td>
    <td><img src="https://github.com/user-attachments/assets/2b24a8f0-83d8-4dd4-b6ee-6bb15ffd3c92" width="420" /></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/aac9ec79-6b44-43cd-ae60-50af2cd69827" width="420" /></td>
    <td><img src="https://github.com/user-attachments/assets/a783e785-206d-4899-b3d6-c25cae3ffc8c" width="420" /></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/3e585faf-f559-4aa2-a3cf-3403f0fc8b6b" width="420" /></td>
    <td><img src="https://github.com/user-attachments/assets/b4c4bfcc-bf41-4836-90b8-8997be8517bf" width="420" /></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/e94ab06c-ec97-4cb4-970f-fa1251c356ef" width="420" /></td>
    <td><img src="https://github.com/user-attachments/assets/f799f491-56ed-4117-8889-c6f57f2fe8a5" width="420" /></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/896b0c74-3920-49e4-8917-55791eb37ee5" width="420" /></td>
    <td></td>
  </tr>
</table>

---

Please do not send confidential information in public channels.
