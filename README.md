# Retina Network
## Quick start
Clone this repository:
```
git clone https://github.com/Xavier1999-Chen/RetinaNet-Pytorch.git
```

Pull an docker image is the most fast and stable way to get the running environment:
```
docker pull 
```

Then, use the following cml to create a container:
```
docker run -it --net=host --name=retinanet -v /YOUR/LOCAL/PATH/to/THIS/REPOSITORY:/workspace -v /tmp/.X11-unix:/tmp/.X11-unix -v /dev:/dev -e DISPLAY=$DISPLAY pytorch/pytorch
```

Now you can access the container to train and test your RetinaNet :)
# Reference
[Focal Loss for Dense Object Detection. ICCV 2017 (Best Student Paper Award)](https://arxiv.org/abs/1708.02002)
