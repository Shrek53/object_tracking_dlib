**Create virtual env**
```bash
virtualenv venv -p python3
```
**Activate virtual env**
```bash
source ./venv/bin/activate
```
**Install system libraries to install dlib**
```bash
sudo apt-get update
sudo apt-get install build-essential cmake
sudo apt-get install libopenblas-dev liblapack-dev 
sudo apt-get install libx11-dev libgtk-3-dev
```
**Install requirements**
```bash
pip install -r requirements.txt
```
**Run object tracking program from webcam**
```bash
python track_object.py --prototxt mobilenet_ssd/MobileNetSSD_deploy.prototxt --model mobilenet_ssd/MobileNetSSD_deploy.caffemodel --label person --output output/result_output.avi
```
**Run object tracking program from input file**
```bash
python track_object.py --prototxt mobilenet_ssd/MobileNetSSD_deploy.prototxt --model mobilenet_ssd/MobileNetSSD_deploy.caffemodel --video input/race.mp4 --label person --output output/vid_output.avi
```
