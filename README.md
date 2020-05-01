# iSarcasm: A Dataset of Intended Sarcasm

iSarcasm is a dataset of tweets, each labelled as either `sarcastic` or `non_sarcastic`.
Each `sarcastic` tweet is further labelled for one of the following types of ironic speech:

- sarcasm: tweets that contradict the state of affairs and are critical towards an addressee;
- irony: tweets that contradict the state of affairs but are not obviously critical towards an addressee;
- satire: tweets that appear to support an addressee, but contain underlying disagreement and mocking;
- understatement: tweets that undermine the importance of the state of affairs they refer to;
- overstatement: tweets that describe the state of affairs in obviously exaggerated terms;
- rhetorical question: tweets that include a question whose invited inference (implicature) is obviously 
  contradicting the state of affairs.

For each sarastic tweet, we also have:
  - an explanation, in English sentences, as to why it is sarcastic, and 
  - a rephrase that conveys the same meaning non-sarcastically.
Both have been provided by the author of the tweet.

iSarcasm contains 4,484 tweets, out of which 777 are labelled as sarcastic and
3,707 as non-sarcastic. You'll find two files, isarcasm_train.csv and isarcasm_test.csv,
each containing 80% and 20% of the examples chosen at random, respectively. Each line in a
file has the format `tweet_id,sarcasm_label,sarcasm_type`, 
where `sarcasm_type` are only defined for sarcastic tweets,
as specified above.

While we only make the tweet IDs public, we maintain and are happy to provide the following
for research purposes, under an agreement that protects the privacy of our users:

- tweet texts;
- for each sarcastic tweet, an explanation given by its authors as to why the tweet is sarcastic;
- for each sarcastic tweet, a rephrase given by its author that conveys the same message non-sarcastically.

What sets iSarcasm apart from other datasets is the fact that the labels have been provided by the
authors of the tweets themselves. The labels therefore reflect the sarcastic intention of the authors, 
eliminating the noise that previous labelling methods such as manual labelling and tag-based distant 
supervision can induce, considering the subjective nature of sarcasm. The dataset was also subjected 
to strict quality control and a further verification by a human trained linguistics.

Full details about the data collection steps, as well as the performance of state-of-the-art sarcasm 
detection models of iSarcasm, is reported in the paper, with extra details in the supplement. The paper will appear at ACL 2020 and can be cited as follows:

@InProceedings{oprea-magdy:2020:isarcasm,
  title={iSarcasm: A Dataset of Intended Sarcasm},
  author={Oprea, Silviu and Magdy, Walid},
  booktitle = "Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics",
  year = "2020",
  publisher = "Association for Computational Linguistics",
}

For now, you can find a draft at https://arxiv.org/abs/1911.03123.
