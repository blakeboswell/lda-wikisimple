## LDA Model of Simplewiki English


### Data Preparation

The simplewiki articles were obtained from [Wikimedia](https://dumps.wikimedia.org/simplewiki/latest/)

``` bash
curl https://dumps.wikimedia.org/simplewiki/latest/simplewiki-latest-pages-articles.xml.bz2 -o simplewiki-latest-pages-articles.xml.bz2
```

The [wikiextractor](http://attardi.github.io/wikiextractor/) python script was then used to convert the simplewiki dump from xml to text.

``` bash
# python 2.7
python WikiExtractor.py -o <extract-output-foldername> simplewiki-latest-pages-articles.xml.bz2
```

Finally, the simplewiki text files are transformed to jsonl files. This step is not absolutely neccesary but doing so helps maintain consisteny across my nlp pipelines.  This transformation takes place in the `merge.py` [script](https://github.com/blakeboswell/nlp-newsgroup/blob/master/merge.py) available within this repository.


``` python
from merge import merge_simplewiki
merge_simplewiki('<extract-output-foldername>', '<jsonl-foldername>')
```


### Analysis

 `under construction`
