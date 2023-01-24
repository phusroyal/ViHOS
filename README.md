# ViHOS: Vietnamese Hate and Offensive Spans Detection
This repository contains official implementation of the paper [*ViHOS: Vietnamese Hate and Offensive Spans Detection*]() accepted at the [EACL 2023]() Main Conference.

## Introduction
The rise in hateful and offensive language directed at other users is one of the adverse side effects of the increased use of social networking platforms. This could make it difficult for human moderators to review tagged comments filtered by classification systems.

To help address this issue, we present the ViHOS (**Vi**etnamese **H**ate and **O**ffensive **S**pans) dataset, the first human-annotated corpus containing 26k spans on 11k online comments.

Our goal is to create a dataset that contains comprehensive hate and offensive thoughts, meanings, or opinions within the comments rather than just a lexicon of hate and offensive terms.

We also provide definitions of hateful and offensive spans in Vietnamese comments as well as detailed annotation guidelines. Futhermore, our solutions to deal with *nine different online foul linguistic phenomena* are also provided in the [*paper*]() (e.g. Teencodes; Metaphors, metonymies; Hyponyms; Puns...).

We hope that this dataset will be useful for researchers and practitioners in the field of hate speech detection in general and hate spans detection in particular.

## Dataset statistics
![ViHOS statistics. Vocabularies size and comments length are calculated at the syllable level](images/vihos_stats.png)
*Fig 1. ViHOS statistics. Vocabularies size and comments length are calculated at the syllable level. In which, Ha/Off? stands for a hate (Ha) or offensive (Off).*
![Spans statistics](images/spans_stats.png)
*Fig 2. Spans quantity and length statistics.*

##