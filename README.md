# Food Tray Detection with Computer Vision

**Stack:** Python · OpenCV · Object Detection · Computer Vision

An object-detection pipeline that finds and classifies food items on a tray from a standard camera image. The project covers dataset preparation, the detection pipeline, the evaluation method, and a documented account of where the model is reliable and where it is not.

---

## 1. Overview

Counting or checking items on a food tray by hand is slow and inconsistent. This project takes an ordinary camera image of a tray and detects the food items on it, returning each item's class and bounding box.

The emphasis is on an honest build: the pipeline works from a standard camera image rather than a controlled lab setup, and the documentation states the conditions under which it is reliable instead of claiming a single universal accuracy figure.

## 2. Problem

Manual tray checking is slow and error-prone. Two constraints shaped the design:

- **Ordinary input.** The detector has to work from a standard camera image, not a specialised sensor or a controlled lighting rig.
- **Honest evaluation.** Performance depends heavily on dataset and camera conditions, so the project documents its limits rather than quoting one number out of context.

## 3. Approach

The pipeline is built in Python with OpenCV and follows four stages:

1. **Dataset preparation.** Collected and structured an image dataset for tray-item detection, with per-item class labels and bounding-box annotations.
2. **Detection pipeline.** Built the detection stage in Python and OpenCV to locate and classify food items in a tray image.
3. **Evaluation method.** Defined an evaluation method that scores detection quality per class, so weak classes are visible rather than averaged away.
4. **Failure documentation.** Recorded where the model is reliable and where it is not — including the camera conditions and dataset properties that drive the difference.

## 4. Tech Stack

| Component | Choice |
|-----------|--------|
| Language | Python |
| Vision library | OpenCV |
| Task | Object detection / classification |

## 5. Results

- End-to-end pipeline from prepared dataset to evaluated detection output.
- Per-class evaluation that surfaces which items are detected reliably and which are not.

> **Note on accuracy.** This project deliberately does not quote a single headline accuracy number. Detection performance depends on the dataset and camera conditions used, and the project documentation states those limits rather than claiming universal accuracy.

## 6. Limitations

Performance depends on the dataset and camera conditions used. Results will not generalise unchanged to different lighting, camera angles, tray types, or food categories that were not represented in the training data.

## 7. Repository Status

The accompanying codebase — dataset loaders, the detection pipeline, and the evaluation script — is being prepared for publication. This README documents the project's design, method, and stated limits.

---

## Getting Started (planned)

```
# Environment (planned)
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

# Run detection on a tray image (planned)
python detect.py --image path/to/tray.jpg
```

## License

Add a license before publishing this repository.
