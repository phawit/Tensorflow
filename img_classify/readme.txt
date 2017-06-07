https://www.youtube.com/watch?v=cKxRvEZd3Mw&list=PLOU2XLYxmsIIuiBfYad6rFYQU_jL2ryal
https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/?utm_campaign=chrome_series_machinelearning_063016&utm_source=gdev&utm_medium=yt-desc#0
//---------------------------------------------------------------------------------

#image_classify
-Prepare environment like init floder

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


***install docker
https://store.docker.com/editions/community/docker-ce-server-ubuntu
Python 2.7.6 ($python -V)
Tensorflow 




