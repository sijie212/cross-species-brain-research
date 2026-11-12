# Cross-Species Brain Anatomy, Function, and Brain Distribution–Toxicity Correlation: A Comprehensive Research Report

> **Audience:** Medicinal chemists / drug-discovery scientists working in preclinical safety
> **Language:** English (translated from the Chinese original, 2026-11-12)
> **Date:** 2026-11-12 (search date; regulations and guidelines are cited as of their original publication/revision dates — verify the current versions before submission)
> **Evidence grades:** ■ **Established** — regulatory guidelines, textbook-level consensus, or agreement across multiple independent sources; ◐ **Emerging** — published but with limited sample size/validation, methodology still evolving, or no regulatory conclusion yet; ○ **Unverified / Hypothesis** — single source, speculation, or extrapolation, **not to be used as the sole basis for decisions**. Any number without a cited source has **not been used** in this report; wherever "approximately/estimated" is written, the quality of its source is noted in the text.

---

## Summary (read these 5 points first)

1. **Establish the "unbound drug" before discussing "brain distribution."** The total brain-to-plasma ratio `Kp,brain = Cbrain,total / Cplasma,total` is severely distorted by plasma protein binding and nonspecific brain tissue binding. The core parameter in modern CNS DMPK is the **unbound brain-to-plasma partition coefficient Kp,uu,brain = Cu,brain / Cu,plasma = Kp,brain × fu,brain / fu,plasma**.■ At steady state, Kp,uu ≈ 1 suggests predominantly passive-diffusion equilibrium; <1 suggests net efflux (P-gp/BCRP, etc.); >1 suggests net uptake / active influx. Cerebral microdialysis is the gold standard for measuring unbound drug concentrations in brain extracellular fluid; the Combinatory Mapping Approach (CMA) — brain homogenate + equilibrium dialysis (fu,brain) combined with the brain slice method (Vu,brain) — is a high-throughput alternative, but for strongly basic compounds (lysosomal accumulation) the homogenate method overestimates fu,brain.■
2. **The brain is not a homogeneous organ: how you sample determines what questions you can answer.** In routine toxicology, brain sampling is a **3-coronal-section screen (optic chiasm, posterior hypothalamus/hippocampus, midbrain–cerebellum–medulla)**; dedicated neurotoxicity studies use **6–7 coronal sections (bilateral in rodents; 6–7 hemisections in non-rodents)** (STP, Bolon et al., 2013).■ Fresh-frozen tissue is used for LC-MS/MS, mass spectrometry imaging (MSI), and omics; perfusion-fixed tissue is used for histopathology. **The same brain from the same animal cannot be optimized for all endpoints at once** — hemispheres/sections/animal subgroups must be pre-allocated in the study design, or it cannot be fixed afterward.
3. **Regional homology cannot be taken for granted, especially for the prefrontal cortex and olfactory system.** The basic brain regional plan (cortex, striatum, hippocampus, thalamus, hypothalamus, amygdala, cerebellum, brainstem) is conserved across rodents, dogs, pigs, non-human primates (NHP), and humans, but the **primate granular dorsolateral prefrontal cortex (granular dlPFC) has no clear homologue in the rat** (Preuss, 1995)■; a 2025 hypothesis proposes that the rodent medial prefrontal cortex contains both streams (prelimbic ≈ dlPFC, infralimbic ≈ vmPFC)◐, **with no consensus yet**. Olfactory bulb as a percentage of brain volume: dog 0.31%, human 0.01% (formalin-fixed specimens, Kavoi & Jameela, 2011)■ — rodent/dog data on the olfactory pathway must be discounted when extrapolating to humans.
4. **"Distribution explains toxicity" requires three-way alignment: same region, same time, same (unbound) concentration.** "High whole-brain concentration + lesions present" alone is not enough. A valid correlation evidence chain is: regional unbound concentration (LC-MS/MS by region / microdialysis / quantitative MSI) → regional lesion incidence and severity (same anatomical level, blinded/semi-quantitative scoring) → dose–response and time–response consistency → temporal changes in mechanistic markers (GFAP/Iba1/Fluoro-Jade, NfL, etc.) in the same region. MPTP (nigrostriatal) and BMAA (hippocampal CA1) are two textbook cases, see §5.■
5. **The most common failures are not scientific problems but sampling and documentation problems:** failure to perfuse / correct for residual blood leads to overestimation of low Kp; post-mortem delay causes metabolite/protein degradation; fixatives and paraffin interfere with mass spectrometry; anesthesia and euthanasia methods alter blood flow and BBB permeability; strain, sex, and age not stratified. See the pitfalls checklist in §6.

---

## 1. Cross-Species Brain Anatomy and Dissection

### 1.1 Conserved vs species-specific: first build a "homology" mental model

All mammals share the same basic plan: telencephalon (neocortex, striatum, hippocampus, amygdala, olfactory bulb), diencephalon (thalamus, hypothalamus), midbrain, hindbrain (cerebellum, pons, medulla).■ Differences lie mainly in **proportions, degree of differentiation, and gyrification**, not in whether a major region exists:

| Structure / Feature | Mouse / Rat | Rabbit | Dog (Beagle) | NHP (cynomolgus / rhesus) | Göttingen Minipig | Human |
|---|---|---|---|---|---|---|
| Gyrification | Lissencephalic | Lissencephalic | Gyrencephalic | Gyrencephalic | Gyrencephalic, brain ~6×5×4 cm ◐ | Gyrencephalic, highly differentiated |
| Neocortical differentiation | Poorly differentiated; granular layer IV underdeveloped | Poorly differentiated | Moderate | Highly differentiated, with granular dlPFC | Moderate; frontal lobe has BA25 (subgenual) and other homologous areas ◐ | Highest; prefrontal cortex occupies the largest proportion of cortex |
| Prefrontal homology | **No granular dlPFC homologue** (Preuss 1995)■; new hypothesis prelimbic≈dlPFC / infralimbic≈vmPFC ◐, no consensus | Similar to rodents; limited data ○ | Has frontal lobe but weak dlPFC homology ○ | **Closest to human**; has granular prefrontal cortex | Has medial prefrontal–nucleus accumbens circuitry ◐ | Reference standard |
| Olfactory bulb | Relatively large, olfaction-dominant | Relatively large | **Large**: olfactory bulb 0.31% of brain volume (human 0.01%)■; olfactory bulb + tract + stria combined: dog 1.95% vs human 0.03% ■ | Relatively small, olfaction regressed | Large (pigs have a well-developed sense of smell; specific percentage figures from web sources lack a primary source, ○ not used) | Smallest, 0.01% ■ |
| Cerebellum | Relatively small, structurally conserved | Conserved | Well developed, motor coordination | Well developed | Well developed | Largest in both absolute and relative terms, with cognitive functions as well ◐ |
| Circumventricular organs (CVOs) | Present in all, all lack a typical BBB (see §4.1)■ | Same as left | Same as left | Same as left | Same as left | Same as left |
| Status as routine toxicology species | **First-choice rodent** (TG 424/426 designed around the rat)■ | Commonly used for reproductive/developmental toxicity and local tolerance; not the first choice for neurotoxicity | **Common non-rodent** (ICH S4 chronic toxicity)■ | **Common non-rodent**, CNS translation closest to human, but limited by cost/ethics/numbers | **Rising non-rodent alternative** (RETHINK project)◐ | — (clinical / post-mortem specimens / imaging) |

**Implications for medicinal chemists:**
- When the target is in the dlPFC (e.g. executive function, working memory), **positive/negative rat behavioral data cannot be translated directly**; NHP or human-derived in vitro/imaging data are needed to support it.■
- For the olfactory bulb, nose-to-brain delivery, or inhalation exposure, high olfactory bulb exposure in rodents/dogs **does not imply high human brain exposure**.■
- Evolutionarily ancient structures such as the cerebellum, brainstem, hippocampus, and striatum are highly conserved across species, making them relatively reliable regions for extrapolating regional toxicity.■

### 1.2 Standard brain atlases — look up by species; do not mix coordinate systems

| Species | Preferred atlas / resource | Key facts (verified) | Notes |
|---|---|---|---|
| Rat | **Paxinos & Watson, *The Rat Brain in Stereotaxic Coordinates*** (7th ed.) | First edition 1982; flat-skull position with bregma/lambda as reference; coronal/sagittal/horizontal sections ■ | One of the most cited atlases in neuroscience; the coordinate reference for stereotaxic surgery, injections, and electrophysiology. Coordinates must be corrected for strain/body weight/age — **coordinates are not universal constants**. |
| Mouse | **Paxinos & Franklin, *The Mouse Brain in Stereotaxic Coordinates***, 5th ed. (Elsevier, 2022-11-09) | 100 revised coronal plates + photographs, ~120 µm spacing; 32 sagittal, 30 horizontal; >800 structures identified ■ | Mainly C57BL/6J; brain size differs in transgenic/other strains. |
| Rhesus | **Paxinos et al., *The Rhesus Monkey Brain in Stereotaxic Coordinates***, 4th ed. (2023) | 141 revised coronal plates + color photographs, ~120 µm spacing; same nomenclature as the mouse, rat, marmoset, and human atlases ■ | Also Saleem & Logothetis (2007, MRI + histology), Martin & Bowden (1996), etc. |
| Cynomolgus | **MNI macaque MRI template** (McGill) + conversion from the Paxinos rhesus atlas | The MNI macaque template is an average of MRI from 25 normal adult monkeys (18 cynomolgus + 7 rhesus); provides a linear transformation to Paxinos coordinates ■ | Fewer cynomolgus-specific cytoarchitectonic atlases than for rhesus; **do not apply rhesus coordinates directly to cynomolgus without MRI registration** ◐. Open-source templates on the PRIME-RE platform (D99, NMT, SARM, CHARM, etc.) ◐. |
| Minipig | **CENSE (Aarhus University) Göttingen minipig brain atlas** (histology + MRI)◐; STP minipig nervous system sampling guidance | Brain of a 1-year-old formalin-perfused specimen ~55×47×36 mm, ~69 g (**single-study figure** ◐); brain ~6×5×4 cm, gyrencephalic ◐ | No Paxinos-style "gold standard" stereotaxic atlas; DBS/imaging studies mostly use individual MRI guidance. |
| Dog / Rabbit | No single Paxinos-style authoritative atlas; use species monographs, MRI templates, and the STP non-rodent sampling guidance | STP has established separate nervous system sampling protocols for rabbit, dog, NHP, and minipig (see §1.3)■; dog brains vary greatly between breeds (body size/head shape)■ | **Gap:** This report found no widely cited primary source for a stereotaxic coordinate atlas for rabbit/dog — for stereotaxic dosing, use individual MRI/anatomical landmarks and state this in the protocol.○ |
| Human | **Paxinos et al., *Atlas of the Human Brain***; **Allen Human Brain Atlas** (gene expression + anatomy); BrainSpan (development) | The Allen Mouse Brain Atlas covers >21,000 genes (ISH, cellular resolution); the Allen Human Brain Atlas is a multi-brain, multi-modal "whole-gene–whole-structure" microarray survey ■ | Human atlases are used for reverse translation: first localize target/pathway expression in the human atlas, then map back to the animal homologue. |

**Stereotaxic key points:** The coordinate system takes bregma (the junction of the coronal and sagittal sutures) as the origin, with three axes: AP (anteroposterior), ML (mediolateral), DV (dorsoventral).■ Species, strain, sex, age, body weight, and skull fixation method (flat skull vs skull horizontal) all shift the relative position of bregma to the target nucleus. **Before reusing coordinates across studies, they must be validated in your own laboratory's animals with dye/tracer** — this is routine practice, not an optional step.◐ (Consensus practice; no regulatory text specifying the number of validation animals was found, so this is marked as practical consensus.)

**Digital atlases / open resources:** Allen Brain Map (mouse.brain-map.org / human.brain-map.org), PRIME-RE macaque templates, MNI macaque template.■ These resources are suitable for regional annotation and cross-species gene-expression comparison, but **cannot replace histological sampling records in GLP studies**.

### 1.3 Standard sampling and trimming protocols

#### (a) Routine general toxicity studies (General toxicity, Tier 1 screen)

The **STP Position Paper, Bolon et al., *Toxicol Pathol* 2013;41:1028–1048** ■ (DOI: 10.1177/0192623312474865) is currently the most authoritative sampling consensus:

- **Structures regularly sampled:** caudate/putamen, cerebellum, cerebral cortex, choroid plexus, eye (including optic nerve), hippocampus, hypothalamus, medulla, midbrain, nerve, olfactory bulb (**rodents only**), pons, spinal cord, thalamus.■
- **Number of sections:** rodents **6–7 coronal sections, sampled bilaterally**; non-rodents **6–7 coronal hemisections**.■
- **Fixation and embedding:** CNS/PNS immersion-fixed in formalin, eyes in an acetic-acid-containing fixative; paraffin-embedded; H&E only for the initial screen.■
- **Reading:** The initial microscopic evaluation is **qualitative and unblinded (evaluator aware of treatment and dose)**; the pathology report must state explicitly which structures were evaluated.■
- The paper notes: previous routine rodent general toxicity studies used **3-level** sampling, which carries a risk of missed findings compared with 6–7 levels; the working group recommends routinely screening the above structures in general toxicity studies, while allowing institutions flexibility to customize provided that "the major neural targets are systematically evaluated."■

The **RENI revised sampling guides (rat/mouse BRAIN)** ■ give an operational definition of the 3-level screen (corresponding to the historical 3-level practice in Bolon):
1. **Optic chiasm level** (forebrain: cortex, basal ganglia, septum, anterior hypothalamus);
2. **Posterior hypothalamus level** (hippocampus, cortex, diencephalic–mesencephalic transition);
3. **Mid-cerebellum + medulla level** (cerebellum, brainstem).
Optional: 4) mid-pons; 5) cranial cervical spinal cord.■ Sections are cut transversely, embedded with the rostral face down; a brain matrix mold allows precise vertical cuts at 1 mm intervals; the spinal cord should be cut at a consistent level to ensure accurate brain weight; **do not store specimens in alcohol for prolonged periods** (may cause artifactual vacuolation).■

**DeFazio et al. 2015 (rat matrix-guided trimming)** ■: using 8 channels keyed to anatomical landmarks (midpoint of the optic chiasm, frontal pole, optic chiasm, infundibulum, mammillary body, midbrain, mid-cerebellum, posterior cerebellum), validation in 60 10-week-old male Han Wistar rats (298±29 g) showed the expected target structures present at each level in **89–100%** of cases, with most misses being caudally displaced. — This shows that **even with a mold, about 1 in 10 sections will deviate**, so the pathology report should record the actual section level, not the assumed one.

**Non-rodents (Göttingen minipig as the example):** Tier 1 (general toxicity screen) uses **7 coronal hemisections** (consistent with the STP non-rodent recommendation); Tier 2 (dedicated neurotoxicity, when the nervous system is a known/suspected target organ) uses **14 coronal hemisections + 2 full coronal sections**.◐ (STP minipig monograph, ResearchGate abstract; full text not open access, figures are as given in the abstract.) Sampling of the spinal cord, ganglia (somatic and autonomic), and nerves follows STP CNS/PNS best practice.

#### (b) Fresh vs perfusion/fixed: split by endpoint — do not compromise after the fact

| Endpoint | Recommended tissue handling | Rationale / evidence |
|---|---|---|
| Histopathology (H&E, special stains, IHC) | **Perfusion fixation via the heart**, commonly 4% paraformaldehyde (PFA) / 10% neutral buffered formalin; the brain autolyzes rapidly, so perfusion is better than immersion ■ | Perfusion fixation best preserves morphology, especially for the brain (rapid autolysis); consensus cited by McFadden et al.: perfusion is superior to immersion.■ But PFA cross-linking severely limits extraction of intact RNA (RNA–protein binding, sequestration in large complexes).■ |
| LC-MS/MS bioanalysis (parent/metabolite quantitation) | **Fresh snap-frozen, no perfusion fixation**; if blood removal is needed, briefly perfuse with ice-cold saline and record it | Fixatives/paraffin interfere with mass spectrometry; formalin cross-linking changes drug extraction recovery.■ After snap-freezing, store at −80 °C and section in a cryostat at −17 to −20 °C.■ |
| Imaging mass spectrometry (MALDI/DESI/ToF-SIMS MSI) | **Fresh snap-frozen is most suitable** ■ | Hanrieder et al. review: commonly used perfusion/fixation strategies are generally incompatible with mass spectrometry (paraffin and other polymers interfere); fresh-frozen tissue is the most commonly used sample for all target molecules (drugs, metabolites, lipids, peptides, proteins).■ **A post-mortem delay of only 3 minutes can cause severe degradation of proteins/peptides**, distorting the true profile of endogenous molecules and drug metabolites.■ |
| RNA-seq / spatial transcriptomics | **Fresh snap-frozen preferred**; ethanol fixation as a compromise | 70% ethanol immersion fixation: RNA yield ~**70%** of fresh-frozen, with comparable integrity and stable RT-PCR success; formalin fixation yields negligible RNA, FFPE RNA is low-molecular-weight fragments with repeated RT-PCR failure (Su et al.).■ RNA recovery from ethanol/RNAlater-fixed tissue after LCM is ~**80–90%** of fresh-frozen.■ A 2025 report described immune LCM + RNA-seq from PFA perfusion-fixed mouse brain using an adapted kit ("reasonable" RNA quality, suitable for qPCR/RNA-seq)◐ — an emerging method, not yet routine. |
| Spatial proteomics / multiplex IF | Fresh snap-frozen or light fixation, depending on antibody validation | Fixation alters epitopes; each antibody must be validated under the fixation conditions used.◐ Practical consensus. |

**Key operating principles:**
- **Pre-allocation:** e.g. in the rat, left hemisphere perfusion-fixed for pathology, right hemisphere fresh snap-frozen for LC-MS/MS/MSI; or split by animal subgroup (satellite groups). **Do not perform MSI and then H&E on the same piece of tissue without an adjacent-section control** — MSI matrix deposition and laser ablation alter the tissue.
- **Brain weight:** Weigh after cutting the spinal cord at a consistent level; change in brain weight is itself an endpoint in TG 424/426.■
- **Left/right and bilateral symmetry:** Transverse sections are used to judge whether lesions are unilateral/bilateral, symmetric/asymmetric — critical for distinguishing dosing-procedure injury, vascular lesions, and systemic neurotoxicity.■

#### (c) Regional microdissection and laser capture microdissection (LCM)

- **Manual microdissection:** On ice, using a brain matrix + scalpel/punch to separate large regions (cortex, hippocampus, striatum, hypothalamus, cerebellum) according to atlas landmarks. Advantages: high throughput, sufficient tissue (suitable for LC-MS/MS); disadvantage: boundary precision is on the millimeter scale, and small nuclei (e.g. amygdala subnuclei, locus coeruleus, substantia nigra pars compacta) are easily contaminated by neighboring regions.◐ Practical consensus.
- **Laser capture microdissection (LCM):** Cutting out defined cell populations (e.g. Purkinje cells, hippocampal CA1 pyramidal cells, TH+ dopaminergic neurons) from frozen or fixed sections based on morphology/immunolabeling; as few as **250 neurons** suffice for RNA-seq (methodology papers in mouse and human post-mortem brain).■ Advantages: cell-type specificity; disadvantages: low throughput, low RNA yield, sensitivity to fixation (see table above).
- **Spatial omics (Visium/Xenium/CosMx/GeoMx):** Transcriptomics/proteomics on the same/adjacent sections with spatial coordinates preserved; co-registration with MSI is covered in §5.3.◐ Emerging; platforms differ greatly in resolution (Visium ~55 µm capture spots; Xenium subcellular) and fixation requirements, so platform selection must be designed together with the pathology endpoints.

---

## 2. Brain Region Function Map

### 2.1 Region–function table

The table below reflects textbook-level consensus (■); the cross-species translation column notes the confidence level. Functions are described for mammals in general; human-specific functions (language, complex executive function) are noted separately.

| Brain region | Core function | Cross-species translation and caveats |
|---|---|---|
| **Cerebral cortex** (frontal, parietal, temporal, occipital, insular, cingulate) | Sensation, movement, association, executive function, memory, emotional integration; laminar (I–VI) and columnar organization | Six-layered neocortical structure is conserved ■; but **frontal lobe differentiation differs the most** (see §1.1); rodent cortex is mainly sensorimotor, whereas association cortex is greatly expanded in primates. |
| **Prefrontal cortex (PFC)** | Working memory, decision-making, attention, rule learning, social behavior; medial stream biased toward evaluation/self-monitoring, lateral stream toward executive control ◐ (Vertes et al. 2025 two-stream framework) | **Largest translation gap**: the primate granular dlPFC has no homologue in rodents ■; the correspondence of rodent prelimbic/infralimbic cortex is still disputed ◐. For medicinal chemists: do not equate rat mPFC behavioral data with human dlPFC function. |
| **Hippocampus** (CA1/CA2/CA3, dentate gyrus DG, subiculum) | Episodic/spatial memory, learning; stress-sensitive; neurogenesis (DG) | **Highly conserved** ■; CA1 is particularly vulnerable to ischemia, excitotoxicity, BMAA, etc. (see §5 cases). Rodent Morris water maze, NHP/human paired-associate/spatial tasks — the tasks are not equivalent and must be chosen by species. |
| **Striatum** (caudate, putamen; in rodents collectively caudate-putamen, CPu; nucleus accumbens) | Movement initiation/habits, reward, motivation; dopaminergic regulation | Conserved ■; but in humans/primates the caudate and putamen are separated by the internal capsule, whereas in rodents they form a single CPu — **anatomical subdivision nomenclature differs, so do not confuse them during sampling**. MPTP damages the nigrostriatal pathway (see §5). |
| **Thalamus** (including dorsomedial nucleus MD, ventrolateral nucleus VL, etc.) | Sensory/motor relay, consciousness, attentional gating; MD projections are one of the classical criteria defining the PFC | Conserved ■; MD projections were once used as the anatomical criterion defining the PFC, but that criterion is itself disputed (MD projections are widely distributed across the frontal lobe and are not unique to dlPFC)■. |
| **Hypothalamus** (preoptic area, arcuate nucleus, paraventricular nucleus, supraoptic nucleus, median eminence) | Body temperature, feeding, circadian rhythm, stress (HPA axis), endocrine function | Conserved ■; **the arcuate nucleus and median eminence are CVOs that lack a typical BBB** — systemically administered peptides (e.g. GLP-1 RA) can act directly here, producing appetite/nausea effects (see §4.1). |
| **Amygdala** (basolateral nucleus, central nucleus, etc.) | Fear, emotional memory, stress, social behavior | Conserved ■; the central nucleus–brainstem pathway mediates autonomic responses; rodent fear conditioning translates relatively well to humans, but subnuclear parcellation is finer in NHP/humans. |
| **Cerebellum** (vermis, hemispheres, cerebellar nuclei, Purkinje cells) | Motor coordination, balance, motor learning; recent evidence extends to language, attention, working memory ◐ | Structurally conserved ■; but the human/great ape cerebellum expanded faster than whole-brain growth ◐; Purkinje cells are sensitive to many toxicants (e.g. ethanol, certain chemotherapeutics). Sampling must include the vermis and hemispheres and the deep nuclei. |
| **Brainstem** (midbrain, pons, medulla) | Respiration, heart rate, arousal, motor/sensory conduction; contains monoaminergic nuclei such as the substantia nigra, locus coeruleus, and raphe nuclei | Conserved ■; monoaminergic nuclei are targets of many neurotoxicants (MPTP, certain sympathomimetics). |
| **Substantia nigra** (pars compacta SNpc / pars reticulata SNpr) | Dopaminergic neurons (SNpc → striatum) regulate movement; SNpr is GABAergic output | **MPTP selectively damages SNpc dopaminergic neurons** ■; human SNpc contains neuromelanin, whereas rodents have low levels — one hypothesis for the species difference in MPTP sensitivity ◐. |
| **Circumventricular organs (CVOs)** (area postrema, choroid plexus, pineal gland, OVLT, subfornical organ, median eminence, posterior pituitary) | Sense blood chemistry signals (toxins, hormones, osmolarity), secrete hormones into blood, secrete CSF | **All lack a typical BBB (fenestrated capillaries, no tight junctions)** ■; the area postrema is the chemoreceptor trigger zone (CTZ) mediating emesis — nausea/vomiting from chemotherapeutics, opioids, and GLP-1 RA largely act via this route.■ But a tanycyte barrier lies between the CVOs and the rest of the brain parenchyma, so substances **do not freely diffuse** into the whole brain.■ |
| **Choroid plexus / ventricular system** | Secretes CSF, forms the blood–CSF barrier | CSF concentration **≠** unbound concentration in brain parenchyma (see §4.2); the choroid plexus is one of the STP-mandated structures ■. |
| **Pituitary** (anterior/posterior lobes) | Endocrine center | Posterior lobe is a CVO; anterior lobe is regulated by the hypothalamic portal system; toxicology sampling usually examines it together with the brain.■ |

### 2.2 Known translational gaps — enter them in the protocol's risk register

1. **Prefrontal cortex (largest gap):** See §1.1. Rodents lack a granular dlPFC; using rat mPFC lesions/behavior to predict human executive-function impairment is **insufficiently supported**.■ Mitigation: NHP cognitive tasks (e.g. delayed response, the monkey version of the Wisconsin Card Sorting Test), human iPSC-derived neurons/organoids, imaging biomarkers.
2. **Olfactory system:** Rodent/dog olfactory bulbs are large and olfaction-dominant; human olfaction is regressed. Olfactory bulb lesions, nose-to-brain distribution, and inhalation toxicity are common in rodents but of limited significance in humans.■ Mitigation: report the concentration/lesion ratio of olfactory vs non-olfactory brain regions together; do not report whole brain alone.
3. **Fineness of corticostriatal circuitry:** Primate corticostriatal projections are highly parcellated by functional domain; rodent parcellation is coarser.◐ Region-specific toxicity (e.g. affecting only associative striatum) may be masked by whole-striatum homogenate in rodents.
4. **Neurogenesis and developmental timing:** Human brain development continues to ~20 years of age; the rat reaches adult levels of neurotransmitters/synaptic plasticity/myelination at ~PND60 (timeline cited in the OECD DNT background document)◐; conversion of exposure windows for developmental neurotoxicity (DNT) cannot be based on body weight alone.
5. **Behavioral tests are not equivalent:** Rat Morris water maze ≠ human episodic memory; rodent motor activity ≠ human psychomotor function. Each behavioral endpoint must state the construct it measures and its known species limitations.◐ Practical consensus.

---

## 3. Neurotoxicity Assessment ("tox")

### 3.1 Regulatory frameworks and study designs

| Framework / guideline | Scope | Key design elements (verified) |
|---|---|---|
| **OECD TG 424** Neurotoxicity study (rodents, adopted 1997-07-21)■ | Confirmation/characterization of neurotoxicity in adult animals; may be standalone or incorporated into a repeat-dose toxicity study | Rat, oral (gavage/diet/drinking water/capsule); 28 days, 90 days, or chronic ≥1 year; standalone study ≥20 animals per dose (10 females + 10 males); limit test ≥1,000 mg/kg bw; endpoints include body weight, food/water consumption, functional tests, daily detailed observations, ophthalmology, hematology, clinical chemistry, histopathology; **at least 5 males + 5 females perfused in situ for detailed neuropathology**; results evaluated by incidence, severity, and correlation of neurobehavioral and neuropathological effects.■ |
| **OECD TG 426** Developmental neurotoxicity (DNT, 2007)■ | Functional and morphological hazards to offspring nervous systems (in utero + early postnatal exposure) | Rat preferred; dams dosed daily from implantation (GD6) through lactation (PND21); ≥3 doses + control; **20 litters per dose**; offspring evaluated for physical development, reflexes, motor function, sensory development and function, spontaneous activity, learning and memory, neuropathology; brain weight and neuropathology through adulthood (~PND70).■ May be replaced/complemented by the DNT cohorts (2A/2B) of TG 443 (EOGRTS).◐ |
| **OECD TG 443** Extended One-Generation Reproductive Toxicity Study (EOGRTS) | Comprehensive reproductive/developmental assessment including DNT cohorts | Offspring exposed from in utero and lactation through direct dosing after weaning until termination at ~PND66–77; DNT parameters include motor activity, motor/sensory function, learning and memory, brain weight, neuropathology.◐ |
| **ICH S7A** Safety pharmacology (2000)■ | Protects clinical trial subjects/patients from adverse pharmacodynamic effects of drugs; core battery | Core battery: **central nervous system (CNS) + cardiovascular system + respiratory system**. CNS evaluation is usually a rodent observational battery after a single dose (Irwin test / simplified FOB), conducted at therapeutic exposure and above.■ A 2023 review called for revising S7A (insufficient citation of in vitro/in silico models, limited predictivity of some in vivo models)◐ — the guideline itself remains in effect. |
| **ICH S7B** (QT) | Delayed cardiac repolarization | No direct relationship to the CNS, but run in parallel within the same safety pharmacology package; listed here only to avoid confusion. |
| **ICH S4** Duration of chronic toxicity (1998)■ | Duration of chronic toxicity studies | Chronic studies of **6 months in rodents and 9 months in non-rodents** generally support clinical dosing >6 months.■ |
| **ICH M3(R2)** Timing and scope of nonclinical safety studies ■ | Nonclinical package by clinical stage | Specifies the repeat-dose toxicity study duration and number of species required at each clinical stage (e.g. clinical trials ≤2 weeks require ≥2-week studies in 2 species); used together with S4/S7A/S5, etc.■ |
| **US EPA OPPTS 870.6200 / 870.6300** | Neurotoxicity and DNT for US pesticides/chemicals | Parallel to OECD TG 424/426; TG 426 was based on the EPA guideline.■ |
| **FDA guidances** (drugs) | Specific indications/modalities may carry additional CNS requirements | This report did not search FDA guidances one by one; **search the FDA Guidance database by indication before submission** — marked here as not fully verified ○. |

**Dose selection principles (general, ■):** At least 3 doses + control, spanning the range from no toxicity to toxicity; the high dose should be based on prior toxicity and kinetic data to avoid masking neuro-specific effects with systemic toxicity/mortality; include a recovery group to assess reversibility; toxicokinetic (TK) satellite groups for exposure confirmation — **do not use the brains of main-study animals for both TK and pathology without pre-allocation**.

### 3.2 In-life functional readouts

| Category | Common methods in rodents | NHP / dog / minipig | Caveats |
|---|---|---|---|
| **Functional Observational Battery (FOB)** | Home-cage observation, open-field observation, sensory responses (tactile, auditory, visual, pain), grip strength, landing foot splay, body temperature, autonomic signs ■ | Species-adapted versions in NHP/dog (clinical observation + neurological examination); gait/posture scoring in minipig ◐ | FOB is a **screening, non-invasive** tool designed to detect gross functional deficits and must be used together with neuropathology; it is not a detailed neurotoxicity evaluation.■ Observation conditions, timing, and observer blinding must be standardized. |
| **Motor activity** | Automated recording cages (photobeam/video), circadian rhythm, habituation | Activity monitoring, video tracking | Must be measured at multiple time points after dosing (acute vs chronic effects differ); decreased motor activity may reflect systemic toxicity, weight loss, or sedation and is **not neuro-specific**. |
| **Motor/sensory function** | Rotarod, grip strength, gait analysis, auditory startle | Neurological examination, gait scoring | TG 426 offspring require motor activity, motor/sensory function, and auditory startle.■ |
| **Learning and memory** | Morris water maze (spatial), novel object recognition, passive avoidance, operant conditioning | NHP: delayed response, paired associates, monkey version of the Wisconsin Card Sorting Test; dog: object discrimination | **Tasks are not equivalent** (see §2.2); learning and memory testing is a standard requirement in TG 426 and optional in TG 424 (added as needed).■ |
| **Electrophysiology** (supplementary) | EEG, nerve conduction, evoked potentials | Same as left; awake EEG possible in NHP | TG 424 allows electrophysiology/neurochemistry as supplementary examinations.■ |

| **Ophthalmology** | Slit lamp, fundoscopy | Same as left | Required by TG 424; the retina/optic nerve are CNS extensions and must be examined routinely.■ |

**Positive controls and sensitivity:** The sensitivity of the FOB/motor activity depends on observer training and baseline variability; the protocol should state the historical control range and the use of positive control drugs (where applicable).◐ Practical consensus; there is no unified regulatory text on the choice of specific positive control drugs.

### 3.3 Neuropathology

- **Fixation:** In situ perfusion fixation is an explicit requirement for the TG 424 neuropathology subgroup (≥5/sex/group).■ Perfusion fluid, flow rate, and pressure must be standardized and recorded; poor perfusion (uneven fixation, dark neuron artifacts) is one of the most common sources of pathology artifacts.◐
- **Sectioning:** See §1.3 (6–7 levels). Routine H&E for the initial screen; **do not conclude "no neurotoxicity" on H&E alone** — H&E is insensitive to early axonal degeneration and mild glial responses.■
- **Special stains and markers (Expanded neurohistopathology, ENHP):** Use expanded processing when the drug is expected to be neuroactive, when H&E reveals suspicious lesions, or when the site/extent of action is unclear.■ The table below follows the STP Forum opinion (Bolon, *Toxicol Pathol* 2024) and multi-source consensus:

| Marker / stain | Detects | Timing / characteristics |
|---|---|---|
| **H&E** | Routine morphology: neuronal necrosis/loss, vacuolation, inflammation, vascular lesions | Initial screen; limited sensitivity ■ |
| **Fluoro-Jade B/C (FJ)** | **Degenerating neurons** (CNS) | High affinity and specificity for degenerating neurons; generally not applicable to dorsal root ganglion (DRG) neuronal degeneration ■; in the DFP rat model, FJ-B positivity was seen in multiple brain regions 1–14 days after exposure ■ |
| **GFAP** (glial fibrillary acidic protein, IHC) | Astrocytes / reactive astrogliosis | Reactive astrocytes appear at ~**7–14 days** and persist longer than the microglial response ■; GFAP elevation is a general marker of many types of CNS injury ■ |
| **Iba1 / IBA1** (ionized calcium-binding adapter molecule 1, IHC) | Microglial / macrophage activation | Reactive microglia appear **early (within hours to 7 days)** ■; morphology (hypertrophy, amoeboid form) matters more than positive area alone |
| **Amino-cupric-silver stain** | Degenerating neurons (CNS) | **Frozen sections only** ■ |
| **Myelin stains** (Luxol fast blue, etc.) / MBP IHC | Myelin integrity, demyelination | In the BMAA model, striatal MBP decreased dose-dependently (see §5)■ |
| **NeuN / synaptophysin** | Neuronal nuclei / presynaptic terminals | Aids quantitative neuronal counts and synapse loss; decreased synaptophysin suggests synaptic injury ◐ |
| **TH** (tyrosine hydroxylase) | Dopaminergic neurons/fibers | In the MPTP model, SNpc TH+ neurons decreased by 30–70% and striatal TH+ fibers by 40–90% (**figures cited from secondary reviews/vendor materials, not primary sources, ○ for order-of-magnitude reference only — do not cite directly**) |

- **Reading and reporting:** The qualitative initial screen is unblinded; quantitative/semi-quantitative scoring (e.g. severity grades 0–4) should be re-checked blinded; lesions must be described by **anatomical site, distribution (focal/multifocal/diffuse), uni-/bilateral, symmetry, and cell type**, using INHAND nomenclature (*Proliferative and Nonproliferative Lesions of the Rat and Mouse CNS/PNS*, *Toxicol Pathol* 2012).■ INHAND is the internationally harmonized nomenclature for rodent lesions established jointly by ESTP/BSTP/JSTP/STP.■
- **Background lesions:** Spontaneous lesions in aged rats (unrelated to e.g. progressive nephropathy), Beagle pain syndrome, spontaneous arteritis/polyarteritis in Göttingen minipigs, etc., can all interfere with interpretation; use concurrent and historical controls to distinguish them.◐

### 3.4 Biomarkers — signals of neural injury in blood/CSF

| Biomarker | Biology | Current status and limitations |
|---|---|---|
| **NfL** (neurofilament light chain) | Neuron-specific cytoskeletal protein; released into CSF and blood after CNS or PNS injury ■ | **The most promising general axonal injury marker** ◐. Serum NfL in healthy volunteers rises with age by ~**2.36%/year**, GFAP by ~1.18%/year; on longitudinal monitoring, a rise of **1.64-fold** over baseline was calculated as the upper limit of normal (ULN) (Lanz et al., *J Neurol* 2025;272:512, 270 cross-sectional + 80 longitudinal cases)■. NfL has a long half-life and remains detectable days to weeks after injury, making it suitable for longitudinal monitoring.■ **Regulatory qualification is not yet complete**: public–private partnerships such as TransBioLine are working to qualify NfL and others as biomarkers of drug-induced neurological injury (DINI) ◐ — **currently an exploratory/supportive endpoint that cannot replace histopathology**. NfL is **not region-specific** (it rises with injury anywhere in the brain/peripheral nerves) and cannot localize lesions.■ |
| **GFAP** (plasma/CSF) | Astrocyte intermediate filament protein; rises with astrogliosis/injury | Plasma GFAP rises in AD and other diseases; it complements NfL in acute CNS injury (glial vs axonal).◐ Detectable in 100% of healthy volunteers (Simoa 4-plex)■. Also not region-specific. |
| **Tau** (total tau / p-tau181 / p-tau217) | Neuronal microtubule-associated protein; phosphorylated tau is associated with tau pathology | Plasma p-tau217/p-tau181 are highly valuable for AD diagnosis, but validation in **drug-induced neurotoxicity** is far less than for NfL ◐; total tau is detectable in only ~67% of healthy human serum (Lanz 2025)■, with lower sensitivity than NfL/GFAP. |
| **UCH-L1** | Neuronal cytoplasmic protein, acute neuronal lysis marker | Detectable in only ~4% of healthy human serum ■; narrow acute window (hours–days), limited value in chronic toxicity studies ◐. |
| **Others (exploratory)** | S100B, NSE, miRNA, TSPO PET ([¹¹C]-(R)-PK11195) | TSPO PET in DFP rats showed hippocampal/cortical neuroinflammation peaking on day 7 and persisting to day 21 ■; but TSPO is also expressed on peripheral immune cells, limiting specificity ◐. |

**Recommendation:** In repeat-dose toxicity studies, **longitudinal blood sampling for NfL (+ GFAP)** is currently the most cost-effective exploratory strategy: baseline → mid-dosing → terminal → recovery; each animal as its own control (fold-change is better than a single absolute value).◐ A positive signal must be traced back to histopathology and regional exposure; it cannot by itself support a conclusion of "neurotoxicity positive."

---

## 4. Locating Brain Distribution

### 4.1 Blood–brain barrier (BBB) biology

The BBB is the **neurovascular unit (NVU)** composed of brain microvascular endothelial cells + pericytes (embedded in the basement membrane) + astrocytic endfeet (covering >99% of the microvascular surface).■ Its barrier function comes from:
- **Tight junctions**: claudin-5, occludin, ZO-1, etc., which virtually eliminate paracellular permeability;■
- **Low pinocytosis/endocytosis rates and absence of fenestrations**;■
- **Efflux transporters** (see below);■
- **A metabolic enzyme barrier** (e.g. monoamine oxidases, cytochrome P450, extent varies by substrate)◐.

**Transport routes (5 classes):** Passive transcellular diffusion (lipophilic small molecules), paracellular diffusion (minimal, negligible at the BBB), carrier-mediated influx (CMT, e.g. GLUT1, LAT1), transporter-mediated active efflux, and receptor-mediated transcytosis (RMT, e.g. transferrin receptor, insulin receptor, LDL receptor).■

| Transporter | Gene | Direction / substrates | Species-difference highlights |
|---|---|---|---|
| **P-gp** (P-glycoprotein, MDR1) | *ABCB1* | Efflux (brain → blood), luminal side; broad substrate range (lipophilic, many drugs)■ | Quantitative proteomics: **mouse brain capillary P-gp expression is higher than in monkey and human**; rat brain endothelial P-gp activity is higher than monkey for some substrates ◐. Human and monkey BBB transporter expression are close; mouse differs more ■. |
| **BCRP** (breast cancer resistance protein) | *ABCG2* | Efflux, luminal side; substrate overlap with P-gp is extensive, jointly blocking drug entry into the brain ■ | Proteomics shows **BCRP is the most abundant transporter in the human BBB** ◐; mouse Bcrp expression is lower than human, while P-gp is higher ■. When a BCRP substrate shows impaired brain penetration in rodents, a P-gp inhibitor cannot correct it — BCRP must be evaluated as well.■ |
| **MRPs** (MRP1/2/4/5) | *ABCC1/2/4/5* | Efflux (mainly endogenous metabolites, brain → blood) | MRP4 has the highest gene/protein level in human brain microvessels, but its protein level is far lower than in mouse ◐. |
| **GLUT1** | *SLC2A1* | Influx (glucose) | Highly expressed, conserved across species ■. |
| **LAT1** | *SLC7A5* | Influx (large neutral amino acids; levodopa, gabapentin, etc. use this route) | Conserved; can be exploited for prodrug/transporter-targeted design ◐. |
| **MFSD2A** | *MFSD2A* | Influx (lysophosphatidylcholine–DHA); suppresses endocytosis and maintains BBB integrity | In primate BBB co-culture models, expression can be upregulated by astrocytes/pericytes ◐. |
| **OATPs / OATs / OCTs** | *SLCO / SLC22* | Bidirectional, substrate-dependent | Expression and function differ greatly between species; in vitro–in vivo extrapolation requires caution ◐. |
| **H⁺/organic cation (H⁺/OC) antiporter** | Not fully identified | Influx (pyrilamine-sensitive); substrates include pyrilamine, diphenhydramine, bupropion, tramadol, oxycodone, memantine | 2024 rat CMA-ROI study: Kp,uu,ROI >1 in all brain regions with no significant regional differences (region-independent active uptake)◐; the authors suggest high brain concentrations may be related to neurotoxicity, but **the mechanism–toxicity causal link has not been established** ○. |

**Circumventricular organs (CVOs) — the "intentional gaps" in the BBB:** The following structures **lack a typical BBB** (fenestrated capillaries, no tight junctions)■: area postrema, choroid plexus, pineal gland, organum vasculosum of the lamina terminalis (OVLT), subfornical organ, median eminence, posterior pituitary (some sources also list the preoptic recess).■ Their function is to **sense blood** (toxins, hormones, osmolarity) and **secrete into blood** (hormones, CSF). The area postrema, located at the floor of the fourth ventricle on the caudal medulla, is the **chemoreceptor trigger zone (CTZ)**: it detects toxins/drugs in the blood and triggers emesis; its neurons express D2, 5-HT₃, opioid, muscarinic, and other receptors.■

**Direct implications for medicinal chemists:**
- Systemically administered macromolecules/polar drugs have **low overall brain penetration, but CVO concentrations can be very high** (e.g. GLP-1 RA labeling is strongest in the area postrema and arcuate nucleus, with limited penetration into deep brain parenchyma — this conclusion comes from a secondary review of the GLP-1 literature, ○ cite a primary source before using it).
- Nausea/vomiting, appetite suppression, and temperature/endocrine effects **cannot be ruled out as centrally mediated on the basis of low whole-brain Kp alone** — CVO exposure and receptor occupancy must be examined separately.
- A **tanycyte barrier** lies between the CVOs and the rest of the brain parenchyma, so substances in the CVOs **do not freely diffuse** into the whole brain; "high CVO concentration = high whole-brain concentration" is a false inference.■

### 4.2 Key parameters (definitions — terminology must be harmonized)

| Parameter | Definition | Interpretation |
|---|---|---|
| **Kp,brain** (total brain-to-plasma ratio) | `Kp,brain = Cbrain,total / Cplasma,total`; logBB = log₁₀(Kp,brain) ■ | Describes **total extent of distribution**, not the available unbound concentration. A high Kp may reflect only high brain tissue binding (e.g. high lipophilicity, lysosomal accumulation) and **cannot serve as evidence of CNS activity/toxicity**.■ |
| **fu,plasma** | Unbound fraction in plasma (equilibrium dialysis/ultrafiltration)■ | Unbound plasma concentration Cu,plasma = fu,plasma × Cplasma,total. |
| **fu,brain** | Unbound fraction in brain homogenate (equilibrium dialysis, commonly 1:4 or 1:9 w/v dilution)■ | Assumes in vitro homogenate fu,brain = in vivo fu,brain. **This assumption does not hold for strongly basic compounds** (homogenization destroys lysosomal pH partitioning, causing fu,brain to be overestimated)■. |
| **Vu,brain** (unbound brain volume of distribution, mL/g brain) | `Vu,brain = Abrain / Cu,brainISF`; measured by the brain slice method ■ | Describes overall drug uptake/binding in brain tissue (intracellular + extracellular), independent of BBB function. Brain slice results agree with microdialysis within **~3-fold** in cited comparisons ◐. |
| **Kp,uu,brain** (unbound brain-to-plasma partition coefficient) | `Kp,uu,brain = Cu,brain / Cu,plasma = Kp,brain × fu,brain / fu,plasma = Kp,brain / (Vu,brain × fu,plasma)` ■ | **Core parameter**: at steady state, ≈1 indicates passive-diffusion equilibrium; <1 net efflux; >1 net influx.■ Note: Kp,uu,BBB from microdialysis (based on brain ECF) and Kp,uu,brain from homogenate (based on whole-brain homogenate) have **different meanings** for strongly basic / lysosomally accumulated compounds; the LeiCNS-PK3.0 paper argues for distinguishing the terms ◐. |
| **Kp,uu,ROI** | Regional unbound brain-to-plasma ratio (CMA-ROI method)◐ | Extends CMA to regions of interest (ROIs) for regional PK; in the H⁺/OC substrate study, all ROIs were >1 with no regional differences ◐. |
| **CSF-to-plasma ratio** | `CCSF,total / Cplasma,total` or the unbound ratio | **CSF ≠ brain parenchyma**: CSF is secreted by the choroid plexus (blood–CSF barrier, distinct from the BBB), with different flow rates, protein content, and transporters; CSF concentrations can be higher or lower than unbound brain ECF concentrations depending on the compound and barrier properties.■ **Do not use the CSF-to-plasma ratio as a substitute for Kp,uu,brain** unless the correlation has been validated for the same species and compound. |
| **CLin** (BBB permeability clearance) | Clearance into the brain per unit time (one of the three Hammarlund-Udenaes parameters)■ | Describes **rate**, complementary to Kp,uu (extent); in most repeat-dosing scenarios, extent matters more than rate.■ |
| **PS** (permeability–surface area product) | Passive permeability × capillary surface area | The in vivo counterpart of in vitro Papp; related to CLin. |

**Historical lesson (Hammarlund-Udenaes et al. 2008)■:** For CNS drugs, Kp (logBB) varies by **≥2,000-fold**, BBB permeability by **≥20,000-fold**, whereas Kp,uu,brain varies by only ~**150-fold**. — Optimizing total Kp optimizes binding, not the concentration available at the target. The Loryan et al. 2022 industry survey showed: 93% of responding pharmaceutical companies had established cross-disciplinary consensus on the Kp,uu,brain concept, 79% called its combined impact "game-changing," and 74% considered the existing Kp,uu toolbox sufficient for discovery/early development, although human brain PK/PD translation still needs improvement.■

### 4.3 Comparison of methods for measuring regional distribution

| Method | Spatial resolution | Quantitation | Parent vs metabolite | Advantages | Limitations / pitfalls |
|---|---|---|---|---|---|
| **LC-MS/MS (regional homogenate)** | Regional (mm; depends on dissection precision) | **Gold-standard quantitation** (ng/g)■ | Distinguishable (MRM)■ | Sensitive, specific, supports TK; can be split from pathology in the same animal | **Loses sub-regional spatial information**; homogenate averaging masks heterogeneity; residual blood must be corrected; fresh snap-frozen tissue required |
| **QWBA** (quantitative whole-body autoradiography) | Whole body, organ/regional (~50–100 µm, depending on phosphor screen) | **Regulatory gold-standard quantitation** (ng equiv/g)■ | **Cannot distinguish** parent from radiolabeled metabolites ■ | Whole-body distribution, high regulatory acceptance, supports clearance/metabolism assessment | Requires radiolabeling (large synthesis investment, radiation protection); high cost; cannot distinguish parent/metabolite; requires frozen whole-body sections |
| **MALDI-MSI** (imaging mass spectrometry) | **5–20 µm** (routine); high resolution down to ~5 µm ◐ | Semi-quantitative to quantitative (internal standard/calibration curve, qMSI)◐ | **Distinguishable** (different m/z for parent vs metabolite)■ | Label-free, molecularly specific, preserves spatial information, can visualize endogenous lipids/metabolites simultaneously | Quantitation not regulatory-validated; matrix interference (small-molecule drugs with m/z <500), ion suppression, large batch variation; fresh snap-frozen tissue required; **not a regulatory substitute for QWBA** ◐ |
| **DESI-MSI / ToF-SIMS** | DESI ~50 µm; SIMS down to sub-micron–1 µm ◐ | Mainly semi-quantitative | Distinguishable | DESI needs no matrix; SIMS has high spatial resolution, suitable for lipids/small molecules | Sensitivity/quantitation lower than MALDI/LC-MS/MS; SIMS has a limited mass range |
| **PET** (positron emission tomography) | mm scale (clinical ~4–6 mm; animal ~1–2 mm) | Quantitative (requires arterial input function/modeling) | **Cannot distinguish** parent from radiolabeled metabolites (unless the metabolite does not enter the brain) | **In vivo, longitudinal, same animal repeatedly**; can measure receptor occupancy | Requires radiolabeling (¹¹C t½ 20.4 min, ¹⁸F); low resolution (small nuclei cannot be resolved); high cost; ¹¹C-PET in MPTP is a case in point ■ |
| **Cerebral microdialysis** | Region around the probe (~mm³) | **Unbound ECF concentration–time curves**, gold standard ■ | Distinguishable (dialysate LC-MS/MS) | Directly measures Cu,brain; multiple regions and time points; Kp,uu can be calculated from AUC | Invasive (probe injury, glial scarring); recovery must be corrected (retrodialysis/no-net-flux); low throughput; poor recovery for large molecules/highly bound drugs |
| **Brain homogenate equilibrium dialysis** (fu,brain) | No spatial information | fu,brain | — | High throughput | Artifacts for strongly basic compounds (see §4.2)■ |
| **Brain slice uptake** (Vu,brain) | No spatial information (whole-slice average) | Vu,brain | — | More physiological (preserves cellular structure, lysosomal pH)■; a high-throughput version has been established ◐ | Demanding to operate; agrees with microdialysis within ~3-fold ◐ |
| **In vitro BBB models** (see below) | — | Papp, efflux ratio (ER) | — | High-throughput screening | **Cannot replace in vivo Kp,uu**; large species and expression differences |

**In vitro BBB models (ranked by fidelity; ◐ all emerging/adjunctive):**
- **PAMPA-BBB**: Artificial-membrane passive permeability screen; no transporters, no cells.■ For early passive-permeability ranking only.

- **MDCK-MDR1 / MDCKII-BCRP**: Canine kidney cells transfected with human/rat MDR1/BCRP; measure bidirectional permeability and efflux ratio (ER = Papp,B→A / Papp,A→B). A high ER suggests a P-gp/BCRP substrate; verify with inhibitors (verapamil, LY335979).■ But MDCK cells are kidney-derived, not brain endothelium, and their tight junctions and transporter expression profile differ from human brain endothelium; **ER thresholds (e.g. <2) are empirical rules, not regulatory standards** ○.
- **hCMEC/D3**: Immortalized human brain microvascular endothelial cell line; expresses P-gp, BCRP, GLUT1, etc., but TEER is low (~100–150 Ω·cm² vs 1,500–2,000 Ω·cm² in vivo, cited from a secondary review ○) and transporter expression is lower than in primary cells.◐ Monolayer models underestimate barrier tightness.
- **Primary brain endothelium + pericyte + astrocyte co-culture (EPA model)**: TEER and expression of tight-junction proteins (occludin, claudin-5, ZO-1) and transporters (GLUT1, MFSD2A, ABCB1, ABCG2) are all higher than in monolayers; permeability coefficients for 10 drugs correlated between the monkey EPA model and the rat EPA model with R²=0.88, higher than the monkey model vs mouse in vivo data (R²=0.66) — suggesting transporter species differences.◐ (Single paper, *Pharmaceutics* 2021)
- **iPSC-derived BBB models**: Human-derived, can be patient-specific, but differentiation protocols, TEER, and transporter maturity vary greatly and are **not yet standardized** ◐. Do not use a single iPSC model result to overrule in vivo data.

**Species differences in transporters (summary, ■/◐):** Human and monkey brain capillary transporter expression are close; mouse differs more; mouse P-gp is high and Bcrp is low; rat P-gp activity is higher than monkey for some substrates.■ **Implication:** When rodent Kp,uu is low (strong efflux), human Kp,uu may be higher (weaker efflux) — rodent data are conservative; conversely, when rodent Kp,uu ≈ 1, humans may not be the same. **Any cross-species Kp,uu extrapolation must note the uncertainty from transporter expression differences.**

### 4.4 CSF, the blood–CSF barrier, and common misreadings of "brain distribution"

- CSF is secreted by the choroid plexus, flows through the ventricles → subarachnoid space → venous sinuses for absorption; CSF bulk flow clears drugs from brain ECF and is one of the clearance terms in the Kp,uu equation.■
- Lumbar CSF (clinically accessible) differs in concentration from ventricular CSF and brain ECF; lumbar CSF concentrations are closer to the spinal cord than to the cortex/hippocampus.◐
- **Do not infer "adequate brain parenchymal concentration" from "measurable CSF concentration,"** nor "no drug in the brain" from "low CSF concentration" — brain tissue or microdialysis data are also required.■

---

## 5. Correlation Analysis: From Regional Exposure to Toxicity

### 5.1 The logic framework for correlation (set the criteria first, then look at the data)

A credible conclusion of "regional exposure → regional toxicity" must satisfy all **four** of the following (all are required; adapted from the Bradford Hill causal inference framework into a practical formulation for neurotoxicology ◐):

1. **Spatial concordance:** The regions with the most severe/earliest lesions are those with the highest unbound concentration (or highest target occupancy, or strongest metabolic activation); regions with mild/no lesions have low concentrations. Comparisons must be made at the **same anatomical level, in the same animal/same cohort** — **do not use whole-brain concentrations from study A to explain regional lesions in study B**.
2. **Dose–response:** Regional concentration and lesion incidence/severity change monotonically with dose; there is a regional correspondence of NOAEL/LOAEL.
3. **Temporal concordance:** Exposure peaks / cumulative exposure precede or coincide with functional and pathological changes; during recovery, falling concentrations accompany recovery of function/markers (or irreversibly persistent lesions, which must be explained separately).
4. **Mechanistic plausibility:** Target/transporter/metabolic enzyme expression and cell-type vulnerability in that region (e.g. uptake of MPP⁺ by dopaminergic neurons with high DAT expression) can explain why that region is affected. **Regional molecular data** (IHC, spatial omics, receptor autoradiography) must support this, not literature speculation alone.

**Counterexample warning:** High whole-brain concentration + hippocampal lesions ≠ high hippocampal concentration. Hippocampal lesions may arise from systemic factors (hypoglycemia, hypoxia, hyperthermia, status epilepticus) or be secondary to systemic toxicity rather than high hippocampal drug concentration. See §5.4.

### 5.2 Exposure–response / PK-PD modeling (with unbound brain concentrations)

- **Use unbound brain concentration (Cu,brain), not total brain or plasma concentration, as the driving concentration for PK-PD.** ■ Multiple CNS drug studies show that unbound brain concentration correlates with pharmacological effect/receptor occupancy significantly better than total brain concentration.■
- **Model selection:** Direct-effect models (Emax, Cu,brain → effect) suit reversible functional effects; indirect-effect/turnover models suit delayed changes in markers such as GFAP/NfL; disease-progression models suit chronic neurodegenerative changes.◐
- **Regional PK-PD:** Fit Kp,uu,ROI against effect (e.g. FJ+ neuron counts, GFAP area fraction in that region) separately for each ROI rather than using whole-brain averages. The H⁺/OC substrate study used the CMA-ROI method and showed Kp,uu >1 in all ROIs with no regional differences — a result that **rules out the hypothesis that "regional concentration differences explain regional toxicity,"** pointing instead to regional target/vulnerability differences.◐ This is an example of how "a negative regional PK result is equally valuable."
- **PBPK models (e.g. LeiCNS-PK3.0):** Using Kp,uu,BBB, plasma PK, and CNS physiological parameters (cerebral blood flow, CSF flow rate, brain ECF volume) as inputs, they predict concentration–time curves in brain ECF, lateral ventricles, cisterna magna, and subarachnoid space; validation errors in rat and human were within 2-fold (as stated by the authors)◐. PBPK can be used to **predict human brain exposure before first-in-human (FIH) dosing**, but must be validated with animal data, and its ability to predict CVOs and BBB disruption in disease states is limited ◐.
- **Statistical points:** Correlation analyses between regional concentration and lesion scores must be done **per animal** (not per section) to avoid pseudoreplication; multi-region comparisons must be corrected for multiple testing; inter-observer agreement (kappa/ICC) for lesion scoring must be reported.◐ Practical consensus.

### 5.3 Spatial omics and pathology co-registration

**Workflow (◐ emerging, but with reproducible examples):**
1. **Adjacent-section strategy:** Section 1 (fresh snap-frozen) → MALDI/DESI-MSI (drug/metabolites/lipids); section 2 (adjacent, ±10–20 µm) → H&E / IHC (pathology anchor); section 3 (adjacent) → spatial transcriptomics (Visium/Xenium) or spatial proteomics.■ Registration error between adjacent sections must be quantified (landmark registration, non-rigid registration such as GreedyFHist).
2. **Same-section strategy:** Transcriptomics on the same section after MALDI-MSI (e.g. the ESCDAT method, >91% transcriptomic correlation retained after MALDI, single report ◐) or fluorescence imaging before MSI. Advantage: pixel-level co-registration; disadvantage: MSI matrix/laser may affect subsequent omics quality, requiring methodological validation.
3. **Computational integration:** Open-source frameworks such as SpatialData can unify Visium, Xenium, histology, and MSI in the same spatial coordinate system; resolution differences (MSI 5–50 µm, Visium 55 µm capture spots, Xenium subcellular) and batch effects must be handled.◐
4. **Biological interpretation:** Find differentially expressed genes/proteins/lipids within the lesioned ROI (e.g. phosphatidylcholine fragments and elevated phosphoethanolamine in BMAA CA1), then validate with IHC/in situ hybridization in an independent cohort. **A spatial omics finding ≠ mechanistic proof** — functional validation (knockout/inhibition/rescue experiments) is required.

**The complete chain in the BMAA case (see §5.5)** is one of the most complete examples of spatial omics–pathology co-registration in neurotoxicology to date: MSI found lipid/protein changes in CA1 → co-localized in the same region with H&E/IHC evidence of CA1 cell loss, mineralization, and astrogliosis → behavioral findings (learning and memory impairment) consistent with that region's function.■

### 5.4 Primary vs secondary: how to distinguish direct neurotoxicity from systemic toxicity

| Feature | Suggests **primary neurotoxicity** | Suggests **secondary/systemic** |
|---|---|---|
| Regional distribution | Lesions confined to specific nuclei/circuits (e.g. SNpc, CA1), consistent with drug/metabolite or target distribution | Lesions diffuse, multifocal, or confined to ischemia/hypoxia-sensitive areas (e.g. hippocampal CA1, watershed cortex) with no regional drug concentration gradient |
| Dose relationship | Neurological effects appear at doses below those causing systemic toxicity (weight loss, liver/kidney injury) | Neurological effects appear only at doses causing severe systemic toxicity, marked weight loss, hypoglycemia, or electrolyte disturbance |
| Temporal relationship | Functional/pathological changes coincide with or slightly lag the brain exposure peak; after dosing stops, recovery or persistence follows lesion reversibility | Neurological symptoms fluctuate in step with systemic toxicity (e.g. dehydration, hypoglycemia, infection); symptoms improve when systemic factors are corrected |
| Cell type | Specific cell types affected (e.g. dopaminergic neurons, Purkinje cells), with neighboring cells relatively spared | Neurons, glia, vessels, and myelin broadly affected, or predominantly vascular/edema |
| Mechanistic markers | Target occupancy/enzyme inhibition/transporter-substrate evidence positive in the affected region | No target evidence; lesions explainable by a known systemic mechanism (e.g. hypoglycemia causing hippocampal injury) |
| Species consistency | Same region affected across multiple species | Seen in only one species, which has a known systemic toxicity background (e.g. progressive nephropathy in rats) |

**Operating checklist:** Whenever a neurological lesion appears, simultaneously check body weight, food intake, clinical chemistry (glucose, electrolytes, liver/kidney function), body temperature, blood pressure/heart rate (if telemetry is available), and infection/inflammation markers; record the anesthesia and euthanasia method (see §6). **Do not attribute a lesion to direct neurotoxicity before systemic factors have been excluded.** ■

### 5.5 Cases: regional distribution patterns explaining specific neurotoxicity

#### Case A — MPTP: selective nigrostriatal injury (■ Established, textbook-level)

- **History:** In the early 1980s, a group of young meperidine users developed a syndrome clinically indistinguishable from Parkinson's disease, caused by the synthetic by-product MPTP.■
- **Regional distribution (PET + autoradiography):** After intravenous ¹¹C-MPTP, PET in rhesus monkeys showed **very rapid and high uptake of radioactivity in the striatum and midbrain (including the substantia nigra region), ~7–8× the homogeneous whole-brain distribution, with no clearance within 2 hours**; whole-body autoradiography in mice confirmed systemic distribution.■
- **Regional lesions:** Autopsy confirmed degeneration of pigmented neurons in the substantia nigra pars compacta (SNpc, A8/A9); monoamine measurements across 45 brain regions in rhesus monkeys showed **the most pronounced dopamine loss in the caudate, putamen, and substantia nigra**, with a characteristic regional pattern also in subcortical/brainstem dopamine, norepinephrine, and serotonin (subcortical/brainstem sensitivity ranking: dopamine > norepinephrine > 5-hydroxytryptamine).■
- **Mechanism (why this region):** MPTP itself does not directly kill neurons; its metabolite **MPP⁺** is actively taken up into dopaminergic neurons by the **dopamine transporter (DAT)**, where it inhibits mitochondrial complex I, causing selective death.■ Nigral neurons are rich in neuromelanin, and the melanin affinity of MPTP/MPP⁺ may lead to high intracellular concentrations — a hypothesis that could explain the particular vulnerability of SNpc neurons ◐. Species differences (primates sensitive, rodents relatively insensitive) suggest involvement of neuromelanin-related biochemical properties ◐.
- **Extended Fluoro-Jade findings:** After a single 50 mg/kg MPTP dose (i.p.) in mice, Fluoro-Jade showed degenerating neurons in the **midline and intralaminar thalamic nuclei** in addition to the SNpc, VTA, and posterior red nucleus (present in all dosed animals, independent of dosing ambient temperature); SNpc degeneration appeared only when dosing occurred in a cold environment (6 °C) — suggesting that **ambient/body temperature can alter the regional toxicity pattern of MPTP**.■ Pretreatment with deprenyl (a MAO-B inhibitor blocking MPTP→MPP⁺) or nomifensine (a DAT inhibitor) prevented both nigral and thalamic degeneration, supporting a shared DAT-dependent mechanism.■
- **Implication for medicinal chemists:** **Low whole-brain Kp of a compound does not mean it is safe** — if its metabolite is a substrate of DAT (or the norepinephrine/5-HT transporters), it can accumulate to toxic concentrations in specific nuclei. **Assess the transporter-substrate properties and regional accumulation of metabolites, not only the whole-brain Kp of the parent drug.**

#### Case B — BMAA (β-N-methylamino-L-alanine): selective hippocampal CA1 injury (■ Established in the rat model; human disease association is a hypothesis ○)

- **Exposure:** Neonatal rats dosed with BMAA on PND9–10 (an environmental neurotoxin produced by cyanobacteria, once thought to be linked to ALS/Parkinsonism–dementia complex — **the causal link to human disease has not been established** ○).
- **Regional distribution and lesions:** Neonatal exposure led to **selective hippocampal uptake**, with CA1 cell loss, mineralization, and astrogliosis in adulthood, accompanied by learning and memory impairment; CA1 protein ubiquitination increased, suggesting protein aggregation.■
- **Spatial omics co-registration:** ToF-SIMS and MALDI-MSI showed **elevated phospholipids and protein fragments in the lesioned CA1 region and phosphate depletion in the DG**; high-resolution SIMS showed specific localization of phosphatidylcholine lipids, protein signals, and potassium in the lesioned CA1; MALDI showed elevated phosphoethanolamine co-localized with protein lesions, suggesting an autophagy mechanism.■ Striatal MALDI-IMS showed **dose-dependent decreases in myelin basic protein (MBP) in the caudate-putamen and nucleus accumbens (150 and 460 mg/kg)**, confirmed by IHC, suggesting developmental exposure can affect axonal growth/oligodendrocyte proliferation and myelination.■
- **Implication:** The BMAA case demonstrates the complete chain of **"brief neonatal exposure → adult regional lesions → molecular changes localizable by spatial omics"** and is a model example of regional exposure–effect correlation in DNT research.■ But the causal link between BMAA and human neurodegenerative disease is **not established**; do not extrapolate rat CA1 lesions directly to human ALS/AD risk.○

#### Case C — H⁺/organic cation antiporter substrates: region-independent active uptake (◐ Emerging; mechanism–toxicity link not established)

- A 2024 *Front Cell Neurosci* study: pyrilamine, diphenhydramine, bupropion, tramadol, oxycodone, and memantine measured by CMA-ROI in rats showed **Kp,uu,ROI >1 in all brain regions** with no significant regional differences, suggesting **region-independent active uptake** mediated by the H⁺/OC antiporter.◐ The authors proposed that high intra-/extracellular concentrations may be related to neurotoxicity, but **the study did not prove that any drug's toxicity is mediated by this transporter** — it remains a hypothesis.○
- **Implication:** When Kp,uu,ROI is >1 in all regions, **regional differences in toxicity cannot be explained by regional concentration differences**; the explanation must shift to regional target expression, metabolism, and vulnerability. A negative regional PK result can equally narrow the hypothesis space.

#### Case D — DFP (diisopropyl fluorophosphate, an organophosphate nerve agent): timing and regional pattern of neuroinflammation (■ Established in the rat model)

- After a single 9 mg/kg DFP dose (i.p.) in adult male SD rats, moderate-to-severe status epilepticus appeared within minutes (lasting up to 6 hours); Iba1/GFAP IHC and TSPO PET ([¹¹C]-(R)-PK11195) showed **hippocampal and cortical neuroinflammation appearing within the first 3 days, peaking on day 7, and persisting to day 21**; Fluoro-Jade-B showed **neuronal degeneration in multiple brain regions (1–14 days after exposure)**, accompanied by Pavlovian conditioning cognitive impairment.■
- **Implication:** Neuroinflammation (Iba1/GFAP/TSPO) and neuronal degeneration (FJ) appearing in the **same regions and on the same timeline** support the chain "seizures → excitotoxicity → neuronal degeneration → glial response"; but whether **inflammation is cause or consequence** must be distinguished with anti-inflammatory/anti-seizure intervention experiments — correlation alone does not prove causation.◐

---

## 6. Practical Workflow

### 6.1 Step-by-step preclinical workflow

**Stage 0 — Hypothesis and literature (2–4 weeks)**
1. Define the question: Which brain region is the target in? Is the expected central effect efficacy or toxicity? Are CVOs relevant? Is there transporter-substrate risk?
2. Check regional expression of the target/transporter/metabolic enzymes in human brain atlases (Allen/Paxinos); check known regional neurotoxicity patterns of related compounds (e.g. MPTP, BMAA).
3. Write a **regional hypothesis table**: one row per brain region, listing expected concentration (high/medium/low), expected effect, and the test method. — This table is the basis for all subsequent sampling and analysis.

**Stage 1 — In vitro BBB and binding (2–4 weeks)**
4. PAMPA-BBB (passive permeability) → MDCK-MDR1 / MDCK-BCRP (ER, ± inhibitors) → hCMEC/D3 or co-culture models (Papp, TEER).

5. Measure fu,plasma and fu,brain (equilibrium dialysis); for strongly basic compounds, also measure brain slice Vu,brain.
6. **Decision point:** If ER is high (P-gp/BCRP substrate) and predicted Kp,uu <0.3, evaluate structural modification or accept low brain exposure; if predicted Kp,uu >1 (active uptake), evaluate uptake-transporter-mediated toxicity risk (see Case C).

**Stage 2 — In vivo distribution (rodents first)**
7. Single-dose PK: plasma + whole brain + **regional brain** (cortex, hippocampus, striatum, hypothalamus, cerebellum, brainstem, olfactory bulb, CVOs such as area postrema/choroid plexus sampled separately) by LC-MS/MS, at multiple time points (at minimum Tmax, Cmax, and the elimination phase).
8. **Perfusion vs no perfusion must be stated in the protocol and kept consistent**; if not perfused, residual blood correction is required (see §6.3).
9. Calculate Kp,brain, Kp,uu,brain (CMA method), and Kp,uu,ROI; compare with unbound plasma concentrations to judge whether target IC₅₀/EC₅₀ or toxicity thresholds are reached.
10. If spatial information is needed, choose either QWBA (regulatory) or MALDI-MSI (exploratory); **do not run both without a pre-specified statistical plan**.

**Stage 3 — Safety pharmacology (ICH S7A)**
11. Rodent CNS observational battery (Irwin test / simplified FOB) after a single dose, at therapeutic exposure and above; record functional changes at multiple time points after dosing.
12. If a CNS signal is positive, add motor activity, grip strength, body temperature, EEG, etc.

**Stage 4 — Repeat-dose toxicity + neurotoxicity**
13. Select species and duration per ICH M3(R2)/S4 (rodent + non-rodent); **routinely screen the brain** in repeat-dose toxicity studies (STP 6–7 levels, see §1.3).
14. If neurological signs, brain weight changes, or suspicious H&E lesions appear, **escalate to a dedicated TG 424 study** (FOB + motor activity + detailed neuropathology, ≥5/sex/group perfusion-fixed).
15. For developmental indications or a DNT signal, initiate **TG 426 or a TG 443 DNT cohort**.
16. **Longitudinal biomarkers:** Collect blood at baseline, mid-dosing, terminal, and recovery time points for NfL + GFAP (Simoa); a positive signal (>1.64-fold over baseline, referencing the Lanz 2025 ULN ◐) must be traced back to pathology and regional exposure.

**Stage 5 — Terminal necropsy (the most critical day — a written SOP and timetable are required)**
17. **The euthanasia method must be standardized and recorded** (see §6.3 on anesthesia effects); avoid hypoxia/hypercapnia from CO₂ altering brain metabolites.
18. **Timing:** The time from euthanasia to brain removal and the start of snap-freezing/perfusion must be recorded to the minute; post-mortem delay for MSI/omics samples should be **<3 minutes** (ideal) or at least consistent across groups and reported.■
19. **Split:** Follow the pre-allocation plan to split hemispheres/sections/animal subgroups: left hemisphere perfusion-fixed (pathology), right hemisphere fresh snap-frozen (LC-MS/MS/MSI/omics); or main-study animals for pathology and satellite groups for TK. **Do not decide the split on the day of necropsy.**
20. Brain weight (after cutting the spinal cord at a consistent level), gross observations (hemorrhage, edema, atrophy), and photographic archiving.

**Stage 6 — Bioanalysis and pathology (in parallel)**
21. LC-MS/MS: regional concentrations, plasma concentrations, CSF (if available); calculate Kp, Kp,uu, Kp,uu,ROI; apply residual blood correction.
22. Pathology: H&E initial screen → ENHP as needed (FJ, GFAP, Iba1, myelin stains); INHAND nomenclature, semi-quantitative scoring, blinded re-check.
23. MSI/spatial omics: co-register with adjacent-section H&E/IHC; report registration error and batch QC.

**Stage 7 — Correlation analysis**
24. Concentration–lesion scatter plots and correlation analyses for the **same animal, same region** (per animal, to avoid pseudoreplication).
25. Dose–response and time–response tables: mean concentrations and lesion incidence/severity means per dose group, per time point, per region.
26. PK-PD modeling: Cu,brain (or Cu,ROI) → effect (FOB score, FJ+ counts, GFAP area, NfL fold-change).
27. **Primary vs secondary assessment** (see the §5.4 checklist), written into the discussion section of the report — **do not report only positive conclusions**.
28. Human extrapolation: Use PBPK (LeiCNS-PK3.0) to predict human brain ECF concentrations, combined with human transporter expression differences, to assess clinical neurotoxicity risk and safety margins.

### 6.2 Recommended references and guidelines (by use case)

| Use case | Preferred sources |
|---|---|
| Regulations (neurotoxicity) | OECD TG 424 (1997), TG 426 (2007), TG 443; OECD Guidance Document on Neurotoxicity Testing Strategies and Methods |
| Regulations (drug safety) | ICH S7A (safety pharmacology), ICH S4 (chronic toxicity duration), ICH M3(R2) (nonclinical timing and scope), ICH S5(R3) (reproductive toxicity, if DNT is involved) |
| Sampling and pathology | Bolon et al. STP Position Paper, *Toxicol Pathol* 2013;41:1028–1048; RENI Revised Guides for Organ Sampling — BRAIN; INHAND CNS/PNS Nomenclature, *Toxicol Pathol* 2012; Bolon et al. Expanded Neurohistopathology Forum, *Toxicol Pathol* 2024 |
| Atlases | Paxinos & Watson Rat (7th ed.); Paxinos & Franklin Mouse (5th ed., 2022); Paxinos et al. Rhesus Monkey (4th ed., 2023); Allen Brain Atlas (mouse/human); MNI Macaque Atlas |
| Brain distribution / Kp,uu | Hammarlund-Udenaes et al., *Pharm Res* 2008, DOI 10.1007/s11095-007-9502-2; Loryan et al., *Pharm Res* 2022;39:1321–1341, DOI 10.1007/s11095-022-03246-6; Fridén et al. Brain Slice Method (*Fluids Barriers CNS* / Springer Protocols); CMA-ROI (*Front Cell Neurosci* 2024, DOI 10.3389/fncel.2024.1493644) |
| Imaging mass spectrometry | Hanrieder et al. Imaging Mass Spectrometry in Drug Development and Toxicology (review); Karlsson/Hanrieder BMAA series (*ACS Chem Neurosci* 2014; *Toxicol Sci* 2012) |
| Biomarkers | Lanz et al., *J Neurol* 2025;272:512, DOI 10.1007/s00415-025-13246-2 (NfL longitudinal ULN 1.64-fold); TransBioLine DINI working group (ongoing, ◐) |
| Comparative anatomy | Preuss, *J Cogn Neurosci* 1995;7:1–24 (PFC homology); Vertes et al. 2025, PMID 39879345 (two-stream hypothesis ◐); Kavoi & Jameela, *Int J Morphol* 2011;29:939–946 (olfactory bulb morphometry) |

### 6.3 Common pitfalls — checklist

| # | Pitfall | Consequence | Mitigation |
|---|---|---|---|
| 1 | **Residual blood not corrected** | Low Kp (<1) overestimated, potentially reversing the conclusion (the example of Kp 0.3 actually being 0.11 is from the §4 methodology sources ○ — derived by a vendor, not primary data, for warning purposes only) | Perfuse (ice-cold saline via the heart) or correct using vascular markers/hemoglobin; report perfusion status and the correction formula; brain residual blood is ~1–2% (**secondary-source estimate** ○, use your own laboratory's measured values) |
| 2 | **Post-mortem delay / post-mortem redistribution** | Metabolite degradation, drug diffusion from blood/high-concentration regions to low-concentration regions, protein/peptide degradation (severe degradation within 3 minutes in MSI ■) | Record timing to the minute; snap-freeze first; keep delays consistent across groups and report them; avoid prolonged room-temperature storage after death |
| 3 | **Perfusion fluid damaging the BBB** | High concentrations of vasodilators (e.g. 2% NaNO₂) can damage the BBB, altering FITC/Texas Red ratios and Kp (single MDPI 2024 study ◐); 100 mM NaNO₂ showed no significant effect | Use low-concentration/validated perfusion protocols; record perfusion fluid composition, flow rate, and pressure; validate with BBB integrity markers |
| 4 | **Fixatives interfering with mass spectrometry/omics** | Formalin cross-linking and paraffin polymers interfere with MSI; FFPE RNA is fragmented | Split by endpoint (see §1.3b); fresh snap-frozen tissue for MSI/omics; ethanol fixation or snap-freezing for RNA |
| 5 | **Anesthesia and euthanasia method** | Ketamine/xylazine vs CO₂ affect blood clotting, cerebral blood flow, BBB permeability, and metabolites (e.g. lactate, neurotransmitters) | Standardize and record the anesthetic, dose, and euthanasia method; keep consistent across groups; after CO₂ euthanasia, collect tissue rapidly |
| 6 | **Strain, sex, and age differences** | Brain size, transporter expression, behavioral baselines, and background lesions all vary with strain/sex/age | State strain, sex, and age/body weight ranges in the protocol; include both sexes; in DNT studies, mind developmental timing conversion |
| 7 | **Coordinates reused across species/strains** | Stereotaxic injections missing the target nucleus | Validate with dye/tracer in your own laboratory; use individual MRI registration (NHP/pig/dog) |
| 8 | **Whole-brain homogenate masking regional heterogeneity** | Regional high concentrations diluted by whole-brain averaging, missing regional toxicity | Regional sampling (at minimum cortex, hippocampus, striatum, cerebellum, brainstem, CVOs); MSI or regional LC-MS/MS |
| 9 | **CSF concentration substituted for brain parenchymal concentration** | Misjudged brain exposure | CSF is adjunctive only; brain tissue/microdialysis data are required (see §4.4) |
| 10 | **FOB/behavioral observer bias** | False positives/false negatives | Standardized conditions, blinding, training, historical control ranges |
| 11 | **Lesion scoring not blinded / not using INHAND nomenclature** | Not accepted by regulators, not comparable across studies | Initial screen unblinded, quantitative scoring blinded and re-checked; use INHAND terminology |
| 12 | **Interpreting single-point absolute NfL values** | Age and individual baseline variation causing false positives | Longitudinal, self-controlled, fold-change (>1.64-fold as ULN reference ◐); combined with pathology |
| 13 | **Over-extrapolating in vitro BBB models** | Treating MDCK/hCMEC/D3 ER/Papp as directly equivalent to in vivo Kp,uu | In vitro is for screening only; in vivo Kp,uu must be validated by microdialysis/CMA; note species differences |
| 14 | **Ignoring metabolites** | Parent Kp low, but a metabolite that is a transporter substrate accumulates in specific nuclei (e.g. MPP⁺) | Evaluate BBB permeability and transporter-substrate properties of major metabolites; QWBA cannot distinguish parent/metabolite, so supplement with LC-MS/MS |

---

## Could Not Verify / Open Questions

1. **Authoritative stereotaxic atlases for rabbit and dog:** No primary source was found for rabbit/dog stereotaxic coordinate atlases of equivalent standing to the Paxinos rat/mouse/rhesus atlases. For stereotaxic dosing in rabbit/dog, use individual MRI/anatomical landmarks and state this in the protocol.○
2. **Specific FDA guidances:** This report did not search FDA CNS-related guidances by indication/modality one by one (e.g. additional requirements for certain antiepileptics or opioids). Search the FDA Guidance database before IND/NDA submission.○
3. **Regulatory qualification status of NfL:** Qualification work in projects such as TransBioLine is still ongoing; regulatory acceptance of NfL as a biomarker of drug-induced neurological injury is **not yet established**, and it remains an exploratory endpoint.◐
4. **Direct measurement of human brain Kp,uu:** Human brain microdialysis data are extremely scarce (limited to neurosurgical/critically ill patients); human Kp,uu is mostly predicted by PBPK or inferred from PET, with large uncertainty.◐
5. **Quantitative anatomical data for the minipig brain:** The Göttingen minipig brain weight/volume figures (~69 g, 55×47×36 mm) come from a single study, and the sample size and age range were not fully reported in the abstract — check the full text before citing.◐
6. **Quality of sources for some figures:** Figures marked ○ in the text (e.g. brain residual blood 1–2%, MPTP TH+ neuron loss percentages, GLP-1 RA CVO distribution details) come from secondary/vendor sources or abstracts, with no primary full text seen — **do not use them directly in regulatory documents**; verify against primary sources first.
7. **What this report did not cover:** It did not search complete toxicology dossiers for specific compounds; it did not compile measured Kp,uu values for any compound (Kp,uu is compound-specific and must be checked against DMPK data compound by compound).

---

## Sources (URLs / DOIs, in order of citation in the text)

**Regulations and guidelines**
1. OECD Test No. 424: Neurotoxicity Study in Rodents. https://www.oecd.org/en/publications/test-no-424-neurotoxicity-study-in-rodents_9789264071025-en.html — PDF: https://www.oecd.org/content/dam/oecd/en/publications/reports/1997/07/test-no-424-neurotoxicity-study-in-rodents_g1gh2951/9789264071025-en.pdf
2. OECD Test No. 426: Developmental Neurotoxicity Study. https://www.oecd.org/en/publications/test-no-426-developmental-neurotoxicity-study_9789264067394-en.html
3. OECD Guidance Document on Mammalian Reproductive Toxicity Testing and Assessment, 2nd ed. (2026), OECD Series No. 446. https://one.oecd.org/document/ENV/CBC/MONO(2026)26/en/pdf
4. ICH S7A / S4 / M3(R2) — overview: https://basicmedicalkey.com/nonclinical-safety-assessment-an-introduction-for-statisticians/ ; S7A revision discussion: Valentin & Leishman, *Regul Toxicol Pharmacol* 2023;139:105368. http://www.afsacollaboration.org/wp-content/uploads/2026/01/Valentin-and-Leishman-2023-2000-2023-Over-two-decades-of-ICH-S7A_has-the-time-come-for-a-revamp.pdf

**Sampling and neuropathology**
5. Bolon B et al. STP Position Paper: Recommended Practices for Sampling and Processing the Nervous System (Brain, Spinal Cord, Nerve, and Eye) during Nonclinical General Toxicity Studies. *Toxicol Pathol* 2013;41:1028–1048. DOI: 10.1177/0192623312474865. https://pathexperts.com/wp-content/uploads/2023/10/Toxicol-Pathol-41-1028-2013-Position-Paper-on-Nervous-System-Sampling-Bolon-STP1.pdf
6. Revised guides for organ sampling and trimming in rats and mice: BRAIN (RENI). https://reni.item.fraunhofer.de/reni/trimming/manus.php?mno=005
7. DeFazio R et al. Neuroanatomy-based matrix-guided trimming protocol for the rat brain. *Toxicol Pathol* 2015;43:249–256. DOI: 10.1177/0192623314538345.
8. Proliferative and Nonproliferative Lesions of the Rat and Mouse CNS/PNS (INHAND). *Toxicol Pathol* 2012. DOI: 10.1177/0192623312439125. https://journals.sagepub.com/doi/10.1177/0192623312439125
9. Bolon B. Toxicologic Pathology Forum Opinion: Rational Approaches to Expanded Neurohistopathology Evaluation. *Toxicol Pathol* 2024. DOI: 10.1177/01926233231225239. https://journals.sagepub.com/doi/10.1177/01926233231225239
10. Nervous System Sampling for General Toxicity and Neurotoxicity Studies in the Laboratory Minipig, with Emphasis on the Göttingen Minipig. https://www.researchgate.net/publication/354068754_Nervous_System_Sampling_for_General_Toxicity_and_Neurotoxicity_Studies_in_the_Laboratory_Minipig_With_Emphasis_on_the_Gottingen_Minipig

**Atlases and comparative anatomy**
11. Paxinos G, Franklin KBJ. *Paxinos and Franklin's The Mouse Brain in Stereotaxic Coordinates*, 5th ed. Elsevier, 2022. https://www.elsevier.com/books/paxinos-and-franklins-the-mouse-brain-in-stereotaxic-coordinates/paxinos/978-0-12-816157-9
12. Paxinos G et al. *The Rhesus Monkey Brain in Stereotaxic Coordinates*, 4th ed. 2023. (Distributor page) https://www.numilog.com/LIVRES/ISBN/9780128158531.Livre
13. MNI Cynomolgus Macaque Atlas / Macaque Atlas. http://www.bic.mni.mcgill.ca/ServicesAtlases/Cyno ; Frey S et al. An MRI based average macaque monkey stereotaxic atlas and space (MNI monkey space). *NeuroImage* 2011. DOI: 10.1016/j.neuroimage.2011.01.040.
14. PRIME-RE Macaque templates & atlases (D99, NMT, SARM, CHARM). https://prime-re.github.io/templates_and_atlases_macaque.html
15. Allen Institute — Transcriptional Landscape of the Brain / Allen Brain Atlas. https://brain-map.org/our-research/gene-expression/transcriptional-landscape-of-the-brain ; https://alleninstitute.org/news/allen-institute-for-brain-science-completes-brain-atlas
16. Preuss TM. Do rats have prefrontal cortex? *J Cogn Neurosci* 1995;7:1–24. DOI: 10.1162/jocn.1995.7.1.1. https://direct.mit.edu/jocn/article-abstract/7/1/1/3142/Do-Rats-Have-Prefrontal-Cortex-The-Rose-Woolsey?redirectedFrom=fulltext
17. Vertes RP, Palomero-Gallagher N, Halassa MM. The Two Prefrontal Streams: Evidence for Homology Across Species. 2025. PMID: 39879345. DOI: 10.7551/mitpress/15679.003.0006. https://pubmed.ncbi.nlm.nih.gov/39879345/
18. Kavoi BM, Jameela H. Comparative morphometry of the olfactory bulb, tract and stria in the human, dog and goat. *Int J Morphol* 2011;29:939–946. https://www.scielo.cl/pdf/ijmorphol/v29n3/art47.pdf
19. Ellegaard Göttingen Minipigs — Background Data / Brain Atlas (CENSE, Aarhus). https://minipigs.dk/about-gottingen-minipigs/background-data
20. Meidahl AC et al. The Retrograde Connections and Anatomical Segregation of the Göttingen Minipig Nucleus Accumbens. *Front Neuroanat* 2016. DOI: 10.3389/fnana.2016.00117. https://www.frontiersin.org/journals/neuroanatomy/articles/10.3389/fnana.2016.00117/xml

**BBB, Kp,uu, and distribution methods**
21. Hammarlund-Udenaes M, Fridén M, Syvänen S, Gupta A. On the Rate and Extent of Drug Delivery to the Brain. *Pharm Res* 2008;25. DOI: 10.1007/s11095-007-9502-2. https://link.springer.com/content/pdf/10.1007/s11095-007-9502-2.pdf
22. Loryan I et al. Unbound Brain-to-Plasma Partition Coefficient, Kp,uu,brain — a Game Changing Parameter for CNS Drug Discovery and Development. *Pharm Res* 2022;39:1321–1341. DOI: 10.1007/s11095-022-03246-6. https://link.springer.com/content/pdf/10.1007/s11095-022-03246-6.pdf
23. Understanding the brain uptake and permeability of small molecules through the BBB: A technical overview. *Pharmaceutics* 2021. PMC: https://pmc.ncbi.nlm.nih.gov/articles/PMC8327119/
24. Muscle to Brain Partitioning as Measure of Transporter-Mediated Efflux at the Rat BBB. *Pharmaceutics* 2019;11:595. DOI: 10.3390/pharmaceutics11110595. https://pmc.ncbi.nlm.nih.gov/articles/PMC6920949/
25. The brain slice method for studying drug distribution in the CNS. https://www.springermedizin.de/the-brain-slice-method-for-studying-drug-distribution-in-the-cns/9680310
26. Characterization of a Primate Blood-Brain Barrier Co-Culture Model. *Pharmaceutics* 2021;13:1484. https://www.mdpi.com/1999-4923/13/9/1484/html
27. Blood-brain barrier / Circumventricular organs overview. https://derangedphysiology.com/main/cicm-primary-exam/nervous-system/Chapter-111/blood-brain-barrier
28. Bällgren F et al. Region-independent active CNS net uptake of marketed H+/OC antiporter system substrates. *Front Cell Neurosci* 2024. DOI: 10.3389/fncel.2024.1493644. https://www.frontiersin.org/journals/cellular-neuroscience/articles/10.3389/fncel.2024.1493644/xml
29. Optimization of Transcardiac Perfusion for More Accurately Evaluating Biodistribution of Large Molecules. *Int J Mol Sci* 2024;25:12180. https://www.mdpi.com/1422-0067/25/22/12180
30. Bruker — Targeted MALDI Imaging (QWBA vs MALDI). https://www.bruker.com/pl/applications/academia-life-science/imaging/maldi-imaging/targeted-maldiimaging-.html
31. QMSI vs QWBA infographic (Aliri Bio). https://aliribio.com/wp-content/uploads/2024/07/ALR_QMSI_vs_QWBA_Infographic-July2024.pdf

**Neurotoxicity cases and biomarkers**
32. Distribution of MPTP in experimental animals studied by PET and whole body autoradiography. *Life Sci* 1986. https://www.sciencedirect.com/science/article/abs/pii/0024320586902791
33. Burns RS et al. The Neurotoxicity of MPTP in the Monkey and Man. *Can J Neurol Sci* 1984;11:166–168. DOI: 10.1017/S0317167100046345. https://core-varnish-new.prod.aop.cambridge.org/core/services/aop-cambridge-core/content/view/2E4A9C0AEB29513EBF676FB1D272AB2A/S0317167100046345a.pdf/the-neurotoxicity-of-1-methyl-4-phenyl-1-2-3-6-tetrahydropyridine-in-the-monkey-and-man.pdf
34. Systemic administration of MPTP induces thalamic neuronal degeneration in mice. *Brain Res* 1997. https://www.sciencedirect.com/science/article/pii/S0006899397000450
35. Hanrieder J et al. High Resolution Metabolite Imaging in the Hippocampus Following Neonatal Exposure to BMAA Using ToF-SIMS. *ACS Chem Neurosci* 2014;5:568–575. DOI: 10.1021/cn500039b. https://research.chalmers.se/en/publication/?id=201609
36. Hanrieder J et al. Probing the lipid chemistry of neurotoxin-induced hippocampal lesions using multimodal imaging mass spectrometry. *Surf Interface Anal* 2014;46(Suppl 1):375–378. DOI: 10.1002/sia.5418. https://pmc.ncbi.nlm.nih.gov/articles/PMC5558446/
37. Karlsson O et al. Neonatal exposure to BMAA induces changes in protein expression and neurodegeneration in adult hippocampus. *Toxicol Sci* 2012;130:391–404. DOI: 10.1093/toxsci/kfs241.
38. Flannery BM et al. Persistent neuroinflammation and cognitive impairment in a rat model of acute diisopropylfluorophosphate intoxication. *J Neuroinflammation* 2016;13:267. PMID: 27733171. https://pubmed.ncbi.nlm.nih.gov/27733171/
39. Lanz TA et al. Longitudinal evaluation of serum neurofilament light levels in normal healthy volunteers: defining a threshold of concern. *J Neurol* 2025;272:512. DOI: 10.1007/s00415-025-13246-2. https://link.springer.com/content/pdf/10.1007/s00415-025-13246-2.pdf
40. Hanrieder J et al. Imaging mass spectrometry in drug development and toxicology (review). https://www.springermedizin.de/imaging-mass-spectrometry-in-drug-development-and-toxicology/50549520

**Methodology (fixation, LCM, spatial omics)**
41. Su A et al. Comparison of ethanol versus formalin fixation on preservation of histology and RNA in laser capture microdissected brain tissues. (Journal not verified — via ResearchGate): https://www.researchgate.net/publication/8514458_Comparison_of_ethanol_versus_formalin_fixation_on_preservation_of_histology_and_RNA_in_laser_capture_microdissected_brain_tissues
42. Immuno-laser capture microdissection of perfusion-fixed mouse brain tissue coupled to RNA-seq. *J Neurosci Methods* 2025. https://www.sciencedirect.com/science/article/abs/pii/S016502702500192X
43. Multimodal spatial omics: From data acquisition to computational integration. *Patterns* 2026. https://www.cell.com/patterns/fulltext/S2666-3899(26)00101-7

*Note: Fact-checking for this report was based on browser search (browser_search) result text on 2026-11-12; no live verification of every paywalled full text was performed. All statements marked ■ in the text are supported by the primary/guideline sources listed above; statements marked ◐/○ have their limitations explained in the text. Before regulatory submission, verify the current versions and original texts on the OECD/ICH websites.*
