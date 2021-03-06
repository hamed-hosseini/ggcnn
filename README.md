# Improving the Successful Robotic GraspDetection on Convolutional Neural Networks

<div align="center">
<img src="https://github.com/hamed-hosseini/ggcnn/blob/master/pics/problem_statement1.png" height="300">
</div>

This repository contains the implementation of the Improving the Successful Robotic GraspDetection on Convolutional Neural Networks from the paper:

**Improving the Successful Robotic GraspDetection on Convolutional Neural Networks**

*[Hamed Hosseini](www.linkedin.com/in/hamed-hosseini), [Mehdi Tale Masouleh](https://scholar.google.com/citations?user=gkiFy20AAAAJ&hl=en), [Ahmad Kalhor](https://scholar.google.com/citations?user=m7xdmMgAAAAJ&hl=en)

<!-- a normal html comment -->
<!--International Conference on Robotics and Automation (ICRA) 2015

[arXiv](https://arxiv.org/abs/1412.3128)

If you use this work, please cite:

```text
@article{Redmon_2015,
   title={Real-time grasp detection using convolutional neural networks},
   ISBN={9781479969234},
   url={http://dx.doi.org/10.1109/ICRA.2015.7139361},
   DOI={10.1109/icra.2015.7139361},
   journal={2015 IEEE International Conference on Robotics and Automation (ICRA)},
   publisher={IEEE},
   author={Redmon, Joseph and Angelova, Anelia},
   year={2015},
   month={May}
}
```
-->
**Contact**

Any questions or comments contact [Hamed Hosseini](hosseini.hamed@ut.ac.ir).

## Installation

⚠️ This code was developed with Python 3.6 on Ubuntu 16.04.  Python requirements can installed by:

```bash
pip install -r requirements.txt
```

## Datasets

Currently, both the [Cornell Grasping Dataset](http://pr.cs.cornell.edu/grasping/rect_data/data.php) and
[Jacquard Dataset](https://jacquard.liris.cnrs.fr/) are supported.

### Cornell Grasping Dataset

1. Download the and extract [Cornell Grasping Dataset](http://pr.cs.cornell.edu/grasping/rect_data/data.php). 
2. Convert the PCD files to depth images by running `python -m utils.dataset_processing.generate_cornell_depth <Path To Dataset>`

<div align="center">
<img src="https://github.com/hamed-hosseini/ggcnn/blob/master/pics/cornell_dataset.png" height="300">
</div>

### Jacquard Dataset

1. Download and extract the [Jacquard Dataset](https://jacquard.liris.cnrs.fr/).

## Pre-trained Models

**Coming Soon**

## Training

Training is done by the `train_ggcnn.py` script.  Run `train_ggcnn.py --help` to see a full list of options, such as dataset augmentation and validation options.

Training Figures:
<div align="center">
<img src="https://github.com/hamed-hosseini/ggcnn/blob/master/pics/total_loss.png" height="300">
</div>

## Evaluation/Visualisation

Predictions are:
<div align="center">
<img src="https://github.com/hamed-hosseini/ggcnn/blob/master/pics/prediction.png" height="500">
</div>

## Running on a Robot

comming soon!
