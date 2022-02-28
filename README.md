# Pipeline for paddydiease classification

## Requirement

- This work was tested with PyTorch 1.6.0, CUDA 10.1 and python 3.7.
     pip3 install -r requirement.txt
## train model
```bash
python train.py --model_name=EfficientNetB3 --batch_size=16 --epochs=40 --img_size=300 --train_dir=train --val_dir=val --visualize_dir=visualize1 --model_dir=model_final
```
## Evaluate Model
```bash
python3 evaluate.py --predict_path test --model_path model_final/EfficientNetB3_model.h5 --save_path final_result/ --model_name efficientnetb5 --img_size 300
```
## Predict result folder with custom accuracy (return csv file  results)
```bash
python3 predict.py --predict_path test --model_path model_final/EfficientNetB4_model.h5--save_path final_result/ --model_name efficientnetd --img_size 300
```
## Predict with  image
```bash
python3 predictimg.py --predict_path test --model_path model_final/EfficientNetB3_model.h5 --model_name efficientnetb5 --img_size 300
```
