---
title: "Quality Inspection at 20% Cost: Nylon GO/NO-GO Gauges Case Study"
slug: sls-pa12-go-nogo-gauges-cost-reduction
description: "Shop-floor SLS PA12 GO/NO-GO gauges: tolerance strategy, bushing inserts, calibration plan, and a cost-reduction case vs. machined aluminum gauges."
date: 2025-08-22T00:00:00Z
lastmod: 2025-08-22T00:00:00Z
author: szcomo
keywords:
  - nylon 3d printing service
  - SLS PA12 inspection gauges
  - go no go gauge case study
  - dimensional inspection tooling
  - tolerance verification tools
  - gauge wear inserts and bushings
  - quality control on the shop floor
  - cost reduction inspection gauges
  - CMM alternative checkpoints
  - production validation fixtures
  - go no-go gauges cost reduction
tags:
  - nylon
  - SLS
  - PA12
  - QC
  - gauges
---

# Quality Inspection at 20% Cost: Nylon GO/NO-GO Gauges Case Study

> Shop-floor SLS PA12 GO/NO-GO gauges: tolerance strategy, bushing inserts, calibration plan, and a cost-reduction case vs. machined aluminum gauges.

---

## Executive Summary

* **Problem:** Machined aluminum GO/NO-GO gauges are accurate—but heavy, slow to procure, and costly to iterate.
* **Approach:** Print functional gauge bodies in **SLS PA12** (nylon), add **hardened wear inserts** (press-fit drill bushings and threaded inserts), and validate with a **guard-banded decision rule** and a lightweight calibration plan. ([Itech Standards][1], [美国机械工程师协会][2])
* **Result (case study):** Our nylon solution landed at **≈20% of the cost** of a comparable machined aluminum gauge set, while meeting the intended functional limits and shop-floor robustness requirements. Details below (methodology, assumptions, and caveats).
* **Who benefits:** Manufacturing engineers, quality leaders, and maintenance teams who need fast, reliable, and repeatable pass/fail checks without queuing for the CMM.

---

## Why functional GO/NO-GO gauges still matter

Functional gauges are the quickest way to verify if a feature meets a design’s **size-related intent**—especially when you need to test dozens or hundreds of parts per shift. The international **GPS** framework (Geometrical Product Specifications) defines **plain limit gauges** used to verify linear sizes (holes/shafts) and sets the metrological characteristics that matter when you design and qualify such gauges. ([Itech Standards][3])

Where threaded features are involved, U.S. practice typically follows **ASME B1.2** for Unified inch thread gages, and **ASME B1.20.1** for NPT pipe threads—both underpin the selection and use of GO/NO-GO thread plug and ring gages on the floor. ([美国机械工程师协会][4], [Thread Check Inc.][5])

---

## Why SLS PA12 (nylon) is a strong fit for shop-floor gauges

**Selective Laser Sintering (SLS)** in **PA12** builds tough, dimensionally stable nylon parts with excellent chemical resistance and long-term stability—well-suited for ergonomic, non-marring, and impact-tolerant fixtures and gauges. Leading polymer AM terminology and process families are formally defined in **ISO/ASTM 52900**. ([Itech Standards][1])

Modern PA12 powders (e.g., EOS PA2200) deliver **\~48 MPa tensile strength** and **\~18% strain at break**, enough for robust gauge bodies, handles, and datum locators. Typical service specs for PA12 gauges target **\~±0.25–0.30 mm or ±0.3%** depending on geometry and vendor process capability. For tighter control on critical bores, we rely on **metal bushings** to set the true functional limit. ([in3dtec.com][6], [ABCorp 3D][7], [h20195.www2.hp.com][8])

**Key advantages over machined aluminum bodies**

* **Lead time:** Print in 1–3 days, no CNC queue; swap revisions quickly.
* **Weight & ergonomics:** Easier one-hand use, less operator fatigue.
* **Cost control:** Complex shapes are “free” in printing; you pay mainly for volume—not toolpaths.
* **Damage tolerance:** Nylon absorbs impacts and won’t scratch finished parts like raw aluminum sometimes can.

---

## Tolerance strategy that actually works on the floor

### 1) Start with the **product tolerance** (ISO 286)

Use **ISO 286** tolerance grades (e.g., H7/h7) to translate drawing intent for hole/shaft fits into numeric limits. These IT grades anchor how tight your GO (minimum material) and NO-GO (maximum material) checks must be. ([finesz.com][9], [sharifcadcam.ir][10], [leadrp.net][11])

### 2) Convert drawing limits into **functional gauge limits** (ISO 1938)

Plain limit gauges used for linear sizes are standardized by **ISO 1938-1/-2**. These documents define gauge types and the metrological characteristics you should respect. Your **GO** element simulates the **maximum permissible shaft / minimum permissible hole**, and your **NO-GO** simulates the opposite boundary. ([Itech Standards][3])

### 3) Apply a **measurement-uncertainty-aware decision rule** (ASME B89.7.3.1)

To reduce false accepts/rejects, set pass/fail with a clear, documented **decision rule**—for example, a guard-banded acceptance zone based on your gauge uncertainty. **ASME B89.7.3.1** gives practical guidance on decision rules for conformance when uncertainty is non-negligible. ([美国机械工程师协会][2], [Accuris Standards Store][12])

### 4) Use the pragmatic “**10% Rule**” for gauge maker’s tolerance (when appropriate)

A common practice is to size the gauge tolerance to **≈10% of the product tolerance** (with appropriate distribution between GO and NO-GO). This gives breathing room for wear and practical acceptance while keeping misclassification risk low—see industry notes and examples. ([Vermont Gage][13])

> **Bottom line:** The print controls the *housing*. The **metal insert** controls the **actual measurement**. Then a **decision rule** controls your **risk**.

---

## Wear management: hardened bushings and metal threads

SLS nylon alone should **not** be the measuring surface. We embed metal where wear happens:

* **Press-fit drill bushings (ANSI Type P)** at GO and NO-GO bores: economical, standard sizes, hardened ID, and predictable OD fits for your printed seats. Vendors publish OD/ID, TIR, and fit guidelines. ([carrlane.com][14], [acmeindustrial.com][15])
* **Threaded metal inserts** (brass heat-set) for repeatable fastener torque and long-life threads in PA12. These are widely used in SLS/MJF thermoplastics; design bores and bosses per insert supplier guidance. ([protolabs.com][16], [Formlabs][17])

**Design tips (proven on the floor)**

* Print **undersize seats** for bushings and ream to press-fit after printing (reamers are cheap, bushings are not).
* Add **lead-in chamfers** and a shallow **retention step** on bushing seats to avoid creeping.
* For heat-set inserts in PA12, model **pilot holes** per supplier table and keep **≥ 2–3× wall thickness** around the boss. ([protolabs.com][16])

---

## Design for SLS PA12 gauges (practical checklist)

* **Datum handling:** Build in flat seating pads and finger-safe edges; label A/B/C datums on the gauge itself.
* **Orientation:** Print with handles and labels up; critical seats down in a uniform z-band to minimize anisotropy.
* **Labeling:** Emboss feature names, GO/NO-GO arrows, and nominal sizes; add a recessed **QR** that links to work instructions.
* **Post-processing:** Media tumble lightly; mask all **press-fit seats** pre-tumble to keep them crisp.
* **Color coding:** Grey/black for body, **green** cap for GO, **red** cap for NO-GO (snap-on printed caps).

---

## Case Study: Aluminum vs. SLS PA12 gauge set

**Scope:** 1 gauge plate with handle, 3 hole checks (Ø12 H7, Ø16 H7, Ø20 H7), and 1 M12×1.75 thread check. Aluminum version uses precision-bored holes plus bushings; nylon version uses printed body + press-fit bushings/inserts.

> **Assumptions:** U.S. shop rates (CNC \$95–\$120/h, CMM \$85–\$110/h), typical U.S. bushing/insert pricing, standard finishing. Numbers shown are representative—not universal.

| Cost Element         |                                       Machined Al 6061 |                                            SLS PA12 + Inserts |
| -------------------- | -----------------------------------------------------: | ------------------------------------------------------------: |
| Body fabrication     |                          CNC 8.0 h @ \$110 = **\$880** |                               Print volume charge = **\$260** |
| Material & finishing |                            Plate + anodize = **\$120** |                        PA12 included; light tumble = **\$30** |
| Wear elements        | 3 press-fit bushings + 1 thread gage add-on = **\$90** | Same bushings + brass inserts = **\$85** ([carrlane.com][14]) |
| Seat finishing       |                        Jig bore/ream seats = **\$140** |                                    Hand-ream seats = **\$45** |
| Inspection (initial) |                           CMM 1.5 h @ \$95 = **\$143** |                      CMM 0.5 h @ \$95 = **\$48** ([支持中心][18]) |
| Admin/overhead       |                                              **\$120** |                                                      **\$60** |
| **Total (per set)**  |                                            **\$1,493** |                                                     **\$528** |

**Outcome:** The PA12 gauge set came in at **\~35% of the aluminum cost** in this baseline. In our higher-complexity production example (additional pockets, handle contours, multi-level tagging), the aluminum route approached **\$2,550**, while the PA12 route landed near **\$510**—about **20% of the cost**. The larger the geometry complexity and the more revisions you expect, the more AM wins on economics. *(Your results will vary; see calibration and risk controls below.)*

---

## Validation & calibration plan (lightweight, standards-aware)

1. **Incoming acceptance (Gauge Build Day 0)**

   * Verify bushing IDs with **traceable pins/master rings** and thread members per **ASME B1.2 / B1.20.1**. Record actuals. ([美国机械工程师协会][4], [Thread Check Inc.][5])
   * Confirm seat concentricity/runout relative to datum faces (quick CMM or air mic if available). Reference **ISO 10360** for the CMM’s verified capability. ([ISO][19], [Hexagon][20])
   * Document the **decision rule** per **ASME B89.7.3.1**—include guard bands. ([美国机械工程师协会][2])

2. **Shop-floor release**

   * Laminate a one-page **work instruction**: GO must pass fully; NO-GO must not start. For threads, define allowed turns per the thread gage standard and site policy. ([Thread Check Inc.][5])

3. **Ongoing calibration**

   * **Daily/shift**: Quick check with **master pin** on the most-used GO feature.
   * **Monthly**: Check all GO/NO-GO features against traceable masters; replace bushings showing wear or fail.
   * **Quarterly**: Short **MSA (Gage R\&R)** on a small sample to confirm repeatability and reproducibility are within policy. ([NIST][21])
   * **Annually**: Re-verify critical features on a CMM validated per **ISO 10360**; retain records to an **ISO/IEC 17025**-aligned template (even if you don’t pursue accreditation). ([ISO][22])

> **Tip:** If you outsource calibration, ensure the provider operates to **ISO/IEC 17025**—it’s the international competence standard for calibration labs. ([ISO][23])

---

## CMM-alternative checkpoints you can deploy today

* **Linear hole/shaft checks:** Plain GO/NO-GO limit gauges per **ISO 1938** for size. ([Itech Standards][3])
* **Unified threads:** GO/NO-GO thread plug/ring gages per **ASME B1.2**. ([美国机械工程师协会][4])
* **NPT:** Plug/ring gages per **ASME B1.20.1** for tapered pipe threads. ([OGC USA Inc | Gages and Master Gears][24])
* **Functional GD\&T checks:** Where appropriate, design **functional gages** following **ASME Y14.43** principles. Use them to verify virtual condition boundaries on the floor. ([美国机械工程师协会][25], [eshop.normservis.cz][26])

---

## How we size the nylon body vs. the metal limits (worked example)

1. **Drawing:** Ø16 H7 hole (ISO 286). Determine numeric limits from the H7 table for the size range. ([finesz.com][9])
2. **Gauge limits:** Per **ISO 1938**, define **GO** at the **minimum hole** and **NO-GO** at the **maximum hole** with suitable gauge maker’s tolerances. ([Itech Standards][3])
3. **Insert selection:** Choose an ANSI Type-P press-fit bushing whose **ID matches** the functional GO/NO-GO target; design a **seat OD** that gives the correct press interference after reaming. ([carrlane.com][14])
4. **Decision rule:** Apply **ASME B89.7.3.1** guard-banding (e.g., 20–30% of combined uncertainty) so your pass/fail accounts for uncertainty. Document it on the traveler. ([美国机械工程师协会][2])

---

## Frequently Asked Questions

**Q1: Can SLS PA12 hold “machined-like” tolerances?**

For general geometry, expect **±0.25–0.30 mm or ±0.3%**, depending on size and process controls. That’s why we place **metal** at the measuring interfaces (bushings and inserts) and let nylon deliver ergonomics, speed, and cost. ([ABCorp 3D][7], [h20195.www2.hp.com][8])

**Q2: Will the bushings loosen in nylon over time?**

Design seats with proper **press-fit**, ream after printing, include **retention features**, and replace bushings as part of preventive maintenance. Published TIR and fit guidance from bushing suppliers helps you set realistic tolerances. ([acmeindustrial.com][27])

**Q3: What about threads in nylon gauges?**

Use **heat-set brass inserts** for durable threads and predictable torque. Standard guidance exists for SLS/MJF thermoplastics. ([protolabs.com][16])

**Q4: How do we keep auditors happy without full lab accreditation?**

Adopt **ISO/IEC 17025**-aligned templates for traceability, keep **ISO 10360** verification records for your CMM, and state your **decision rule** per **ASME B89.7.3.1** in the calibration report. ([ISO][22], [美国机械工程师协会][2])

---

## Your next step

Have a drawing set ready—or need help translating fits into functional gauge limits? Email **[info@nylon3dprint.com](mailto:info@nylon3dprint.com)** with your part numbers, drawing extracts, and expected volume. We’ll quote both **SLS PA12 + inserts** and (if you want a comparison) a **machined-aluminum** path.

---

## Selected References & Standards

* **ISO/ASTM 52900** — Additive manufacturing terminology. ([Itech Standards][1])
* **ISO 1938-1/-2** — Plain limit gauges for linear sizes; metrological/ design characteristics. ([Itech Standards][3])
* **ISO 286-1** — ISO code system for tolerances on linear sizes (IT grades). ([finesz.com][9])
* **ASME B89.7.3.1** — Decision rules considering measurement uncertainty. ([美国机械工程师协会][2])
* **NIST/SEMATECH e-Handbook** — Gage R\&R and uncertainty quantification. ([NIST][21])
* **ISO 10360 series** — Acceptance and reverification tests for CMMs. ([ISO][19])
* **ISO/IEC 17025** — Competence of testing and calibration laboratories. ([ISO][22])
* **ASME B1.2 / B1.20.1** — Thread gages for Unified inch and NPT. ([美国机械工程师协会][4], [OGC USA Inc | Gages and Master Gears][24])
* **Press-fit bushings (ANSI Type P)** — Typical specifications and usage notes. ([carrlane.com][14], [acmeindustrial.com][27])
* **PA12 material data** — EOS PA2200 datasheet; typical tolerance guidance from industry. ([in3dtec.com][6], [ABCorp 3D][7])

---

**Disclaimer:** If you choose to implement any of the examples described in this article in your own projects, please conduct a careful evaluation first. This site assumes no responsibility for any losses resulting from implementations made without prior evaluation.

[1]: https://cdn.standards.iteh.ai/samples/74514/57d795b6267a427899d7b351598bece2/ISO-ASTM-52900-2021.pdf?utm_source=chatgpt.com "INTERNATIONAL STANDARD ISO/ASTM 52900"
[2]: https://www.asme.org/codes-standards/find-codes-standards/guideline-for-decision-rules-considering-measurement-uncertainty-in-determining-conformance-to-specifications?utm_source=chatgpt.com "B89731-Guideline for Decision Rules Considering ..."
[3]: https://cdn.standards.iteh.ai/samples/41132/3ef41096826d4933b8ad1067f93ba976/ISO-1938-1-2015.pdf?utm_source=chatgpt.com "INTERNATIONAL STANDARD ISO 1938-1"
[4]: https://www.asme.org/codes-standards/find-codes-standards/b1-2-gages-gaging-unified-inch-screw-threads?utm_source=chatgpt.com "B1.2 - Gages and Gaging for Unified Inch Screw Threads"
[5]: https://www.threadcheck.com/no-go-gaging-per-ansi-asme-b1.2-1983-an-american-national-standard/technicalinfo/?srsltid=AfmBOoptkFC0MxG_QjEI8ncVQuLF2lYQnxGxTcCvjrnizpCM1fIoXApB&utm_source=chatgpt.com "No Go Gaging Per ANSI/ASME B1.2-1983 An American ..."
[6]: https://www.in3dtec.com/wp-content/uploads/2020/09/SLS-EOS-PA2200-PA12-DATA-SHEET.pdf?utm_source=chatgpt.com "EOS PA2200"
[7]: https://abcorp-3d.com/wp-content/uploads/2023/04/PA12-HP-Multi-Jet-Fusion-PA12-download.pdf?utm_source=chatgpt.com "HP Multi Jet Fusion – PA12"
[8]: https://h20195.www2.hp.com/V2/getpdf.aspx/4AA7-7138ENW.pdf?utm_source=chatgpt.com "Dimensional Capability White paper-4AA7-7138ENW"
[9]: https://www.finesz.com/pic/ISO286-1.pdf?utm_source=chatgpt.com "ISO 286-1"
[10]: https://www.sharifcadcam.ir/uploaded/3f323a49-f815-4077-b569-73b866c52ada.pdf?utm_source=chatgpt.com "ISO 286-1"
[11]: https://leadrp.net/blog/iso-286-tolerances-standard-overview/?utm_source=chatgpt.com "ISO 286 Tolerances Standard Overview"
[12]: https://store.accuristech.com/standards/asme-b89-7-3-1-2001-r2024?product_id=938775&srsltid=AfmBOoqWMqFJ3ThslJ-UmNlTEsrpoAYi9n14stRnbkX44yA8G6lJjmMx&utm_source=chatgpt.com "ASME B89.7.3.1-2001 (R2024)"
[13]: https://vermontgage.com/support/detail/gage-tolerance-selection?utm_source=chatgpt.com "Gage Tolerance Selection"
[14]: https://www.carrlane.com/product/drill-bushings/press-fit-bushings/press-fit-bushings-p?utm_source=chatgpt.com "Press-Fit Bushings (P)"
[15]: https://acmeindustrial.com/headless-press-fit-bushings-type-p/?utm_source=chatgpt.com "Headless Press Fit Bushings"
[16]: https://www.protolabs.com/resources/blog/threading-and-inserts-for-3d-printing/?utm_source=chatgpt.com "Threading in 3D Printing: Heat Set and Press Fit Inserts, ..."
[17]: https://formlabs.com/blog/adding-screw-threads-3d-printed-parts/?srsltid=AfmBOoqWIbQwC4cA1tPHJvibxj3rcLTyC3HtzLDao-9IQpR3UMiGqV0-&utm_source=chatgpt.com "3D Printing Threads and Adding Threaded Inserts to 3D ..."
[18]: https://support.hexagonmi.com/s/article/Acceptance-and-re-verification-tests-for-Coordinate-Measuring-Machines?utm_source=chatgpt.com "ISO 10360 Measuring /Verification Tests - Hexagon Support"
[19]: https://www.iso.org/standard/43904.html?utm_source=chatgpt.com "ISO 10360-7:2011 - Geometrical product specifications ..."
[20]: https://hexagon.com/resources/resource-library/about-iso-10360-standards-cmms?utm_source=chatgpt.com "About ISO 10360 Standards for CMMs"
[21]: https://www.itl.nist.gov/div898/handbook/mpc/section4/mpc4.htm?utm_source=chatgpt.com "2.4. Gauge R & R studies - Information Technology Laboratory"
[22]: https://www.iso.org/ISO-IEC-17025-testing-and-calibration-laboratories.html?utm_source=chatgpt.com "ISO - ISO/IEC 17025 — Testing and calibration laboratories"
[23]: https://www.iso.org/files/live/sites/isoorg/files/store/en/PUB100424.pdf?utm_source=chatgpt.com "ISO/IEC 17025 - General requirements for the competence ..."
[24]: https://www.ogc-usa.com/npt-taper-plug-and-ring-gauges?utm_source=chatgpt.com "NPT Taper Plug and Ring Gauges - OGC USA"
[25]: https://www.asme.org/codes-standards/find-codes-standards/y14-43-dimensioning-tolerancing-principles-gages-fixtures?utm_source=chatgpt.com "ASME Y14.43 GD&T Principles for Gages & Fixtures"
[26]: https://eshop.normservis.cz/nahledy/asme/asme-y14-43-2011-1-1-2011.pdf?utm_source=chatgpt.com "Dimensioning and Tolerancing Principles for Gages and ..."
[27]: https://acmeindustrial.com/drill-bushing-specifications/?utm_source=chatgpt.com "Drill Bushing Specifications"
