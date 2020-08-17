# Improving the Successful Robotic GraspDetection on Convolutional Neural Networks

![problem statement](pics/problem_statement1.png =10x10)
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

This code was developed with Python 3.6 on Ubuntu 16.04.  Python requirements can installed by:

```bash
pip install -r requirements.txt
```

## Datasets

Currently, both the [Cornell Grasping Dataset](http://pr.cs.cornell.edu/grasping/rect_data/data.php) and
[Jacquard Dataset](https://jacquard.liris.cnrs.fr/) are supported.

### Cornell Grasping Dataset

1. Download the and extract [Cornell Grasping Dataset](http://pr.cs.cornell.edu/grasping/rect_data/data.php). 
2. Convert the PCD files to depth images by running `python -m utils.dataset_processing.generate_cornell_depth <Path To Dataset>`

### Jacquard Dataset

1. Download and extract the [Jacquard Dataset](https://jacquard.liris.cnrs.fr/).

## Pre-trained Models

**Coming Soon**

## Training

Training is done by the `train_ggcnn.py` script.  Run `train_ggcnn.py --help` to see a full list of options, such as dataset augmentation and validation options.

Some basic examples:

```bash
# Train GG-CNN on Cornell Dataset
python train_ggcnn.py --description training_example --network ggcnn --dataset cornell --dataset-path <Path To Dataset>

# Train GG-CNN2 on Jacquard Datset
python train_ggcnn.py --description training_example2 --network ggcnn2 --dataset jacquard --dataset-path <Path To Dataset>
```

Trained models are saved in `output/models` by default, with the validation score appended.

## Evaluation/Visualisation

Evaluation or visualisation of the trained networks are done using the `eval_ggcnn.py` script.  Run `eval_ggcnn.py --help` for a full set of options.

Important flags are:
* `--iou-eval` to evaluate using the IoU between grasping rectangles metric.
* `--jacquard-output` to generate output files in the format required for simulated testing against the Jacquard dataset.
* `--vis` to plot the network output and predicted grasping rectangles.

For example:

```bash
python eval_ggcnn.py --network <Path to Trained Network> --dataset jacquard --dataset-path <Path to Dataset> --jacquard-output --iou-eval
```


## Running on a Robot

Our ROS implementation for running the grasping system see [https://github.com/dougsm/mvp_grasp](https://github.com/dougsm/mvp_grasp).

The original implementation for running experiments on a Kinva Mico arm can be found in the repository [https://github.com/dougsm/ggcnn_kinova_grasping](https://github.com/dougsm/ggcnn_kinova_grasping).
