## Team: Broncos <img align="right" src="https://user-images.githubusercontent.com/95270677/221381417-168eae3f-0cab-4c93-bdad-7d692ec511f3.png">

Team members: Tianjie Zhang, Donglei Wang, Yang Lu


How to run:
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


Links: 
- https://dsps-1e998.web.app/
- https://github.com/UM-Titan/DSPS23


