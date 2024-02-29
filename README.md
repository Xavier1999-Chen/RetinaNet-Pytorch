# Retina Network
## Quick start
Clone this repository:
```
git clone https://github.com/Xavier1999-Chen/RetinaNet-Pytorch.git
```

Pull a docker image is the most fast and stable way to get the running environment:
```
docker pull xavier1999/retinanet-pytorch:v1.0
```

Then, use the following cml to create a container:
```
docker run -it --net=host --name=retinanet -v /YOUR/LOCAL/PATH/to/THIS/REPOSITORY:/workspace -v /tmp/.X11-unix:/tmp/.X11-unix -v /dev:/dev -e DISPLAY=$DISPLAY xavier1999/retinanet-pytorch:v1.0
```

Now you can access the container to train and test your RetinaNet :)

## Scripts
### Train
```
python train.py --coco_path ./data --output_path ./output --depth 50 --epochs 20
```
### Evaluation
Use this script to generate test set predictions for submission
```
python test.py --coco_path ./data --checkpoint_path ./output/model_final.pt --depth 50
```
or evaluate your model on validataion results
```
python test.py --coco_path ./data --checkpoint_path ./output/model_final.pt --depth 50 --set_name 'val'
```
### Visualization
```
python vis.py
```

# Reference
[Focal Loss for Dense Object Detection. ICCV 2017 (Best Student Paper Award)](https://arxiv.org/abs/1708.02002)
