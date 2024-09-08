# Introduction
This repository contains the data and code associated with the manuscript [A Pipeline for the Automatic Identification of Randomized Controlled Oncology Trials and Assignment of Tumor Entities Using Natural Language Processing](https://www.medrxiv.org/content/10.1101/2024.07.09.24310155v1) which is currently available as a preprint while undergoing peer review.
The config file can be used to train a model using the spacy/prodigy packages. 

# Data
Each trial is a row in the csv file. For each trial there are the follwing columns:
- __doi__: Digital Object Identifier of the publication
- __date__: Publication data according to PubMed
- __journal__: Journal the publication was published in according to PubMed
- __abstract__: The abstract of the publication
- __text__: The text that was displayed to the annotator.
- __accept__: Contains "accept" if an annotator annotated the publication.
- __answer__: The labels that the annotator assigned. Publications that described randomized controlled trials (RCTs) received the label “RCT”. Publications that covered oncological topics received the label “ONCOLGY”. Trials that fulfilled both criteria were assigned both labels. Trials that were neither RCTs nor covered oncology topics were assigned no label.
- __options__: List of labels that the annotator could select
- **_input_hash**, **_task_hash**, **_view_id**, **config**, **_timestamp**, **_annotator_id**, **_session_id**: Additional columns automatically created by the annotation tool during the annotation process. For detailed documentation see the [prodigy docs](https://prodi.gy/docs/api-components).

The dataset has also been uploaded to [Dryad](https://doi.org/10.5061/dryad.gb5mkkx00).
