# object-detection
Tensorflow Demo

## clone the repo
`git clone https://github.com/Enthuons/object-detection.git`


## install project dependencies using pip
`pip install -r requirements.txt`

## install tensorflow training models (inside or outside the current project)
`git clone https://github.com/tensorflow/models.git`

### update following files
* models/research/object-detection/utils/label_map_util.py
    * line 138 `with tf.gfile.GFile(path, 'r') as fid:` to `with tf.io.gfile.GFile(path, 'r') as fid:`

## install and setup protoc
`sudo apt-get install protobuf-compiler python-pil python-lxml python-tk` <br>
`cd models/research/` <br>
`protoc object_detection/protos/*.proto --python_out=.`

## set the models path as environment variables
`cd models/research/` <br>
`export PYTHONPATH=$PYTHONPATH:$(pwd):$(pwd)/slim`

## running the script
You can run the script in two modes <br>
* **Camera mode** <br>
`python my-object-detection.py -d 1 -o 1 -w 20 -q-size 150`
* **Input video file mode** <br>
`python my-object-detection.py -d 1 -o 1 -i traffic.mp4 -w 20 -q-size 150`
<br>(input video files `e.g. traffic.mp4` should be available inside `inputs` folder)

After running the script you will get the output as a videos file containing the input video and identified objects inside `outputs` folder
