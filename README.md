# ReqEval: the shared task on anaphora ambiguity detection and disambiguation 

This repo contains the annotated dataset that was generated as a part of the shared task introduced in the third workshop on Natural Language Processing for Requirements Engineering. 

The dataset is comprised of 200 requirements statements (at a sentence-level). The requirements are orignated from seven distinct domains: spacecraft, diagnostic, digital home, digital library repository management, weather, archive file manipulation and railway.

The requirements are selected from a publicly available repository of requirements specifications~\cite{ferrari:17}. 

The dataset was prepared by five annotators with a background in RE and/or linguistics. Each requirement was analyzed by two different annotators. The annotators would first label each pronoun in the requirement as ambiguous or unambiguous and then suggest the likely disambiguation in the case of unambiguous.  

Each pronoun occurrence in the dataset is marked as nocuous if (i) at least one of the annotators labels it as ambiguous; or (ii) the two annotators disagreed on the likely disambiguation. All pronoun occurrences that received the same interpretation from both annotators are marked as innocuous. 
The annotation process resulted in 103 ambiguous requirements. 

We split the dataset into two thirds used for training and development (training or development set -- training.tsv), and one third left out for the final evaluation (test set -- test.tsv file). To examine the impact of training on one domain and testing on another, all of the requirements of the digital home are used for training whereas all of the requirements in the diagnostic and archive domains are used for testing. The requirements in the four remaining are then split randomly with stratification over the label (nocuous versus innocuous).  

More details about the task can be found at: https://nlp4re.github.io/2020/reqeval.html

