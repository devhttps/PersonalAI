# 🏋️‍♂️ AI Personal Trainer

An intelligent personal training system based on AI that uses computer vision to analyze posture, count exercises, and provide real-time feedback.

## ✨ Features

- **Posture Detection**: Analysis of 33 body points using MediaPipe
- **Automatic Counting**: Counts push-ups and other exercises automatically
- **Angle Analysis**: Calculates angles between joints to verify correct form
- **Web Interface**: Interactive dashboard with Streamlit for real-time visualization
- **Video Processing**: Support for video files (.MOV, .MP4)
- **Real-time Metrics**: Movement graphs and exercise statistics

## 🚀 Technologies Used

- **Python 3.11+**
- **MediaPipe** - AI framework for computer vision
- **OpenCV** - Video and image processing
- **Streamlit** - Interactive web interface
- **Pandas & NumPy** - Data manipulation and analysis
- **Matplotlib** - Data visualization

## 📋 Prerequisites

- Python 3.11 or higher
- Webcam or video file for analysis
- Internet connection for MediaPipe model download

## 🛠️ Installation

1. **Clone the repository**
```bash
git clone https://github.com/seu-usuario/ai-personal-trainer.git
cd ai-personal-trainer
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **MediaPipe model download**
The `pose_landmarker_full.task` model is already included in the repository.

## 🎯 How to Use

### 1. Basic Video Analysis
```bash
python pose_estimator.py
```

### 2. Complete AI System
```bash
python personal_ai.py
```

### 3. Web Interface (Recommended)
```bash
streamlit run personalai_dash.py
```

## 📁 Project Structure

```
AI Personal Trainer/
├── personal_ai.py              # Core AI system
├── personalai_dash.py          # Web interface with Streamlit
├── pose_estimator.py           # Basic detection module
├── pose_landmarker_full.task   # MediaPipe model
├── requirements.txt            # Python dependencies
├── IMG_2149.mov               # Example video
└── README.md                  # This file
```

## 🔧 Configuration

### Video Files
- Supported formats: `.MOV`, `.MP4`, `.AVI`
- Recommended resolution: 720p or higher
- Recommended FPS: 24-30 fps

### Monitored Body Points
- **Shoulders**: Points 11 (right) and 12 (left)
- **Hips**: Points 23 (right) and 24 (left)
- **Elbows**: Points 13 (right) and 14 (left)
- **Total**: 33 body points

## 📊 Analysis Features

### Exercise Detection
- **Push-ups**: Automatic counting based on elbow angles
- **States**: "relaxed", "ready", "up"/"down" direction
- **Metrics**: Real-time angles, repetition counter

### Visualization
- Body landmarks drawn on video
- Real-time angle display
- Movement graphs of body points
- Dashboard with statistics

## 🎮 Interface Controls

- **Display Charts**: Enable/disable movement graphs
- **Reset**: Restart counters and metrics
- **Status**: Show current exercise state
- **Count**: Display repetition count

## 🔍 Usage Examples

### Push-up Analysis
```python
from personal_ai import PersonalAI

# Initialize system
trainer = PersonalAI("your_video.mov")

# Process video
trainer.process_video(display=True)

# Run in background
trainer.run()
```

### Web Interface
```bash
# Start dashboard
streamlit run personalai_dash.py

# Access in browser
# http://localhost:8501
```

## 📈 Advanced Features

- **Asynchronous Processing**: Queue system for better performance
- **Multiple Exercises**: Support for different types of movements
- **Quality Analysis**: Verification of correct form and posture
- **Data Export**: Metrics saved for later analysis

## 🐛 Troubleshooting

### Error: "No module named 'mediapipe'"
```bash
pip install mediapipe --upgrade
```

### Error: "Error opening video stream or file"
- Check if video file exists
- Confirm correct path in code
- Test with different video formats

### Slow Performance
- Reduce video resolution
- Use GPU if available
- Adjust FPS for processing

## 🤝 Contributing

1. Fork the project
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is under the MIT license. See the `LICENSE` file for more details.

## 🙏 Acknowledgments

- **MediaPipe** for posture detection technology
- **Google** for the AI framework
- **Streamlit** for the web interface
- **Python Community** for support

## 📞 Contact

- **Author**: [Guilherme Gomes]
- **Email**: [guilherme@mymesh.com.br]
- **GitHub**: [@devhttps]
- **LinkedIn**: [https://www.linkedin.com/in/erro404/]

## 🔮 Roadmap

- [ ] Support for more exercises
- [ ] Advanced biomechanics analysis
- [ ] Wearable integration
- [ ] Mobile app
- [ ] REST API
- [ ] Custom Machine Learning

---

⭐ **If this project helped you, consider giving it a star on GitHub!**
