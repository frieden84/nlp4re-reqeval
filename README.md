# ReqEval: The shared task on anaphora ambiguity detection and disambiguation 

This repo contains the annotated dataset that was generated as a part of the shared task introduced in the third workshop on Natural Language Processing for Requirements Engineering. 

More details about the task can be found at: https://nlp4re.github.io/2020/reqeval.html.

## Dataset Details 
The dataset is comprised of 200 requirements statements (at a sentence-level). The requirements are orignated from seven distinct domains: spacecraft, diagnostic, digital home, digital library repository management, weather, archive file manipulation and railway.

The requirements are selected from a publicly available repository of requirements specifications at https://zenodo.org/record/1414117#.X_28LS1h2M4. 

The dataset was prepared by five annotators with a background in RE and/or linguistics. Each requirement was analyzed by two different annotators. The annotators would first label each pronoun in the requirement as ambiguous or unambiguous and then suggest the likely disambiguation in the case of unambiguous.  

Each pronoun occurrence in the dataset is marked as nocuous if (i) at least one of the annotators labels it as ambiguous; or (ii) the two annotators disagreed on the likely disambiguation. All pronoun occurrences that received the same interpretation from both annotators are marked as innocuous. 
The annotation process resulted in 103 ambiguous requirements. 

We split the dataset into two thirds used for training and development (training or development set -- *training.tsv*), and one third left out for the final evaluation (test set -- *test.tsv*). To examine the impact of training on one domain and testing on another, all of the requirements of the digital home are used for training whereas all of the requirements in the diagnostic and archive domains are used for testing. The requirements in the four remaining are then split randomly with stratification over the label (nocuous versus innocuous).  

The files provided in this repo are tab-separated. Each file contains four different columns: 
- *ID*: a unique identifier representing each pronoun occurrence
- *Sentence*: the sentence where the pronoun is tagged with 'referential'
- *Detected as*: the detection result whether this occurrence is nocuous or innocuous
- *Disambiguated as*: the disambiguation result when applicable  

## Annotators Details
This dataset has been created and annotated by: 
- Sallam Abualhaija, University of Luxembourg 
- Fabiano Dalpiaz, Utrecht University
- Alessio Ferrari, CNR-ISTI 
- Xavier Franch, Polytechnic University of Catalonia
- Davide Fuccie, Blekinge Institute of Technology

## License
This dataset is licensed under a Creative Commons Attribution 4.0 International License. **Disclaimer: The data was found online and, since it refers to old/completed projects and it was made publicly available, we therefore assume the dataset is not infringing copyright.**
