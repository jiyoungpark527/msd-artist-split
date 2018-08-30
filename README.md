## Description
This dataset split contains 20 track_ids of each artist for 17,591 artists. We filtered out 20 songs for each
artist which are randomly selected including various albums to prevent recording environment effects.
- This data consists of `7Digital_id/artist_index/song_index`.

## Usage
- In python 3.6.1,
  ```
  import pickle
  import numpy as np

  def load_label(num_artist, train_size=15, valid_size=18, test_size=20):

      file_list = pickle.load(open('msd-artist-list.pkl','rb'))
      file_list = file_list[:num_artist*20]  # Cut as many artists as you want to use.
      np.random.shuffle(file_list)

  ... 
  ```
- `train_size=15, valid_size=18, test_size=20` means that we used 1-15 songs for training, 16-18 songs for validation and 19-20 songs for testing of each artist.

## This dataset split was used in following works:
- **Representation Learning of Music Using Artist Labels** [[pdf](https://arxiv.org/abs/1710.06648), [code](https://github.com/jongpillee/ismir2018-artist)]  
  Jiyoung Park, Jongpil Lee, Jangyeon Park, Jung-Woo Ha and Juhan Nam  
  _Proceedings of the 19th International Society for Music Information Retrieval Conference (ISMIR), 2018_

- **A Hybrid of Deep Audio Feature and i-vector for Artist Recognition** [[pdf](https://docs.google.com/viewer?a=v&pid=sites&srcid=ZGVmYXVsdGRvbWFpbnxmYWltbXVzaWMyMDE4fGd4OjVhYWZlOWVhMmZjYzUwYTI)]  
Jiyoung Park, Donghyun Kim, Jongpil Lee, Sangeun Kum and Juhan Nam  
_Joint Workshop on Machine Learning for Music, the 34th International Conference on Machine Learning (ICML), 2018_

- **Representation Learning Using Artist Labels for Audio Classification Tasks** [[pdf](http://www.music-ir.org/mirex/abstracts/2017/PLNPH1.pdf), [code](https://github.com/jiyoungpark527/MIREX_2017_music_classification)]  
Jiyoung Park, Jongpil Lee, Jangyeon Park, Jung-Woo Ha and Juhan Nam  
_Music Information Retrieval Evaluation eXchange (MIREX) in the 18th International Society for Musical Information Retrieval Conference (ISMIR), 2017_  
(1st place in the Music Mood Classification task across all algorithms submitted so far) 
