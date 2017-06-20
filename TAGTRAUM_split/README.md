# TAGTRAUM_split

Tagtraum split that I've used for my experiments in the paper [Multi-Level and Multi-Scale Feature Aggregation Using Pre-trained Convolutional Neural Networks for Music Auto-tagging, IEEE SPL(to be published), 2017](https://arxiv.org/abs/1703.01793).

This is stratified split with 80% training data of CD2C version of [Tagtraum genre annotations](http://www.tagtraum.com/msd_genre_datasets.html).<br> 
We then filtered the list so that the audio of all the songs in the list can be longer than 29.1 seconds.

# Split example:
In python, by using these commands we can simply use given data.
<pre><code>
import cPickle as cP
train_list = cP.load(open('train_list.cP','r'))
valid_list = train_list[141372:]
train_list = train_list[0:141372]
test_list = cP.load(open('test_list.cP','r'))
</code></pre>
