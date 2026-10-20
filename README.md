# NYCU NLP Lab

**Natural Language Processing Lab, Department of Computer Science, National Yang Ming Chiao Tung University, Hsinchu, Taiwan**
Principal investigator: An-Zi Yen (顏安孜)

Website: https://nycu-nlp-lab.github.io/ · GitHub: https://github.com/NYCU-NLP-Lab · YouTube: https://www.youtube.com/@NYCU_NLP_Lab

> AI that reasons, adapts, and works with people.

We build personalized, trustworthy, and efficient AI that brings together multimodal perception, knowledge, and reasoning to support people in daily life. Our work sits at the intersection of natural language processing and information retrieval, and much of it is now about personal AI assistants that see, listen, and know when to act.

## Research directions

Four questions we keep coming back to, with one goal: AI that understands people and the world they live in, and helps them well.

**Multimodal understanding & situated intelligence** (flagship theme)
How can AI integrate what it sees, hears, and reads to understand an environment, an event, and what the user needs right now?
Representative work: EgoArgus, VISTA.

**Personalization & adaptive intelligence**
How can AI use personal knowledge and interaction history to adapt to each user and each task?
Representative work: PersonaEdit, RSVP, E-QGen, ISSR.

**Trustworthy reasoning & assistance**
How can AI reason from evidence and give help that is understandable, checkable, and appropriate?
Representative work: RefuteClaim, MAGIC, MathEDU, evidence recommendation for financial legal resolutions.

**Efficient & resource-aware AI**
How can AI allocate models and data to what a task needs, balancing quality against cost?
Representative work: VDAR-Router, confidence-driven model selection, representative sample selection for model editing.

## Flagship series: situational assistants

A personal AI assistant that lives in your point of view has to do three things at once: understand the scene, listen to the person, and decide whether stepping in would help or get in the way. This series builds the benchmarks, the data, and the systems for that judgment.

- **EgoArgus** (EMNLP 2026). A human-annotated benchmark of dialogue-video scenarios that tests whether vision-language models can arbitrate between what they see and what the user says, and decide whether to intervene. It measures two capabilities: understanding (multiple-choice reasoning under multimodal, contradictory, off-topic, on-topic, and text-grounded conditions) and decision (whether to intervene, when, and which assistance steps to give). The release contains 7,767 examples (6,978 understanding, 789 decision) and 311 decision videos. Current VLMs still struggle to arbitrate between modalities, and existing bias-mitigation methods help only within narrow limits. [Paper](https://arxiv.org/abs/2608.25561) · [Dataset & code](https://github.com/NYCU-NLP-Lab/EgoArgus) · [Videos](https://huggingface.co/datasets/tommytyc/EgoArgus)
- **VISTA** (EMNLP 2026 Demo). Rare or risky assistance situations are hard, costly, or unsafe to film. VISTA turns a one-line scenario seed into an editable plan, an egocentric video, and an auditable review trail, with an approval gate at each step. The platform ships 14 reviewed demonstrations across reactive, explicit proactive, and implicit proactive help, in safety-critical and everyday settings, plus matched cases where the right answer is to stay quiet. [Paper](https://arxiv.org/abs/2605.10579) · [Platform](https://nlplab-vista-research-vista-demo.hf.space/platform)

The series page (https://nycu-nlp-lab.github.io/assistants.html) has the timeline, real EgoArgus decision videos that you can replay with different user utterances, and the VISTA demonstrations.

## Featured research

Each of these has an interactive explainer on the website, under "Play with the idea".

- **EgoArgus: Benchmarking VLMs as Situational Assistants** (EMNLP 2026). An assistant sees your kitchen and hears you say "the stove is off." Which one should it believe? When the camera and the user disagree, can the model tell which modality is trustworthy and decide whether to step in at all?
- **VDAR-Router: Adaptive LLM Routing via Verbalized Query Difficulty** (EMNLP 2026 Findings). Two queries can use the same words and still be worlds apart in difficulty. VDAR-Router first writes out an explicit difficulty analysis, retrieves past queries with a similar difficulty profile, and uses their outcomes to pick the model that balances cost and quality.
- **PersonaEdit: Representative Sample Selection for Personalized Model Editing** (EMNLP 2026 Findings). A user has told the model hundreds of things about themselves. Which few should be written into its weights? PersonaEdit clusters the hidden representations of a user's data and picks representative samples by proportional stratified sampling, which makes model editing an effective route to personalization.
- **MathEDU: Feedback Generation on Problem-Solving Processes** (EACL 2026). A student's answer is wrong. Where did the reasoning go off track, and what should the teacher say? MathEDU pairs real student problem-solving processes with teacher-written feedback and evaluates models on three tasks: is the answer correct, which step is wrong, and what feedback would help.
- **How We Refute Claims: Fact-Checking through Flaw Identification** (WWW 2024). "False" is not an explanation. RefuteClaim generates the aspects a claim should be judged on, identifies the flaw under each aspect, and explains the verdict. FlawCheck, our dataset, distills expert fact-checker reviews into aspects and flaws.

## Selected publications

Lab publications since 2022, newest first. The full list, filterable by research area, is on the website.

- Yu-Chien Tang, Yu-Hsiang Liu, and An-Zi Yen. EgoArgus: Benchmarking VLMs as Situational Assistants for Modality-Grounded User Supports. EMNLP 2026. https://arxiv.org/abs/2608.25561
- Yu-Hsiang Liu, Yu-Chien Tang, and An-Zi Yen. VISTA: A Controllable Platform for Generating and Auditing Egocentric Assistance Scenarios. EMNLP 2026 Demo. https://arxiv.org/abs/2605.10579
- Yu-Chien Tang, Jun-Chen Hung, Wen-Chih Peng, and An-Zi Yen. VDAR-Router: Adaptive LLMs Routing via Verbalized Query Difficulty Analysis Retrieval. EMNLP 2026 Findings. https://arxiv.org/abs/2607.18098
- You-Mei Huang, Chung-Chi Chen, and An-Zi Yen. PersonaEdit: Representative Sample Selection for Personalized Model Editing. EMNLP 2026 Findings. https://arxiv.org/abs/2608.27816
- Wei-Ling Hsu, Yu-Chien Tang, and An-Zi Yen. MathEDU: Feedback Generation on Problem-Solving Processes for Mathematical Learning Support. EACL 2026. https://arxiv.org/abs/2505.18056
- Bo-Wei Chen, Chung-Chi Chen, and An-Zi Yen. Confidence-Driven Multi-Scale Model Selection for Cost-Effective NLU. EACL 2026 Findings. https://arxiv.org/abs/2602.22090
- Yu-Cheng Liu and An-Zi Yen. Iterative Selection with Self-Review for Vocabulary Test Distractor Generation. ACML 2025. https://openreview.net/forum?id=X6Gr7CHO2y
- Mao-Siang Chen and An-Zi Yen. E-QGen: Educational Lecture Abstract-based Question Generation System. IJCAI 2024 Demo. http://arxiv.org/abs/2404.13547
- Wei-Yu Kao and An-Zi Yen. MAGIC: Multi-Argument Generation with Self-Refinement for Domain Generalization in Automatic Fact-Checking. LREC-COLING 2024.
- Wei-Yu Kao and An-Zi Yen. How We Refute Claims: Automatic Fact-Checking through Flaw Identification and Explanation. WWW 2024. https://arxiv.org/abs/2401.15312
- An-Zi Yen and Wei-Ling Hsu. Three Questions Concerning the Use of Large Language Models to Facilitate Mathematics Learning. EMNLP 2023 Findings. https://aclanthology.org/2023.findings-emnlp.201/

## Systems and demos

Demo systems built by lab members. Short videos of each are on the website and on the lab's YouTube channel.

- **ISSR** (ACML 2025): LLMs for vocabulary test distractor generation with iterative selection and self-review.
- **E-QGen** (IJCAI 2024 Demo): educational lecture abstract-based question generation.
- **MAGIC** (LREC-COLING 2024): multi-argument generation with self-refinement for domain generalization in fact-checking.
- **RefuteClaim** (WWW 2024): automatic fact-checking through flaw identification and explanation.
- **MathEDU** (EMNLP 2023): LLMs and the future of mathematics education.
- **金融消費者權益領航員** (2024 法律 × 法遵科技黑客松, 理律學堂跨領域特別獎): NLPFIN × NYCU-NLP, refining financial consumer complaints.

## People

**An-Zi Yen (顏安孜)**, Principal Investigator. Assistant Professor, Department of Computer Science, National Yang Ming Chiao Tung University. Her research interests include natural language processing and information retrieval. Her work has been published in AAAI, EMNLP, WWW, SIGIR, and CIKM. She received the Honorable Mention of the ACLCLP Doctoral Dissertation Award in 2020 and was a distinguished PC member at IJCAI 2023. [Personal page](https://azyen0522.github.io/) · [Google Scholar](https://scholar.google.com.tw/citations?user=QL-GNDQAAAAJ)

**PhD students:** Yu-Chien Tang, Yen-Shyun Huang.

**Master's students:** You-Mei Huang, Hsiang-Yu Cheng, Ding-Xin Kang, Nien-Hui Huang, Yong-Xuan Zheng, Wei-Lin Wen, Ting-Shian Kuo, Lai-Sen Cao, Hong-Yuan Cheng, Yi-Fu Chen, Wei-Chia Chang, Min-Quan Wang, Tun-Chieh Yang, Chun-Ting Hou.

**Alumni:** Yu-Hang Deng, Bo-Cheng Pan, Min-Kuang Tsu, Yu-Tung Chou, Chun-Wei Kang, Guan-Yi He, Wei-Ling Hsu, Yu-Cheng Liu, Bo-Wei Chen, Cheng-Xin Song, Hsiu-Hung Lee, Yen-Chun Huang, Yu-Chen Kang, Jou-Chia Chiang.

## Join us

Master's and PhD students: read a recent paper from the area you like, then write to us with what you would do next.

Contact: azyen@nycu.edu.tw · Department of Computer Science, National Yang Ming Chiao Tung University, Hsinchu, Taiwan

## Credits

The decision videos on the website come from the public EgoArgus dataset and were generated with VISTA. The dialogue, reviewed decisions, intervention times, and assistant messages shown with them are taken verbatim from the released annotations. The VISTA clip and posters are from the public VISTA demonstration platform.
