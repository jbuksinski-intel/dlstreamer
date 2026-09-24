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

<!-- Shared card styling (GitHub strips this <style> block harmlessly; Sphinx applies it) -->
<style>
.sample-card { display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443; }
.sample-thumb { flex:0 0 96px; max-width:96px; }
.sample-body { flex:1; line-height:1.35; }
.sample-title { margin:0 0 0.2rem; }
.sample-desc { margin:0.15rem 0; }
.sample-meta { margin:0.15rem 0; font-size:0.9rem; color:#888; }
</style>

---

### Object detection, classification & segmentation

<div class="sample-card">
  <div class="sample-thumb">

  ![Detection with YOLO](../_images/sample-detection-with-yolo-thumb.jpg)

  </div>
  <div class="sample-body">
    <p class="sample-title"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/detection_with_yolo">Detection with YOLO</a></strong> <code>CLI</code></p>
    <p class="sample-desc">Object detection and classification with publicly available YOLO models.</p>
    <p class="sample-meta"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolox_s</code> (default; many YOLO variants)</p>
  </div>
</div>

<div class="sample-card">
  <div class="sample-thumb">

  ![Face Detection and Classification](../_images/sample_app_template.jpg)

  </div>
  <div class="sample-body">
    <p class="sample-title"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/face_detection_and_classification">Face Detection and Classification</a></strong> <code>CLI</code></p>
    <p class="sample-desc">Detect faces and estimate age, gender, emotions and facial landmarks.</p>
    <p class="sample-meta"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>centerface</code>, <code>dima806_facial_age_image_detection</code>, <code>dima806_fairface_gender_image_detection</code>, <code>dima806_face_emotions_image_detection</code></p>
  </div>
</div>

<div class="sample-card">
  <div class="sample-thumb">

  ![Instance Segmentation](../_images/sample-instance-segmentation-thumb.jpg)

  </div>
  <div class="sample-body">
    <p class="sample-title"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/instance_segmentation">Instance Segmentation</a></strong> <code>CLI</code></p>
    <p class="sample-desc">Instance segmentation via the <code>object_detect</code> and <code>object_classify</code> bin elements.</p>
    <p class="sample-meta"><strong>Elements:</strong> <code>object_detect</code>, <code>object_classify</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo26s-seg</code> (default; also <code>yolo11s-seg</code>)</p>
  </div>
</div>

<div class="sample-card">
  <div class="sample-thumb">

  ![Human Pose Estimation](../_images/sample_app_template.jpg)

  </div>
  <div class="sample-body">
    <p class="sample-title"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/human_pose_estimation">Human Pose Estimation</a></strong> <code>CLI</code></p>
    <p class="sample-desc">Full-frame human pose estimation.</p>
    <p class="sample-meta"><strong>Elements:</strong> <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo26s-pose</code></p>
  </div>
</div>

<div class="sample-card">
  <div class="sample-thumb">

  ![Depth Estimation](../_images/sample_app_template.jpg)

  </div>
  <div class="sample-body">
    <p class="sample-title"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/depth_estimation">Depth Estimation</a></strong> <code>CLI</code></p>
    <p class="sample-desc">YOLO11n detection followed by Depth Anything V2 depth estimation on detected regions.</p>
    <p class="sample-meta"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvainference</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo11n</code>, <code>Depth-Anything-V2-Small-hf</code></p>
  </div>
</div>

<div class="sample-card">
  <div class="sample-thumb">

  ![License Plate Recognition](../_images/sample_app_template.jpg)

  </div>
  <div class="sample-body">
    <p class="sample-title"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/license_plate_recognition">License Plate Recognition</a></strong> <code>CLI</code></p>
    <p class="sample-desc">YOLO detector combined with an optical character recognition model.</p>
    <p class="sample-meta"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvainference</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolov8</code> license-plate detector, <code>PP-OCRv4</code></p>
  </div>
</div>

<div class="sample-card">
  <div class="sample-thumb">

  ![Prompt-based Object Detection](../_images/sample-prompted-detection-thumb.jpg)

  </div>
  <div class="sample-body">
    <p class="sample-title"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/prompted_detection">Prompt-based Object Detection</a></strong> <code>Python</code></p>
    <p class="sample-desc">Search a video for user-defined objects using an open-vocabulary model (YOLOE).</p>
    <p class="sample-meta"><strong>Elements:</strong> <code>gvadetect</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yoloe-26s-seg</code> (text-prompt, class baked in at export)</p>
  </div>
</div>

<div class="sample-card">
  <div class="sample-thumb">

  ![Deployment of Geti™ models](../_images/sample-geti-deployment-thumb.jpg)

  </div>
  <div class="sample-body">
    <p class="sample-title"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/geti_deployment">Deployment of Geti™ models</a></strong> <code>CLI</code></p>
    <p class="sample-desc">Deploy Geti™-trained models for detection, anomaly detection and classification.</p>
    <p class="sample-meta"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> Geti™-trained (Padim / STFPM / UFlow)</p>
  </div>
</div>

<div class="sample-card">
  <div class="sample-thumb">

  ![Motion Detect](../_images/sample_app_template.jpg)

  </div>
  <div class="sample-body">
    <p class="sample-title"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/motion_detect">Motion Detect</a></strong> <code>CLI</code></p>
    <p class="sample-desc">Run detection only over motion ROIs (GPU and CPU paths).</p>
    <p class="sample-meta"><strong>Elements:</strong> <code>gvamotiondetect</code>, <code>gvadetect</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolov8n</code></p>
  </div>
</div>

### Object tracking & analytics

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Vehicle and Pedestrian Tracking](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/vehicle_pedestrian_tracking">Vehicle and Pedestrian Tracking</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Object tracking across frames.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvatrack</code>, <code>gvadetect</code>, <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo26s</code>, <code>dima806_vehicle_10_types_image_detection</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Vehicle Counter with gvaanalytics Tripwires](../_images/sample-gvaanalytics-tripwire-thumb.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/gvaanalytics_tripwire">Vehicle Counter with gvaanalytics Tripwires</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Count vehicles crossing a virtual line in both directions using tripwires.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvaanalytics</code>, <code>gvatrack</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo11n</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Smart NVR for Lane Hogging Detection](../_images/sample-smart-nvr-thumb.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/smart_nvr">Smart NVR for Lane Hogging Detection</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Build an NVR with custom analytics and video storage to detect lane-hogging events.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvaanalytics_py</code>, <code>gvarecorder_py</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>rtdetr_v2_r50vd</code> (RT-DETRv2)</p>
  </div>
</div>

### Vision-Language Models (VLM) & GenAI

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Using VLM Models with gvagenai](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvagenai">Using VLM Models with gvagenai</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Video summarization with MiniCPM-V.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvagenai</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>MiniCPM-V</code>, <code>Phi-4-multimodal-instruct</code> or <code>Gemma-3</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![VLM Alerts](../_images/sample-vlm-alerts-thumb.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/vlm_alerts">VLM Alerts</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Edge alerting pipeline that generates structured JSON alerts per frame with annotated video.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvagenai</code> &nbsp;|&nbsp; <strong>Models:</strong> Configurable VLM (e.g. <code>Qwen2.5-VL</code>, <code>InternVL</code>)</p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![VLM-assisted Self Checkout](../_images/sample-vlm-self-checkout-thumb.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/vlm_self_checkout">VLM-assisted Self Checkout</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Combine CV object detection with a VLM for item classification, running both locally on edge.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvagenai</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo26s</code>, <code>MiniCPM-V-4_5</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![ONVIF Camera Analytics Validation](../_images/sample-onvif-camera-analytics-validation-thumb.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/onvif_camera_analytics_validation">ONVIF Camera Analytics Validation</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Use a VLM as an additional validation layer for ONVIF-enabled analytics cameras.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvagenai</code> &nbsp;|&nbsp; <strong>Models:</strong> Configurable VLM</p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Image Embeddings Generation with ViT](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/lvm">Image Embeddings Generation with ViT</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Generate image embeddings using the Vision Transformer component of a CLIP model.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvainference</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>clip-vit-large-patch14</code> (CLIP ViT)</p>
  </div>
</div>

### Audio analytics

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Audio Event Detection](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/audio_detect">Audio Event Detection</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Audio event detection, converting results to JSON.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvaaudiodetect</code>, <code>gvametaconvert</code>, <code>gvametapublish</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>aclnet</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Audio Transcription](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/audio_transcribe">Audio Transcription</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Speech transcription using an OpenVINO GenAI Whisper model.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvaaudiotranscribe</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>whisper</code></p>
  </div>
</div>

### 3D: LiDAR & radar

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![PointPillars Inference with g3dinference](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/g3dinference">PointPillars Inference with g3dinference</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Complete LiDAR-only 3D detection pipeline.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>g3dlidarparse</code>, <code>g3dinference</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>PointPillars</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![LiDAR Parse](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/g3dlidarparse">LiDAR Parse</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">LiDAR parsing pipeline.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>g3dlidarparse</code> &nbsp;|&nbsp; <strong>Models:</strong> — (parsing only)</p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Live LiDAR Capture](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/g3dlidarsrc">Live LiDAR Capture</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Real-time LiDAR capture from a physical device (RoboSense via rs_driver).</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>g3dlidarsrc</code>, <code>g3dinference</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>PointPillars</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Camera + 3D Object Fusion](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/g3dobjectfuser">Camera + 3D Object Fusion</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Fuse 2D camera detections with 3D LiDAR detections.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>g3dobjectfuser</code>, <code>gvastreammux</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo11n</code>, <code>PointPillars</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Radar Signal Process](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/g3dradarprocess">Radar Signal Process</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">mmWave radar signal processing with point-cloud detection, clustering and tracking.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>g3dradarprocess</code> &nbsp;|&nbsp; <strong>Models:</strong> — (signal processing)</p>
  </div>
</div>

### Cameras & input sources

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![RealSense™ Camera](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvarealsense">RealSense™ Camera</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Capture a video stream from a 3D Intel RealSense™ Depth Camera.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvarealsense</code> &nbsp;|&nbsp; <strong>Models:</strong> — (capture only)</p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![ONVIF Camera Discovery](../_images/sample-onvif-cameras-discovery-thumb.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/onvif_cameras_discovery">ONVIF Camera Discovery</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Automatically discover ONVIF cameras on the network and launch pipelines for each.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code> &nbsp;|&nbsp; <strong>Models:</strong> Configurable detector</p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Multi-camera deployments](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/multi_stream">Multi-camera deployments</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Handle video streams from multiple cameras in a single application.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvafpscounter</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo11s</code> (many YOLO variants)</p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Multi-Stream Mux/Demux](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/stream_mux_and_demux">Multi-Stream Mux/Demux</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Share a single inference pipeline across streams with per-source routing.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvastreammux</code>, <code>gvastreamdemux</code> &nbsp;|&nbsp; <strong>Models:</strong> Configurable detector</p>
  </div>
</div>

### Metadata: publishing, access & visualization

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Metadata Publishing](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/metapublish">Metadata Publishing</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Convert inference metadata to JSON and publish to file or Kafka/MQTT.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvametaconvert</code>, <code>gvametapublish</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>centerface</code>, <code>dima806_fairface_gender_image_detection</code>, <code>dima806_facial_age_image_detection</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![gvaattachroi](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvaattachroi">gvaattachroi</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Define the regions on which inference should be performed.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvaattachroi</code>, <code>gvadetect</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolov8s</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![FPS Throttle](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvafpsthrottle">FPS Throttle</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Throttle framerate independently of sink sync, without frame duplication or dropping.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvafpsthrottle</code> &nbsp;|&nbsp; <strong>Models:</strong> —</p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Watermark Metadata](../_images/sample-watermark-meta-thumb.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/watermark_meta">Watermark Metadata</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Attach custom drawing primitives (hexagons, lines, circles, text) and render them.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvawatermark</code> &nbsp;|&nbsp; <strong>Models:</strong> — (drawing only)</p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Draw Face Attributes (C++)](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/cpp/draw_face_attributes">Draw Face Attributes (C++)</a></strong> <code>C++</code></p>
    <p style="margin:0.15rem 0;">Set a C callback to access frame metadata and visualize inference results.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>centerface</code>, <code>dima806_facial_age_image_detection</code>, <code>dima806_fairface_gender_image_detection</code>, <code>dima806_face_emotions_image_detection</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Draw Face Attributes (Python)](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/draw_face_attributes">Draw Face Attributes (Python)</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Set a Python callback to access frame metadata and visualize inference results.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>centerface</code>, <code>dima806_facial_age_image_detection</code>, <code>dima806_fairface_gender_image_detection</code>, <code>dima806_face_emotions_image_detection</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Open Close Valve](../_images/sample-open-close-valve-thumb.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/open_close_valve">Open Close Valve</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Open/close a GStreamer <code>valve</code> branch from a callback based on detection results.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>valve</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo11s</code>, <code>dima806_vehicle_10_types_image_detection</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Hello DL Streamer](../_images/sample-hello-dlstreamer-thumb.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/hello_dlstreamer">Hello DL Streamer</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Build a detection pipeline, analyze metadata to count objects, and visualize results.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvawatermark</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo11n</code></p>
  </div>
</div>

### Customization & extensibility

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Custom Post-Processing Library — Classification](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/custom_postproc/classify">Custom Post-Processing Library — Classification</a></strong> <code>CLI</code>, <code>C++</code></p>
    <p style="margin:0.15rem 0;">Write a custom post-processing library that converts emotion-classification outputs to GstAnalytics metadata.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>centerface</code>, <code>hsemotion</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Custom Post-Processing Library — Detection](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/custom_postproc/detect">Custom Post-Processing Library — Detection</a></strong> <code>CLI</code>, <code>C++</code></p>
    <p style="margin:0.15rem 0;">Write a custom post-processing library that converts YOLOv11 tensor outputs to detection metadata.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo11s</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![gvapython — Face Detection and Classification](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvapython/face_detection_and_classification">gvapython — Face Detection and Classification</a></strong> <code>CLI</code>, <code>Python</code></p>
    <p style="margin:0.15rem 0;">Customize a pipeline with a Python script for inference post-processing.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvapython</code>, <code>gvadetect</code>, <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>centerface</code>, <code>dima806_fairface_gender_image_detection</code>, <code>dima806_facial_age_image_detection</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![gvapython — Save Frames with ROI](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/gvapython/save_frames_with_ROI_only">gvapython — Save Frames with ROI</a></strong> <code>CLI</code>, <code>Python</code></p>
    <p style="margin:0.15rem 0;">Use <code>gvapython</code> to save video frames containing detected objects to disk.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvapython</code>, <code>gvadetect</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>centerface</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![python-elements — Face Detection and Classification](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/python-elements/face_detection_and_classification">python-elements — Face Detection and Classification</a></strong> <code>CLI</code>, <code>Python</code></p>
    <p style="margin:0.15rem 0;">Build a custom Python GStreamer element using the GstAnalytics metadata API.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvaagelogger_py</code>, <code>gvadetect</code>, <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>YOLOv8-Face-Detection</code>, <code>fairface_age_image_detection</code>, <code>fairface_gender_image_detection</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![python-elements — Save Frames with ROI](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/python-elements/save_frames_with_ROI_only">python-elements — Save Frames with ROI</a></strong> <code>CLI</code>, <code>Python</code></p>
    <p style="margin:0.15rem 0;">Build a custom Python GStreamer element to save frames with detected objects.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvaframesaver_py</code>, <code>gvadetect</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>YOLOv8-Face-Detection</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![python-elements — Loitering Detection](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/gst_launch/python-elements/loitering_detection">python-elements — Loitering Detection</a></strong> <code>CLI</code>, <code>Python</code></p>
    <p style="margin:0.15rem 0;">Measure object dwell time with a custom Python element and render a visual alert when the threshold is exceeded.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvaanalytics</code>, <code>gvawatermark</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo11s</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Face Detection and Classification (Python)](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/face_detection_and_classification">Face Detection and Classification (Python)</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Download models from Hugging Face, export to OpenVINO IR, and run inference.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>YOLOv8-Face-Detection</code>, <code>fairface</code></p>
  </div>
</div>

### Performance & benchmarking

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Benchmark](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/benchmark">Benchmark</a></strong> <code>CLI</code>, <code>Python</code></p>
    <p style="margin:0.15rem 0;">Measure the performance of single- or multi-channel video analytics pipelines.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvafpscounter</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>centerface</code> (configurable)</p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![DL Streamer E2E Performance](../_images/sample-e2e-performance-thumb.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/e2e_performance">DL Streamer E2E Performance</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Compare DL Streamer vs. OpenCV + OpenVINO throughput with a YOLO26s INT8 model.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo26s</code> (INT8)</p>
  </div>
</div>

### Interoperability

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![DL Streamer and DeepStream Coexistence](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/coexistence">DL Streamer and DeepStream Coexistence</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Run pipelines on DL Streamer and/or NVIDIA DeepStream side by side.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolov8</code> license-plate detector, <code>PP-OCRv4</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Coexistence Benchmark](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/gstreamer/python/coexistence_benchmark">Coexistence Benchmark</a></strong> <code>Python</code></p>
    <p style="margin:0.15rem 0;">Measure the maximum number of concurrent LPR streams on systems combining Intel and NVIDIA hardware.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolov8</code> license-plate detector, <code>PP-OCRv4</code></p>
  </div>
</div>

---

## Auto-generated reference applications

These end-to-end reference apps combine multiple elements into complete solutions.
Find them under
[samples/auto_generated_samples](https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples).

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![DeepStream Test4 → DL Streamer Conversion](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/deepstream_python_conversion">DeepStream Test4 → DL Streamer Conversion</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">DL Streamer equivalent of NVIDIA's deepstream-test4 with YOLO11n detection and metadata publishing.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvametaconvert</code>, <code>gvametapublish</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo11n</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![DeepStream LPR App Conversion (C++)](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/deepstream_cpp_conversion">DeepStream LPR App Conversion (C++)</a></strong> <code>C++</code></p>
    <p style="margin:0.15rem 0;">C++ conversion of NVIDIA's DeepStream LPR app — license plate detection, tracking and text recognition.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvatrack</code>, <code>gvaclassify</code> &nbsp;|&nbsp; <strong>Models:</strong> YOLOv11, PaddleOCR</p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![License Plate Recognition](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/license_plate_recognition">License Plate Recognition</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Detect license plates with YOLOv11 and recognize text with PaddleOCR.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvainference</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>YOLOv11</code>, <code>PaddleOCR</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Multi-Stream Compose](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/multi_stream_compose">Multi-Stream Compose</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Multi-camera analytics with composite WebRTC output, on-demand recording and a 2x2 GPU-accelerated mosaic.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvastreammux</code>, <code>gvawatermark</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo11s</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![People Detection and Tracking with Deep SORT](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/people_detection_tracking">People Detection and Tracking with Deep SORT</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Detect and track people using YOLO26m and Deep SORT with a Mars-Small-128 re-ID model.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvatrack</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo26m</code>, <code>mars-small128</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Pose Estimation Compose](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/pose_estimation_compose">Pose Estimation Compose</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Run 4 YOLO pose models in parallel on the same video and composite results into a 2x2 mosaic.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvaclassify</code>, <code>gvawatermark</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo26n-pose</code>, <code>yolo11n-pose</code>, <code>yolov8n-pose</code>, <code>yolov8l-pose</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Safety Compliance Monitor](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/safety_compliance">Safety Compliance Monitor</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Detect and track workers and use Qwen2.5-VL to verify helmet and harness compliance.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code>, <code>gvatrack</code>, <code>gvagenai</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo26m</code>, <code>Qwen2.5-VL-3B</code></p>
  </div>
</div>

<div style="display:flex; gap:1rem; align-items:center; margin:0.5rem 0; padding-bottom:0.5rem; border-bottom:1px solid #4443;">
  <div style="flex:0 0 96px; max-width:96px;">

  ![Smart NVR — Event-Based Recording](../_images/sample_app_template.jpg)

  </div>
  <div style="flex:1; line-height:1.35;">
    <p style="margin:0 0 0.2rem;"><strong><a href="https://github.com/open-edge-platform/dlstreamer/tree/main/samples/auto_generated_samples/smart_nvr">Smart NVR — Event-Based Recording</a></strong> <code>CLI</code></p>
    <p style="margin:0.15rem 0;">Detect people with YOLO11n and record video only when a person is present.</p>
    <p style="margin:0.15rem 0; font-size:0.9rem; color:#888;"><strong>Elements:</strong> <code>gvadetect</code> &nbsp;|&nbsp; <strong>Models:</strong> <code>yolo11n</code></p>
  </div>
</div>
