# Eye direction classifier

 The project tells the user whether an eye is looking right, left, up, or closed based on image classifier. I wanted to make a eyetracker to see where people are paying attention to on the screen, and if blue light effects the user.  

![add image descrition here](direct image link here)

## The Algorithm

It's a retrained Resnet 18 model, it uses a database of more than 3000 eye photos. It runs on imagenet.py and runs on the Jetson Nano. 

## Running this project

1. Download Resnet 18 and lebels.txt
2. Have Jetson inference installed or downloaded.
3. In Jetson inference change classification Change directory using command ```cd jetson-inference/python/training/classification```
4. Set net and dataset using ```NET=models/eyes``` ```DATASET=data/eyedataset```
5. Run ```imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/_____.jpg ____.jpg```(the first jpg is the image your giving to the model and the second one is the one gets lebeled.
6. Open the image to results (results will also be in the command line)
[View a video explanation here](video link)
