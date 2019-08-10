# IPRE
IPRE: a Dataset for Inter-Personal Relationship Extraction

## Dataset/Format
|**Files**|**Contents**|
|:------|:------|
|sent_train/dev/test|sentID &ensp; instance|
|sent_relation_train/dev/test|sentID &ensp; relationIDs|
|bag_relation_train/dev/test|bagID &ensp; e<sub>h</sub> &ensp; e<sub>t</sub> &ensp; sentIDs &ensp; relationIDs|

The above table shows the format of our data set. Some keywords are explained as follows:
* e<sub>h</sub> &emsp; The head entity in the sentence.
* e<sub>t</sub> &emsp; The tail entity in the sentence.
* instance &emsp; An instance consists of a ordered entity pair and a sentence, which segmented by the [Jieba](https://github.com/fxsjy/jieba)
* sentID &emsp; A unique ID given to an instance.
* bagID  &emsp; A unique ID given to a bag, and all setences in a bag contains the same entity pair.
* relationID &emsp; A unique ID given to a relation type.

Note that the part represented by the keywords mentioned above is separated by a tab character.
Moreover, *relationIDs* is composed of several *relationID* that separated by a space character, and *sentIDs* is also so.

## Dataset/Files
Each dataset contains three files, in which one file stores the mapping information between *sentID* and *instance*, and the remaining two files store the data in dataset at sentence-level and bag-level respectively.

For example, test set contains ``sent_test.txt``, ``sent_relation_test.txt`` and ``bag_relation_test.txt``.
The mapping information between *sentID* and *instance* in test set is stored in ``sent_test.txt``, and the data in test set at sentence-level and bag-level are stored in ``sent_relation_test.txt`` and ``bag_relation_test.txt`` respectively.


## Reference

If you use the IPRE data, please cite the following paper:
* Haitao Wang, Zhengqiu He, Jin Ma, Wenliang Chen, Min Zhang. 2019. IPRE: a Dataset for Inter-Personal Relationship Extraction. https://arxiv.org/abs/1907.12801
