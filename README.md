# YogaIntelliJ - AI-Powered Yoga Pose Detection App

An intelligent yoga application that uses TensorFlow.js and MoveNet to detect and classify yoga poses in real-time through your webcam. Get instant feedback on your yoga practice with AI-powered pose recognition.

## 🧘 Features

- **Real-time Pose Detection**: Uses TensorFlow MoveNet model to detect body poses through webcam
- **Yoga Pose Classification**: Recognizes 8 different yoga poses:
  - Chair Pose
  - Cobra Pose
  - Downward Dog
  - Shoulder Stand
  - Triangle Pose
  - Tree Pose
  - Warrior Pose
  - No Pose (resting position)
- **Interactive UI**: Clean and intuitive React-based interface
- **Pose Instructions**: Step-by-step guidance for each yoga pose
- **Tutorials**: Learn proper form and technique
- **Real-time Feedback**: Get instant feedback on your pose accuracy

## 🛠️ Tech Stack

### Frontend
- **React** (v17.0.2) - UI framework
- **TensorFlow.js** (v3.10.0) - Machine learning in the browser
- **MoveNet** - Pose detection model
- **React Webcam** - Camera integration
- **React Router DOM** - Navigation

### Machine Learning
- **TensorFlow** - Model training
- **MoveNet Thunder** - Pre-trained pose detection model
- **Custom Classification Model** - Trained on 8 yoga poses
- **Python** - Model training and preprocessing

## 📋 Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Webcam
- Modern web browser (Chrome, Firefox, Edge)
- Python 3.x (for model training)

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/TejavathChakridhar/YogaIntelliJ.git
cd YogaIntelliJ
```

### 2. Frontend Setup

```bash
cd frontend
npm install
npm start
```

The app will open at `http://localhost:3000`

### 3. Classification Model (Optional - for training)

```bash
cd "classification model"
pip install tensorflow numpy pandas opencv-python
```

## 📁 Project Structure

```
YogaIntelliJ/
├── classification model/          # ML model training
│   ├── movenet_thunder.tflite    # MoveNet model
│   ├── training.py               # Model training script
│   ├── data.py                   # Data processing
│   ├── preprocessing.py          # Data preprocessing
│   ├── weights.best.hdf5         # Trained model weights
│   ├── model/                    # Saved model files
│   ├── csv_per_pose/            # Training data per pose
│   └── yoga_poses/              # Training images
│       ├── train/
│       └── test/
│
└── frontend/                     # React application
    ├── public/
    ├── src/
    │   ├── components/          # Reusable components
    │   │   ├── DropDown/
    │   │   ├── Instructions/
    │   │   └── PoseStart/
    │   ├── pages/              # Application pages
    │   │   ├── Home/
    │   │   ├── About/
    │   │   ├── Tutorials/
    │   │   └── Yoga/
    │   └── utils/              # Utility functions
    │       ├── data/
    │       ├── helper/
    │       ├── images/
    │       ├── music/
    │       └── pose_images/
    └── package.json
```

## 🎯 Usage

1. **Start the Application**
   ```bash
   cd frontend
   npm start
   ```

2. **Allow Camera Access**: When prompted, allow the browser to access your webcam

3. **Select a Pose**: Choose a yoga pose from the dropdown menu

4. **Follow Instructions**: Read the step-by-step instructions for the selected pose

5. **Start Practice**: Click "Start" to begin real-time pose detection

6. **Get Feedback**: The AI will analyze your pose and provide feedback

## 🏋️ Training Your Own Model

If you want to retrain the model with your own data:

1. Prepare your dataset in the `yoga_poses/train` and `yoga_poses/test` folders
2. Run the preprocessing script:
   ```bash
   python preprocessing.py
   ```
3. Train the model:
   ```bash
   python training.py
   ```
4. Copy the generated model files to the frontend

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).


## 🙏 Acknowledgments

- TensorFlow.js team for the amazing ML framework
- Google for the MoveNet model
- React community for the awesome framework
- All contributors and yoga enthusiasts

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.

---

**Note**: Make sure your webcam is properly connected and permissions are granted for the best experience!

Happy Yoga! 🧘‍♀️🧘‍♂️
