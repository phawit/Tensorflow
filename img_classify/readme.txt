https://www.youtube.com/watch?v=cKxRvEZd3Mw&list=PLOU2XLYxmsIIuiBfYad6rFYQU_jL2ryal
https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/?utm_campaign=chrome_series_machinelearning_063016&utm_source=gdev&utm_medium=yt-desc#0
//---------------------------------------------------------------------------------

#image_classify
-Prepare environment like img_classify'floder(this github)
-image just example 14 photos of each kind of flower in flower_photos'folder from this github. It's not enought data for train. So you must download full photos from this link. it's contain about 633 photos of each kind of flower.
 $curl -O http://download.tensorflow.org/example_images/flower_photos.tgz
tar xzf flower_photos.tgz

RUN..
1.Tensorboard

  $tensorboard --logdir training_summaries &
  http://0.0.0.0:6006/


2.TrainData(.jpg>>.txt & training data)

  $python retrain.py \
  --bottleneck_dir=bottlenecks \
  --how_many_training_steps=500 \
  --model_dir=inception \
  --summaries_dir=training_summaries/basic \
  --output_graph=retrained_graph.pb \
  --output_labels=retrained_labels.txt \
  --image_dir=flower_photos


3.PredictIMG

  $python label_image.py flower_photos/sunflower.jpg


***install python, Tensorflow, ...
***install docker
https://store.docker.com/editions/community/docker-ce-server-ubuntu
Python 2.7.6 ($python -V)
Tensorflow 




