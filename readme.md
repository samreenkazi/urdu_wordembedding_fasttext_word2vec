####Urdu Word Embeddings

 we have traind the skip-gram model using word2vec and fasttext on top of   different urdu sources;
 Tweets, News Articles, Latest Wikipedia Urdu dump, and publicly availble corpora. The total number of tokens used to build the model amount to more than 132,246,587 Urdu words to create the large-scale word embeddings for the Urdu language..

##Download:

Models can be downloaded from following link

https://drive.google.com/open?id=1sKD1ioXrXV6HMi4B6fGfjrRE6tOSDq0k

Skip-gram model trained with word2vec : ur_wiki_fasttext_300.rar

Skip-gram model trained with fasttext : wiki.ur.vector.rar

##Usage:

Extract the archive and use Python and Gensim to read the embeddings:

from gensim.models import word2vec

model = gensim.models.KeyedVectors.load_word2vec_format('wiki.ur.vector.bin', binary=True)

model=  gensim.models.KeyedVectors.load_word2vec_format(ur_wiki_fasttext_300.bin, binary=True)

##Evaluate:

print(model.most_similar('پاکستان'))

##Result:


[('پاکستا', 0.7276749014854431), ('اورپاکستان', 0.7151240110397339), ('کستان', 0.5933041572570801), ('پنجاب', 0.5784835815429688), ('پاکستانی', 0.5677152872085571), ('پاکستانیوں', 0.5271217823028564), ('بلوچستان', 0.5172491073608398), ('سرائیکستان', 0.5115364193916321), ('بھارت', 0.508114218711853), ('سندھ', 0.5026125907897949)]
