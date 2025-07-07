**YOLOv8-SAM Real-Time Detection**

A real-time object detection + segmentation pipeline integrating Ultralytics YOLOv8 and Meta AI's Segment Anything
Model (SAM). Designed for automated annotation, real-time computer vision tasks, and smart segmentation pipelines.

Key Features
- YOLOv8 for fast, accurate bounding box detection
- SAM for prompt-based segmentation (bounding box or point-based)
- Real-time webcam or video stream support
- Single image segmentation with export to YOLO/COCO/JSON formats
- Modular Python pipeline for research and production

Ideal Use Cases
- Dataset auto-annotation for segmentation tasks
- Real-time AI in robotics, AR/VR, smart cameras
- Labeling assistance in tools like CVAT, Roboflow, Label Studio
- Research in promptable segmentation

  
Models Used
- YOLOv8 (Ultralytics) - https://docs.ultralytics.com/
- SAM (Meta AI) - https://github.com/facebookresearch/segment-anything
- YOLOv8n-seg.pt - https://github.com/ultralytics/assets/releases/download/v0.0.0/yolov8n-seg.pt
- SAM ViT-H - https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth

Installation
pip install ultralytics
pip install git+https://github.com/facebookresearch/segment-anything.git
git clone https://github.com/nshahmeer-ai/YOLOv8-SAM-RealTime-Detection.git
cd YOLOv8-SAM-RealTime-Detection


Inference Examples
python main.py --source 0 --yolo yolov8n-seg.pt --sam sam_vit_h.pth
python detect_multiple_object_SAM.py --img data/sample.jpg
python visualise_mask.py --results outputs/mask_output.json

Workflow
1. YOLOv8 detects objects and draws bounding boxes
2. Bounding boxes are passed as prompts to SAM
3. SAM returns segmentation masks
4. Results saved in JSON or visual formats

To-Do (Upcoming Features)
- Multi-image and batch mode support
- YOLO and JSON hybrid output
- COCO-style mask output
- Integration with annotation tools (CVAT, Roboflow, Label Studio)
  
Contributing
- Star this repo
- Fork and PR improvements
- Report issues or bugs
- Add new model integrations or features

Open to:
- Remote roles (ML/DL Engineer, CV Specialist)
- Research internships or collaborations
- Open-source AI/ML contributions
  

About the Author
Shahmeer Nawaz
Master's Student in Artificial Intelligence

Email: shahmeernawazai@gmail.com
GitHub: https://github.com/nshahmeer-ai
LinkedIn: https://www.linkedin.com/in/shahmeernawazai


License
MIT License
