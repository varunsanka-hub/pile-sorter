# ♻️ Pile Sorter — AI-Based Waste Segregation

**An AI-powered waste detection and classification system that identifies waste items from images and helps organize them into different categories.**

## 📌 About the Project

Pile Sorter is a browser-based application designed to detect and classify waste items using a trained deep-learning object detection model. Users can upload an image or use their camera to identify waste items and view their classifications through visual bounding boxes and category-wise counts.

The application runs inference directly in the browser using ONNX Runtime Web.

## 🎯 Objectives

- Detect individual waste items in a pile.
- Classify detected items into different waste categories.
- Display bounding boxes and confidence scores.
- Count the number of detected items in each category.
- Provide a simple, responsive interface for image-based waste analysis.
- Explore the use of AI for waste management and segregation.

## 🗂️ Waste Categories

The application supports the following categories:

| Category | Examples |
|---|---|
| Plastic | Bottles, bags, wrappers |
| Metal | Cans, foil, tins |
| Paper | Cardboard, cartons, sheets |
| Organic | Food scraps, fruit peels |
| Other | Items belonging to other waste categories |

*Actual classification performance depends on the trained model and the quality of the input image.*

## 🛠️ Technologies Used

- **HTML5** — Web page structure
- **CSS3** — Responsive interface and styling
- **JavaScript** — Application logic and image processing
- **YOLO26 Nano** — Waste object detection model, as identified by the application
- **ONNX** — Model format for inference
- **ONNX Runtime Web** — Runs model inference in the browser
- **WebAssembly (WASM)** — Supports browser-based model execution
- **GitHub** — Source-code management and team collaboration
- **Netlify** — Intended platform for public deployment

## 📁 Project Structure

```text
pile-sorter/
│
├── index.html
├── best.onnx
├── ort-wasm-simd-threaded.wasm
└── README.md
```

### File descriptions

- `index.html` — Main web application, user interface, and inference logic.
- `best.onnx` — Trained object detection model.
- `ort-wasm-simd-threaded.wasm` — WebAssembly runtime file used by the application.
- `README.md` — Project overview, setup instructions, and documentation.

## 🚀 Getting Started

### Prerequisites

You will need:
- A modern web browser.
- The project files listed above.
- An internet connection to load the ONNX Runtime JavaScript dependency from its CDN.

### Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/varunsanka/pile-sorter.git
   ```

2. Enter the project directory:

   ```bash
   cd pile-sorter
   ```

3. Start a local development server. If Python is installed, run:

   ```bash
   python -m http.server 8000
   ```

4. Open the following address in your browser:

   ```text
   http://localhost:8000
   ```

5. Wait for the model status to display **Model ready**.

6. Upload a waste image or use the camera to test the application.


## 💡 Features

- **Image Upload:** Upload a photo containing multiple waste items.
- **Camera Support:** Use a compatible camera to capture and analyze waste.
- **Object Detection:** Display bounding boxes around detected objects.
- **Confidence Threshold:** Adjust detection sensitivity.
- **Category-Wise Counting:** View the number of detected objects in each category.
- **Interactive Filtering:** Select a category to highlight its detections.
- **Browser-Based Inference:** The application is designed to process images locally without uploading them to a project server.

## 📊 Model Information

The supplied application identifies its model as YOLO26 Nano with a 640-pixel input size.

- **Model file:** `best.onnx`
- **Inference format:** ONNX
- **Execution provider:** WebAssembly
- **Input size:** 640 × 640 pixels
- **Training data described in the application:** TACO litter photos and an organic waste dataset
- **Validation metric reported in the application:** mAP50 = 0.31

The reported validation metric indicates that detection performance may be limited, especially for overlapping objects, cluttered scenes, and visually similar materials.

The training dataset details, class mapping, model evaluation, and licensing should be verified with the model provider before presenting the model as a validated waste-segregation system.

## 🌐 Deployment

The project is designed to be hosted as a static website in netlify.

### 🔗 Web Link 

Model is already deployed in chrome, Link: https://pilesorter.netlify.app/

## 👥 Team Collaboration

This project is maintained collaboratively through GitHub.

Team members can contribute by:
- Improving the user interface.
- Testing object detection on different waste images.
- Evaluating model performance.
- Improving documentation.
- Investigating model optimization and accessibility.
- Testing deployment across browsers and devices.

Repository owner: Varun Sivaram S

Team members:
- Shreenivas V S
- Munesh Chandra Rai
- Yuvan Tusuju

## 🔮 Future Improvements

- Improve model accuracy and detection reliability.
- Expand and balance the waste-image dataset.
- Evaluate performance under different lighting conditions.
- Add more waste categories where supported by suitable training data.
- Optimize inference speed for mobile devices.
- Improve accessibility and user guidance.
- Explore integration with robotic waste-segregation systems.
- Add quantitative evaluation using precision, recall, and per-class metrics.

## 🔒 Privacy

The supplied application is designed to run model inference in the browser. Its interface states that images are not uploaded. Verify this behaviour and any external dependencies before making formal privacy claims.

## ⚠️ Limitations

- Detection accuracy depends on the trained model.
- Small, obscured, or overlapping waste objects may be missed.
- Predictions should not be treated as guaranteed material identification.
- Browser performance varies across devices.
- The reported mAP50 value is not equivalent to classification accuracy.

## 📄 License

The license for the trained model, dataset, and application code has not yet been specified. Confirm that you have permission to redistribute all supplied files before selecting and publishing a license.

## 🙌 Acknowledgements

Thanks to the contributors who developed the web application and supplied the trained model.

The project also references the TACO litter dataset and an organic waste dataset, as described in the application. Appropriate dataset and model attribution should be added once the exact sources and licenses are confirmed.

---

**Pile Sorter — Using AI to support smarter waste segregation.** ♻️
