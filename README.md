# Question_Answering_SQUAD

Stanford Question Answering Dataset (SQuAD) is a reading comprehension dataset, consisting of questions posed by crowdworkers on a set of Wikipedia articles, where the answer to every question is a segment of text, or span, from the corresponding reading passage, or the question might be unanswerable.
<br>
So I am planning to try various combinations of Question Answer generation models like ALBERT, ELECTRA along with the ensembles like Retro-Reader, nlayers, DAAF, verifiers and SA-Net models which are currently on the leader boards and experiment the combinations that has not yet been tested. 

# Implementation on Baseline Models

## ALBERT
ALBERT (https://arxiv.org/pdf/1909.11942.pdf) is a variant of BERT which lighter i.e less number of parameters and can be trained faster. It was released in ICLR 2020 by Google and performed better on datasets like SQUAD, GLUE and RACE than BERT. Currently it ranks 30 in the SQUAD competition but most of its ensembles are currently in the leaderboard and hence took it as a baseline model.

## ELECTRA

ELECTRA (https://arxiv.org/pdf/2003.10555.pdf) is another model which is released by Google and Stanford. It works very similar to GANs where there is one Generator which is capable of generating fake images and Discriminator which classifies the given image is genuine/fake and both are trained till Generator generates so genuine looking image that discriminator is not able to differentiate. Here in ELECTRA, the words are not masked like in BERT but some tokens from the original text are corrupted by replacing it with plausible alternate words genenrated from a small genenrator and the discriminator predicts that the each token from the corrupted text was replaced by small generator or not. ELECTRA outperformed ALBERT on Squad by getting the EM (Exact Match) score of 89.7. I am considering it as another baseline as its ensembles are also in the leaderboard.

# Ensembles

After implementing the baselines like ALBERT and ELECTRA, the plan is to explore various ensemble techniques like implementing Verifier, Retro Reader, DAAF along with models like ALBERT, RoBerta, ELECTRA and try out various combinations of the techniques to check the EM and F1 score of each combination and if any combination has the ability to reach to the leaderboards. Currently I am resarching on various techniques and will release the code soon.
