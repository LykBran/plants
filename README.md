# Plants  

This project contains a pre-trained model. It recognize plants and tells people their names. It might be helpful in the wild.  

## The Algorithm  

The image classification model was trained on Jetson Nano with a dataset of plants. You can use it with imagenet to recognize plants.  

## Running This Project

1. Clone jetson-inference project from Github.  

```
$ git clone --recursive https://github.com/dusty-nv/jetson-inference
```

2. Make sure to have python packages installed.  

```
$ sudo apt-get install libpython3-dev python3-numpy
```

3. Build jetson-inference from source.  

```
$ mkdir build
$ cd build
$ cmake ../
$ make
$ sudo make install
$ sudo ldconfig
```

4. Clone this repository from Github and change dir into the project.  

```
$ git clone https://github.com/LykBran/plants.git
$ cd plants
```

5. Run this command to use the model.  

tips: Replace A with your own camera device or image, and replace B with your expected output file.  
```
$ imagenet --input_blob=input_0 --output_blob=output_0 --model=resnet18.onnx --labels=labels.txt A B
```

Dataset URL : https://nvidia.box.com/shared/static/vbsywpw5iqy7r38j78xs0ctalg7jrg79.gz
