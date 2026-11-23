# RFO FAR and DFARS HTML

HTML extracts of the **Revolutionary FAR Overhaul (RFO)**: the deviated FAR parts published by GSA and the
DoD class deviations to the DFARS and DFARS PGI. Each file holds one section, clause, or part/subpart
introduction, so the text can be loaded, diffed, and searched section by section.

## Contents

| Directory | Content | Files |
| --- | --- | --- |
| `html/far_overhaul_processed/` | FAR overhaul parts, one file per section/clause | ~2,800 |
| `dfar_html/` | DFARS and PGI deviation text, one file per section/clause, plus each cover memo | ~2,600 |

## Sources

- **FAR**: GSA FAR Part Deviation Guide, <https://www.acquisition.gov/far-overhaul/far-part-deviation-guide>.
  Each part page is scraped article by article (each section's own text, without its nested child sections).
- **DFARS / PGI**: DoD (DPC/DARS) RFO class deviations,
  <https://www.acq.osd.mil/dpap/dars/dfars_far_overhaul_class_deviations.html>. The TAB A deviation memo PDFs,
  including revision reissues (Rev1/Rev2/...), are converted to HTML. Table text comes from the PDF text layer.

## File naming

**FAR** (`html/far_overhaul_processed/`), named after the acquisition.gov article id:
- `FAR_<part>_<section>.html`, e.g. `FAR_9_104_6.html` for 9.104-6.
- `FAR_Part_<n>.html` / `FAR_Subpart_<n>_<m>.html`, only where a part or subpart has text of its own.

**DFARS** (`dfar_html/`):
- `DFARS_<part>_<section>.html`, e.g. `DFARS_252_204-7012.html` for 252.204-7012.
- `DFARS_PGI_<part>_<section>.html` for PGI sections, e.g. `DFARS_PGI_204_201-71.html`.
- `DFARS_<part>[_<subpart>].html` for DFARS part/subpart introductory text, e.g. `DFARS_229_70.html`.
- `DFARS_MEMO_<memo pdf name>.html` for each class-deviation cover memo (SUBJECT through signer).
- A range of reserved sections uses the first number, e.g. `DFARS_225_7005.html` for 225.7005-225.7008 [Reserved].

Each file is a small HTML page whose `<title>` and `<h2>` carry the section number and title, followed by
`<div class="body conbody">` with the text (paragraphs, and tables where the source has them).

## Format notes

- The FAR files keep acquisition.gov's markup for the section body.
- In DFARS 252 clause files, the first paragraph holds the prescription and the clause title with its date
  ("As prescribed in ..., use the following clause: TITLE (MON YYYY)").
- Source quirks are reproduced as printed (for example a mistyped heading number in the PDF).

## Attribution

- FAR: U.S. General Services Administration, <https://www.acquisition.gov/far-overhaul>
- DFARS/PGI: Department of Defense, Defense Pricing, Contracting, and Acquisition Policy,
  <https://www.acq.osd.mil/dpap/dars/>
- Base FAR HTML conventions: <https://github.com/GSA/GSA-Acquisition-FAR>

Regulatory text is a U.S. Government work. Always check the official sources before relying on this text.
