## Team: Broncos <img align="right" src="https://user-images.githubusercontent.com/95270677/221381417-168eae3f-0cab-4c93-bdad-7d692ec511f3.png">

**Team members:**  Tianjie Zhang, Donglei Wang, Yang Lu


### 🚗Task 1

**How to run:**
0. Download this repository and put it in your tutorial file folder.
1. open the terminal and go to your file folder:

```
cd 'your_path'
```

2. Run the following code to train the mdoel. 

```
python train_dsps.py --data data/dsps.yaml --epochs 400 --weights yolov5s.pt --cfg yolov5s.yaml  --batch-size 16 --hyp data/hyps/hyp.scratch-med.yaml
```

3. After training, run the detec.py to test the result.

```
python detect_dsps.py --weights 'your_trained .pt file path' --source test_data --conf-thres 0.65 --iou-thres 0.999 --augment
```

*Other way:* run the DSPS_task1.ipynb directly.

**Strategy used:**

1. Using wGAN to generate real-like images;
2. using random crop, flip and contrast adjusting to augment the images;
3. A feature-balanced strategy: try to make the amount of different defects equal'
4. Fine tune of the hyperparameters: 
training: epochs = 400, batch_size = 16, hyp = hyp.scatch-med.yaml
testing: conf-thres = 0.65, iou-thres = 0.999, augment = true

### 🚓Task 2

**How to run:**
1. open the terminal and go to your file folder:

```
cd 'your_path'
```

2. Run the following code to train the mdoel. 

```
python train_dsps.py --data data/dsps2.yaml --epochs 400 --weights yolov5s.pt --cfg yolov5l_simAM.yaml  --batch-size 16 --hyp data/hyps/hyp.scratch-med.yaml
```

3. After training, run the detec.py to test the result.

```
python detect_dsps2.py --weights runs/train/exp10/weights/best.pt --source images/ --conf-thres 0.65 --iou-thres 0.999 --augment  
```

*Other way:* run the DSPS_task2.ipynb directly.

**Strategy used:**

Attention module modified the yolov5




**Links:**
- https://dsps-1e998.web.app/
- https://github.com/UM-Titan/DSPS23


