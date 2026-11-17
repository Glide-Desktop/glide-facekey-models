# FaceKey models

The recognition models and the ONNX Runtime build that
[FaceKey](https://github.com/Glide-Desktop/glide-auth) (`glide-facekey`) loads.
The `glide-facekey-models` package installs them where FaceKey looks:

| File | Installed to | What it does |
|---|---|---|
| `models/face_detection_yunet_2023mar.onnx` | `/usr/share/glide/face/` | face detection (YuNet, OpenCV Zoo) |
| `models/2d106det.onnx` | `/usr/share/glide/face/` | 106 facial landmarks (InsightFace) |
| `models/ghostfacenet_v1_w1.3_s1_ms1mv3.onnx` | `/usr/share/glide/face/` | face embeddings (GhostFaceNet) |
| `models/MiniFASNetV2.onnx` | `/usr/share/glide/face/` | anti-spoofing (Silent-Face-Anti-Spoofing) |
| `lib/libonnxruntime.so.1.20.1` | `/usr/lib/glide/face/libonnxruntime.so` | ONNX Runtime 1.20.1 (Microsoft, MIT), the version FaceKey's `ort` 2.0.0-rc.9 is built against |

The files are unmodified copies of the upstream releases. Their licences have
not been checked here; InsightFace's models in particular may be limited to
non-commercial research use. Check each upstream licence before redistributing
them further.
