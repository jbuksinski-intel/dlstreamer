# Available Sample Apps

This page indexes all DL Streamer samples by use case. See
[Using Sample Apps](./using_sample_apps.md) for installation, model download, and run
instructions before trying any of the samples below.

Each entry below is a mini "card": name, a one-line preview thumbnail (when available), what it
demonstrates, the elements/models it uses, and its language — `CLI` (`gst-launch` command line),
`Python`, or `C++`.

---

## Browse by category

[Object detection, classification & segmentation (9)](#object-detection-classification-segmentation) ·
[Object tracking & analytics (3)](#object-tracking-analytics) ·
[Vision-Language Models (VLM) & GenAI (5)](#vision-language-models-vlm-genai) ·
[Audio analytics (2)](#audio-analytics) ·
[3D: LiDAR & radar (5)](#3d-lidar-radar) ·
[Cameras & input sources (4)](#cameras-input-sources) ·
[Metadata: publishing, access & visualization (8)](#metadata-publishing-access-visualization) ·
[Customization & extensibility (8)](#customization-extensibility) ·
[Performance & benchmarking (2)](#performance-benchmarking) ·
[Interoperability (2)](#interoperability) ·
[Auto-generated reference applications (8)](#auto-generated-reference-applications)

> **Tip:** Use your browser's find-in-page (Ctrl+F / Cmd+F) to search across all samples by name,
> element (e.g. `gvadetect`), or model (e.g. `yolo11n`).

---

### Object detection, classification & segmentation

![](../_images/sample-detection-with-yolo-thumb.jpg)

**[Detection with YOLO](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/detection_with_yolo)** — CLI. Object detection and classification with publicly available YOLO models. Elements: `gvadetect`, `gvaclassify` · Models: `yolox_s` (default; many YOLO variants)

**[Face Detection and Classification](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/face_detection_and_classification)** — CLI. Detect faces and estimate age, gender, emotions and facial landmarks. Elements: `gvadetect`, `gvaclassify` · Models: `centerface`, `dima806_facial_age_image_detection`, `dima806_fairface_gender_image_detection`, `dima806_face_emotions_image_detection`

![](../_images/sample-instance-segmentation-thumb.jpg)

**[Instance Segmentation](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/instance_segmentation)** — CLI. Instance segmentation via the `object_detect` and `object_classify` bin elements. Elements: `object_detect`, `object_classify` · Models: `yolo26s-seg` (default; also `yolo11s-seg`)

**[Human Pose Estimation](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/human_pose_estimation)** — CLI. Full-frame human pose estimation. Elements: `gvaclassify` · Models: `yolo26s-pose`

**[Depth Estimation](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/depth_estimation)** — CLI. YOLO11n detection followed by Depth Anything V2 depth estimation on detected regions. Elements: `gvadetect`, `gvainference` · Models: `yolo11n`, `Depth-Anything-V2-Small-hf`

**[License Plate Recognition](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/license_plate_recognition)** — CLI. YOLO detector combined with an optical character recognition model. Elements: `gvadetect`, `gvainference` · Models: `yolov8` license-plate detector, `PP-OCRv4`

![](../_images/sample-prompted-detection-thumb.jpg)

**[Prompt-based Object Detection](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/prompted_detection)** — Python. Search a video for user-defined objects using an open-vocabulary model (YOLOE). Elements: `gvadetect` · Models: `yoloe-26s-seg` (text-prompt, class baked in at export)

![](../_images/sample-geti-deployment-thumb.jpg)

**[Deployment of Geti™ models](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/geti_deployment)** — CLI. Deploy Geti™-trained models for detection, anomaly detection and classification. Elements: `gvadetect`, `gvaclassify` · Models: Geti™-trained (Padim / STFPM / UFlow)

**[Motion Detect](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/motion_detect)** — CLI. Run detection only over motion ROIs (GPU and CPU paths). Elements: `gvamotiondetect`, `gvadetect` · Models: `yolov8n`

### Object tracking & analytics

**[Vehicle and Pedestrian Tracking](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/vehicle_pedestrian_tracking)** — CLI. Object tracking across frames. Elements: `gvatrack`, `gvadetect`, `gvaclassify` · Models: `yolo26s`, `dima806_vehicle_10_types_image_detection`

![](../_images/sample-gvaanalytics-tripwire-thumb.jpg)

**[Vehicle Counter with gvaanalytics Tripwires](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/gvaanalytics_tripwire)** — Python. Count vehicles crossing a virtual line in both directions using tripwires. Elements: `gvaanalytics`, `gvatrack` · Models: `yolo11n`

![](../_images/sample-smart-nvr-thumb.jpg)

**[Smart NVR for Lane Hogging Detection](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/smart_nvr)** — Python. Build an NVR with custom analytics and video storage to detect lane-hogging events. Elements: `gvaanalytics_py`, `gvarecorder_py` · Models: `rtdetr_v2_r50vd` (RT-DETRv2)

### Vision-Language Models (VLM) & GenAI

**[Using VLM Models with gvagenai](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvagenai)** — CLI. Video summarization with MiniCPM-V. Elements: `gvagenai` · Models: `MiniCPM-V`, `Phi-4-multimodal-instruct` or `Gemma-3`

![](../_images/sample-vlm-alerts-thumb.jpg)

**[VLM Alerts](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/vlm_alerts)** — Python. Edge alerting pipeline that generates structured JSON alerts per frame with annotated video. Elements: `gvagenai` · Models: Configurable VLM (e.g. `Qwen2.5-VL`, `InternVL`)

![](../_images/sample-vlm-self-checkout-thumb.jpg)

**[VLM-assisted Self Checkout](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/vlm_self_checkout)** — Python. Combine CV object detection with a VLM for item classification, running both locally on edge. Elements: `gvadetect`, `gvagenai` · Models: `yolo26s`, `MiniCPM-V-4_5`

![](../_images/sample-onvif-camera-analytics-validation-thumb.jpg)

**[ONVIF Camera Analytics Validation](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/onvif_camera_analytics_validation)** — Python. Use a VLM as an additional validation layer for ONVIF-enabled analytics cameras. Elements: `gvagenai` · Models: Configurable VLM

**[Image Embeddings Generation with ViT](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/lvm)** — CLI. Generate image embeddings using the Vision Transformer component of a CLIP model. Elements: `gvainference` · Models: `clip-vit-large-patch14` (CLIP ViT)

### Audio analytics

**[Audio Event Detection](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/audio_detect)** — CLI. Audio event detection, converting results to JSON. Elements: `gvaaudiodetect`, `gvametaconvert`, `gvametapublish` · Models: `aclnet`

**[Audio Transcription](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/audio_transcribe)** — CLI. Speech transcription using an OpenVINO GenAI Whisper model. Elements: `gvaaudiotranscribe` · Models: `whisper`

### 3D: LiDAR & radar

**[PointPillars Inference with g3dinference](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/g3dinference)** — CLI. Complete LiDAR-only 3D detection pipeline. Elements: `g3dlidarparse`, `g3dinference` · Models: `PointPillars`

**[LiDAR Parse](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/g3dlidarparse)** — CLI. LiDAR parsing pipeline. Elements: `g3dlidarparse` · Models: — (parsing only)

**[Live LiDAR Capture](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/g3dlidarsrc)** — CLI. Real-time LiDAR capture from a physical device (RoboSense via rs_driver). Elements: `g3dlidarsrc`, `g3dinference` · Models: `PointPillars`

**[Camera + 3D Object Fusion](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/g3dobjectfuser)** — CLI. Fuse 2D camera detections with 3D LiDAR detections. Elements: `g3dobjectfuser`, `gvastreammux` · Models: `yolo11n`, `PointPillars`

**[Radar Signal Process](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/g3dradarprocess)** — CLI. mmWave radar signal processing with point-cloud detection, clustering and tracking. Elements: `g3dradarprocess` · Models: — (signal processing)

### Cameras & input sources

**[RealSense™ Camera](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvarealsense)** — CLI. Capture a video stream from a 3D Intel RealSense™ Depth Camera. Elements: `gvarealsense` · Models: — (capture only)

![](../_images/sample-onvif-cameras-discovery-thumb.jpg)

**[ONVIF Camera Discovery](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/onvif_cameras_discovery)** — Python. Automatically discover ONVIF cameras on the network and launch pipelines for each. Elements: `gvadetect` · Models: Configurable detector

**[Multi-camera deployments](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/multi_stream)** — CLI. Handle video streams from multiple cameras in a single application. Elements: `gvadetect`, `gvafpscounter` · Models: `yolo11s` (many YOLO variants)

**[Multi-Stream Mux/Demux](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/stream_mux_and_demux)** — CLI. Share a single inference pipeline across streams with per-source routing. Elements: `gvastreammux`, `gvastreamdemux` · Models: Configurable detector

### Metadata: publishing, access & visualization

**[Metadata Publishing](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/metapublish)** — CLI. Convert inference metadata to JSON and publish to file or Kafka/MQTT. Elements: `gvametaconvert`, `gvametapublish` · Models: `centerface`, `dima806_fairface_gender_image_detection`, `dima806_facial_age_image_detection`

**[gvaattachroi](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvaattachroi)** — CLI. Define the regions on which inference should be performed. Elements: `gvaattachroi`, `gvadetect` · Models: `yolov8s`

**[FPS Throttle](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvafpsthrottle)** — CLI. Throttle framerate independently of sink sync, without frame duplication or dropping. Elements: `gvafpsthrottle` · Models: —

![](../_images/sample-watermark-meta-thumb.jpg)

**[Watermark Metadata](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/watermark_meta)** — Python. Attach custom drawing primitives (hexagons, lines, circles, text) and render them. Elements: `gvawatermark` · Models: — (drawing only)

**[Draw Face Attributes (C++)](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/cpp/draw_face_attributes)** — C++. Set a C callback to access frame metadata and visualize inference results. Elements: `gvadetect`, `gvaclassify` · Models: `centerface`, `dima806_facial_age_image_detection`, `dima806_fairface_gender_image_detection`, `dima806_face_emotions_image_detection`

**[Draw Face Attributes (Python)](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/draw_face_attributes)** — Python. Set a Python callback to access frame metadata and visualize inference results. Elements: `gvadetect`, `gvaclassify` · Models: `centerface`, `dima806_facial_age_image_detection`, `dima806_fairface_gender_image_detection`, `dima806_face_emotions_image_detection`

![](../_images/sample-open-close-valve-thumb.jpg)

**[Open Close Valve](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/open_close_valve)** — Python. Open/close a GStreamer `valve` branch from a callback based on detection results. Elements: `gvadetect`, `valve` · Models: `yolo11s`, `dima806_vehicle_10_types_image_detection`

![](../_images/sample-hello-dlstreamer-thumb.jpg)

**[Hello DL Streamer](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/hello_dlstreamer)** — Python. Build a detection pipeline, analyze metadata to count objects, and visualize results. Elements: `gvadetect`, `gvawatermark` · Models: `yolo11n`

### Customization & extensibility

**[Custom Post-Processing Library — Classification](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/custom_postproc/classify)** — CLI, C++. Write a custom post-processing library that converts emotion-classification outputs to GstAnalytics metadata. Elements: `gvaclassify` · Models: `centerface`, `hsemotion`

**[Custom Post-Processing Library — Detection](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/custom_postproc/detect)** — CLI, C++. Write a custom post-processing library that converts YOLOv11 tensor outputs to detection metadata. Elements: `gvadetect` · Models: `yolo11s`

**[gvapython — Face Detection and Classification](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvapython/face_detection_and_classification)** — CLI, Python. Customize a pipeline with a Python script for inference post-processing. Elements: `gvapython`, `gvadetect`, `gvaclassify` · Models: `centerface`, `dima806_fairface_gender_image_detection`, `dima806_facial_age_image_detection`

**[gvapython — Save Frames with ROI](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvapython/save_frames_with_ROI_only)** — CLI, Python. Use `gvapython` to save video frames containing detected objects to disk. Elements: `gvapython`, `gvadetect` · Models: `centerface`

**[python-elements — Face Detection and Classification](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/python-elements/face_detection_and_classification)** — CLI, Python. Build a custom Python GStreamer element using the GstAnalytics metadata API. Elements: `gvaagelogger_py`, `gvadetect`, `gvaclassify` · Models: `YOLOv8-Face-Detection`, `fairface_age_image_detection`, `fairface_gender_image_detection`

**[python-elements — Save Frames with ROI](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/python-elements/save_frames_with_ROI_only)** — CLI, Python. Build a custom Python GStreamer element to save frames with detected objects. Elements: `gvaframesaver_py`, `gvadetect` · Models: `YOLOv8-Face-Detection`

**[python-elements — Loitering Detection](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/python-elements/loitering_detection)** — CLI, Python. Measure object dwell time with a custom Python element and render a visual alert when the threshold is exceeded. Elements: `gvaanalytics`, `gvawatermark` · Models: `yolo11s`

**[Face Detection and Classification (Python)](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/face_detection_and_classification)** — Python. Download models from Hugging Face, export to OpenVINO IR, and run inference. Elements: `gvadetect`, `gvaclassify` · Models: `YOLOv8-Face-Detection`, `fairface`

### Performance & benchmarking

**[Benchmark](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/benchmark)** — CLI, Python. Measure the performance of single- or multi-channel video analytics pipelines. Elements: `gvadetect`, `gvafpscounter` · Models: `centerface` (configurable)

![](../_images/sample-e2e-performance-thumb.jpg)

**[DL Streamer E2E Performance](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/e2e_performance)** — Python. Compare DL Streamer vs. OpenCV + OpenVINO throughput with a YOLO26s INT8 model. Elements: `gvadetect` · Models: `yolo26s` (INT8)

### Interoperability

**[DL Streamer and DeepStream Coexistence](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/coexistence)** — Python. Run pipelines on DL Streamer and/or NVIDIA DeepStream side by side. Elements: `gvadetect` · Models: `yolov8` license-plate detector, `PP-OCRv4`

**[Coexistence Benchmark](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/coexistence_benchmark)** — Python. Measure the maximum number of concurrent LPR streams on systems combining Intel and NVIDIA hardware. Elements: `gvadetect` · Models: `yolov8` license-plate detector, `PP-OCRv4`

---

## Auto-generated reference applications

These end-to-end reference apps combine multiple elements into complete solutions.
Find them under
[samples/auto_generated_samples](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples).

**[DeepStream Test4 → DL Streamer Conversion](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/deepstream_python_conversion)** — CLI. DL Streamer equivalent of NVIDIA's deepstream-test4 with YOLO11n detection and metadata publishing. Elements: `gvadetect`, `gvametaconvert`, `gvametapublish` · Models: `yolo11n`

**[DeepStream LPR App Conversion (C++)](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/deepstream_cpp_conversion)** — C++. C++ conversion of NVIDIA's DeepStream LPR app — license plate detection, tracking and text recognition. Elements: `gvadetect`, `gvatrack`, `gvaclassify` · Models: YOLOv11, PaddleOCR

**[License Plate Recognition](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/license_plate_recognition)** — CLI. Detect license plates with YOLOv11 and recognize text with PaddleOCR. Elements: `gvadetect`, `gvainference` · Models: `YOLOv11`, `PaddleOCR`

**[Multi-Stream Compose](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/multi_stream_compose)** — CLI. Multi-camera analytics with composite WebRTC output, on-demand recording and a 2x2 GPU-accelerated mosaic. Elements: `gvadetect`, `gvastreammux`, `gvawatermark` · Models: `yolo11s`

**[People Detection and Tracking with Deep SORT](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/people_detection_tracking)** — CLI. Detect and track people using YOLO26m and Deep SORT with a Mars-Small-128 re-ID model. Elements: `gvadetect`, `gvatrack` · Models: `yolo26m`, `mars-small128`

**[Pose Estimation Compose](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/pose_estimation_compose)** — CLI. Run 4 YOLO pose models in parallel on the same video and composite results into a 2x2 mosaic. Elements: `gvaclassify`, `gvawatermark` · Models: `yolo26n-pose`, `yolo11n-pose`, `yolov8n-pose`, `yolov8l-pose`

**[Safety Compliance Monitor](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/safety_compliance)** — CLI. Detect and track workers and use Qwen2.5-VL to verify helmet and harness compliance. Elements: `gvadetect`, `gvatrack`, `gvagenai` · Models: `yolo26m`, `Qwen2.5-VL-3B`

**[Smart NVR — Event-Based Recording](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/smart_nvr)** — CLI. Detect people with YOLO11n and record video only when a person is present. Elements: `gvadetect` · Models: `yolo11n`
