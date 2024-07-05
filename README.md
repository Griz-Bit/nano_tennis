# Jetson Nano Tennis Model

 This machine learning model has been trained to classify between different tennis shots, mainly forehand and backhand.

## Running this project

1. Run the docker shell in the jetson-inference folder with ./docker/run.sh
2. Change directories into jetson-inference/python/training/classification
3. The model can be trained with train.py and the images in the data folder (python3 train.py --model-dir='OUTPUT DIR' data/tennis)
4. The model can be exported with onnx_export.py (python3 onnx_export.py --model-dir='OUTPUT DIR')
5. The model can be tested with (imagenet.py --model=$'OUTPUT DIR'/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$data/tennis/labels.txt $data/tennis/test/'CLASS'/01.jpg FILENAME.jpg)
