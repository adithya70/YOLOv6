# YOLOv6
yolov6 for cusom dataset
# 1) clone the repo in colab or in local system
   ! git clone  https://github.com/adithya70/YOLOv6.git
# 2) change directory to yolov6 parent folder
   * run the following command to install required packages !pip install -r requirements.txt
   *In the parent folder access dataset.yaml fike and add the required path to the train dataset and test dateset and change other parametrs as requited
   * In the weights add required yolov6 pretrained weights.pt files
# 3) Training custom dataset
   * Use the following command to start training on custom dataset. 
   !python tools/train.py --batch 16 --conf configs/yolov6s_finetune.py --data-path dataset.yaml --device 0 --epochs 2 --eval-interval 2
     change the parameters as required
# 4) For evaluation 
    * Run the following command 
    !python tools/eval.py --data dataset.yaml  --weights runs/train/exp/weights/best_ckpt.pt --device 0
# 5) For inference run the following command
    !python tools/infer.py --weights runs/train/exp/weights/best_ckpt.pt --source 100.jpg --yaml dataset.yaml --device 0 
