# grasp_multiObject_multiGrasp

This is the implementation of our RA-L work 'Real-world Multi-object, Multi-grasp Detection'. The detector takes RGB-D image input and predicts multiple grasp candidates for a single object or multiple objects, in a single shot. The original arxiv paper can be found [here](https://arxiv.org/pdf/1802.00520.pdf). The final version will be updated after publication process.

If you find it helpful for your research, please consider citing:

    @inproceedings{chu2018deepgrasp,
    Author = {Fu-Jen Chu and Ruinian Xu and Patricio A. Vela},
    Title = {Deep Grasp: Detection and Localization of Grasps with Deep Neural Networks},
    booktitle = {arXiv:1802.00520},
    Year = {2018}
    }

If you encounter any questions, please contact me at fujenchu[at]gatech[dot]edu


### Demo
1. Clone this repository
```
git clone https://github.com/ivalab/grasp_multiObject_multiGrasp.git
cd grasp_multiObject_multiGrasp
```

2. Build Cython modules
```
cd lib
make clean
make
cd ..
```

3. Install [Python COCO API](https://github.com/cocodataset/cocoapi)
```
cd data
git clone https://github.com/pdollar/coco.git
cd coco/PythonAPI
make
cd ../../..
```

4. Download pretrained models
- trained model for grasp on [dropbox drive](https://www.dropbox.com/s/ldapcpanzqdu7tc/models.zip?dl=0) 
- put under `output/res50/train/default/`

5. Run demo
```
./tools/demo_graspRGD.py --net res50 --dataset grasp
```
you can see images pop out.

### Acknowledgment

This repo borrows tons of code from
- [tf-faster-rcnn](https://github.com/endernewton/tf-faster-rcnn) by endernewton

### Resources
- [multi-object grasp dataset](https://github.com/ivalab/grasp_multiObject)
- [grasp annotation tool](https://github.com/ivalab/grasp_annotation_tool)
