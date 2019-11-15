# object-detection
Tensorflow Demo

## clone the repo
`git clone https://github.com/Enthuons/object-detection.git`


## install project dependencies using pip
`pip install -r requirements.txt`

## install tensorflow training models (inside or outside the current project)
`git clone https://github.com/tensorflow/models.git`

## set the models path as environment variables
`cd models/research/`
`export PYTHONPATH=$PYTHONPATH:$(pwd):$(pwd)/slim`

## running the script
You can run the script in two modes
    * Camera mode
    `python my-object-detection.py -d 1 -o 1 -w 20 -q-size 150`
    * Input video file mode
    `python my-object-detection.py -d 1 -o 1 -i traffic.mp4 -w 20 -q-size 150`
    (input video files `e.g. traffic.mp4` should be available inside `inputs` folder)

After running the script you will get the output as a videos file containing the input video and identified objects inside `outputs` folder
