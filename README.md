# BPersona-chat

This repository contains the Japanese–English bilingual chat corpus BPersona-chat published in the paper [Chat Translation Error Detection for Assisting Cross-lingual Communications](https://aclanthology.org/2022.eval4nlp-1.9/) at [AACL-IJCNLP 2022](https://www.aacl2022.org/)'s Workshop [Eval4NLP 2022](https://eval4nlp.github.io/2022/index.html).

BPersona-chat is an evaluation dataset based on the English multiturn chat corpus [Persona-chat](https://arxiv.org/abs/1801.07243) and the Japanese multiturn chat corpus [JPersona-chat](https://arxiv.org/abs/2109.05217).

Each chat was performed between two crowd workers assuming artificial personas.
The speakers discuss a given personality trait, including but not limited to self-introduction, hobby, and others.
(Notice that they are not translations of each other.)

Chats are translated into Japanese/English by professional translators, a low-quality machine translation model A and a high-quality machine translation model B.

Translations are evaluated by crowdworkers as either good or bad, depending on the correctness and coherence.

Each chat is included in one .xlsx file with the following structure:
* **person** - the speaker on the current utterance,
* **source** - the utterance in the source language,
* **translation** - the translation in the target language,
* **evaluation: is this a good translation?** - the evaluation of the translation's quality,
  - y - the current translation is a correct translation of the source utterance,
  - n - the current translation is an erroneous translation of the source utterance.

Chats are included in:

    ├── en-ja ···················· English chats with Japanese translations and labels
    │   ├── human ················ chats translated by professional human translators
    │   │   ├── 0011.xlsx ········ * 200 files in total, the filenames are not continued *
    │   │   ├── ... ...
    │   │   └── 1495.xlsx
    │   ├── nmt-model-a ·········· chats translated by the low-quality nmt model A
    │   │   ├── 0011.xlsx
    │   │   ├── ... ... 
    │   │   └── 1495.xlsx
    │   └── nmt-model-b ·········· chats translated by the low-quality nmt model B
    │       ├── 0011.xlsx
    │       ├── ... ...
    │       └── 1495.xlsx
    └── ja-en ···················· Japanese chats with English translations and labels
        ├── human ················ chats translated by professional human translators
        │   ├── 0001.xlsx ········ * 250 files in total, the filenames are continued *
        │   ├── ... ...
        │   └── 0250.xlsx
        ├── nmt-model-a ·········· chats translated by the low-quality nmt model A
        │   ├── 0001.xlsx
        │   ├── ... ...
        │   └── 0250.xlsx
        └── nmt-model-b ·········· chats translated by the low-quality nmt model B
            ├── 0001.xlsx
            ├── ... ...
            └── 0250.xlsx

# License
Shield: [![CC BY-NC 4.0][cc-by-nc-shield]][cc-by-nc]

This work is licensed under a
[Creative Commons Attribution Non Commercial No Derivatives 4.0 International License][cc-by-nc].

[![CC BY-NC 4.0][cc-by-nc-image]][cc-by-nc]

[cc-by-nc]: https://creativecommons.org/licenses/by-nc/4.0/
[cc-by-nc-image]: https://licensebuttons.net/l/by-nc/4.0/88x31.png
[cc-by-nc-shield]: https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg

For detailed information, please check [LICENSE](LICENSE).


# Citation
If you use this please cite:

Yunmeng Li, Jun Suzuki, Makoto Morishita, Kaori Abe, Ryoko Tokuhisa, Ana Brassard, and Kentaro Inui. 2022. Chat Translation Error Detection for Assisting Cross-lingual Communications. In Proceedings of the 3rd Workshop on Evaluation and Comparison of NLP Systems, pages 88–95, Online. Association for Computational Linguistics.

    @inproceedings{li-etal-2022-chat,
        title = "Chat Translation Error Detection for Assisting Cross-lingual Communications",
        author = "Li, Yunmeng  and
          Suzuki, Jun  and
          Morishita, Makoto  and
          Abe, Kaori  and
          Tokuhisa, Ryoko  and
          Brassard, Ana  and
          Inui, Kentaro",
        booktitle = "Proceedings of the 3rd Workshop on Evaluation and Comparison of NLP Systems",
        month = nov,
        year = "2022",
        address = "Online",
        publisher = "Association for Computational Linguistics",
        url = "https://aclanthology.org/2022.eval4nlp-1.9",
        doi = "10.18653/v1/2022.eval4nlp-1.9",
        pages = "88--95",
    }

and,

Hiroaki Sugiyama, Masahiro Mizukami, Tsunehiro Arimoto, Hiromi Narimatsu, Yuya Chiba, Nakajima, and Toyomi Meguro. 2021. Empirical analysis of training strategies of transformer-based japanese chit-chat system.

    @misc{sugiyama2021empirical,
          title={Empirical Analysis of Training Strategies of Transformer-based Japanese Chit-chat Systems}, 
          author={Hiroaki Sugiyama and Masahiro Mizukami and Tsunehiro Arimoto and Hiromi Narimatsu and Yuya Chiba and Hideharu Nakajima and Toyomi Meguro},
          year={2021},
          eprint={2109.05217},
          archivePrefix={arXiv},
          primaryClass={cs.CL}
    }
    
Thank you for your cooperation.