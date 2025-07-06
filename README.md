version https://git-lfs.github.com/spec/v1
oid sha256:40122004c775977eda9f3ba0ea73c092f386e7c8156a5fe98b902df0c4c55241
size 1506

YOLOv8‑SAM Real‑Time Detection
A real-time object detection and segmentation pipeline that integrates YOLOv8 (from Ultralytics) with Meta AI’s Segment Anything Model (SAM). This tool is ideal for automated data annotation, computer vision research, and real-time AI-powered applications.



Combines bounding-box detection and promptable segmentation

🚀 Key Features
🔲 YOLOv8 for fast, high-accuracy object detection (bounding boxes).
🎯 Segment Anything Model (SAM) for segmentation using bbox/point prompts.
🎥 Real-time processing from webcam or video stream.
🖼️ Support for single image annotation and JSON/YOLO format export.
🧰 Modular architecture for easy customization and research extension.

✅ Ideal Use Cases
Automated annotation for segmentation datasets.
Fast prototyping of real-time vision pipelines.
Integration into robotics, AR, and smart camera systems.
Interactive labeling for platforms like CVAT or Label Studio.

🧪 Models Used
Model	Description	Link
YOLOv8	Ultralytics object detector	Ultralytics Docs
SAM	Segment Anything from Meta AI	Meta SAM GitHub
Pretrained YOLOv8n-seg.pt	Lightweight segmentation variant	Download
SAM ViT-H Model	Best segmentation quality	Download

🧑‍💻 Installation
bash
Copy
Edit
# YOLOv8 + SAM setup
pip install ultralytics
pip install git+https://github.com/facebookresearch/segment-anything.git
bash
Copy
Edit
# Clone this repo
git clone https://github.com/nshahmeer-ai/YOLOv8-SAM-RealTime-Detection.git
cd YOLOv8-SAM-RealTime-Detection
🧠 Inference Examples
Real-Time Detection (Webcam)
bash
Copy
Edit
python main.py --source 0 --yolo yolov8n-seg.pt --sam sam_vit_h.pth
Segment Objects in an Image
bash
Copy
Edit
python detect_multiple_object_SAM.py --img data/sample.jpg
Visualize JSON Output
bash
Copy
Edit
python visualise_mask.py --results outputs/mask_output.json
📂 Folder Structure
bash
Copy
Edit
YOLOv8-SAM-RealTime-Detection/
│
├── main.py                        # Real-time detection + segmentation
├── detect_multiple_object_SAM.py # Image-based detection/segmentation
├── visualise_mask.py             # Render segmentation results
├── utils/                        # Custom helper functions
├── data/                         # Sample images or video
├── outputs/                      # Save results in JSON/YOLO formats
├── requirements.txt              # Dependencies

🔄 Workflow
YOLOv8 detects bounding boxes for each object.
Each box is passed to SAM as a prompt.
SAM generates high-quality segmentation masks.
Results are saved in standard annotation formats.

🔭 To-Do (Upcoming Features)
 Support batch image annotation
 CLI arguments for custom sources
 Export combined segmentation masks in COCO format
 Integration with annotation tools (CVAT, Roboflow)

🤝 Contributing
Star ⭐ this repo if you find it helpful.
Fork and contribute new features.
Report issues or request new capabilities.
Open to integration requests and collaborations.

📜 License
This project is released under the MIT License.

🙋 About Me
Shahmeer Nawaz – Master's student in AI & Deep Learning, building real-world projects in computer vision, MLOps, and AI infrastructure.
Open to:

💼 Remote roles (ML/DL Engineer, CV Specialist)
🤝 Research collaborations or internships
👨‍💻 Contributions to open-source vision pipelines

Email:shahmeernawazai@gmail.com


