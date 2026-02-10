# Independent Verification Protocol

This document outlines how to replicate the core immune priming and anti-tumor effect observed in the NOVA-TIRA pilot studies.

## Part 1: In Vitro Immune Priming Assay

### Materials Needed
- Bone marrow-derived dendritic cells (BMDCs) from C57BL/6 mice.
- Engineered viral vector (specifications in `protocols/verification_protocol.md` – you must construct this per the outlined sequence backbone; the active template insert is *not* provided).
- Naïve T-cells from OT-I/Rag-/- mice (as a reporter system).
- Standard cell culture reagents (RPMI-1640, FBS, cytokines GM-CSF, IL-4).

### Method
1.  Differentiate BMDCs over 7 days with GM-CSF + IL-4.
2.  On day 7, incubate BMDCs with the engineered vector (MOI 10) for 24h. Include controls (no vector, empty vector).
3.  Co-culture primed BMDCs with naïve OT-I T-cells at a 1:10 ratio (DC:T-cell).
4.  At 72h, collect supernatant for IFN-γ ELISA and analyze T-cells by flow cytometry for CD69/CD25 activation markers.

### Expected Outcome
Vector + template-treated BMDCs should induce significantly higher T-cell activation (>50% CD69+) and IFN-γ secretion compared to empty vector controls. This confirms the dendritic cell priming capacity.

## Part 2: In Vivo Anti-Tumor Activity (Murine Model)

### Model
- Subcutaneous MC38 colon carcinoma or B16-F10 melanoma in C57BL/6 mice (n=8/group).
- Groups: 1) PBS control, 2) Empty vector control, 3) TIRA vector.

### Dosing
- Single intratumoral injection (5e8 vp) when tumors reach ~50 mm³.
- Measure tumor volume with calipers every 2-3 days.
- Harvest tumors and draining lymph nodes at endpoint (day 21) for flow cytometry.

### Analysis
1.  **Tumor Growth:** The TIRA group should show significant growth inhibition (>70% vs. PBS) starting around day 10-12.
2.  **Immune Infiltration:** Flow cytometry of digested tumors should show a >3-fold increase in tumor-infiltrating CD8+ T-cells and a higher ratio of CD8+/Treg cells in the TIRA group.
3.  **Memory:** Survivors from the TIRA group should reject a re-challenge of the same tumor line at 60 days.

All protocols for tumor digestion, antibody panels, and gating strategies are in `/protocols`.

## Notes on Replication

The effect size depends on the model. MC38 is more immunogenic and shows a stronger response. The key is observing the *shift* in the immune profile and the correlated growth delay. The exact magnitude may vary by lab.

The data in `/data` is provided as a reference benchmark.
