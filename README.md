# Classification of USA and Australian wildlife
My project is about the diffrences, the changes and unique perks of Australia wildlife and The USA wild life. And help determine where an animal is from. 
Link to retraimed model https://drive.google.com/file/d/1R5yIF3imvZHd8PXX8nReErfYjKad7TIi/view?usp=sharing
Algorithm
We have fine tuned the ResNet-18 model to be able to classify between Australian or American wildlife. The model was provided twenty training images under every category. The validation set consisted 6 images and so did the test set. 
![0](https://github.com/CHAOTICSPRIGHT/Usa-Aus_Wildlife/blob/main/testUsa.jpg?raw=true)
## Steps to Run the Project 
1. Have acces to resnet18.onnx and labels.txt on jetson nano
2. Clone the jetson-inference project from GitHub using "git clone --recursive https://github.com/dusty-nv/jetson-inference" and change directories into it
3. Have these python packages installed "sudo apt-get install libpython3-dev python3-numpy"
4. Create a build directory and run "cmake../" in the directory
5. To classify an image, run "imagenet.py --model=$MODEL/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$LABEL/labels.txt $IMAGE $OUTPUT", where $MODEL is the folder resnet18.onnx is stored, $LABEL is the folder labels.txt is stored, $IMAGE is the image file to classify, and $OUTPUT is the name of the file to output to.
6. Output image will be generated in the directory, open it to check the class label.

## Demo
