I Built a Real-Time Number Plate Detector with Python and OpenCV, and You Can Too: Detailed Guide
Real-Time Number Plate Detection using OpenCV
This project uses Python and OpenCV to detect car number plates in real-time from a webcam feed. It identifies the plate region, draws a bounding box around it, and offers the functionality to save the detected plate as an image.

🚀 Key Features
Real-Time Detection: Utilizes your webcam to detect number plates in a live video stream.

Visual Feedback: Draws a bounding box around detected plates and displays the cropped Region of Interest (ROI) in a separate window.

Save Plates: Allows you to save the cropped image of a detected number plate with a simple key press ('s').

📸 Demo
Here’s a quick look at the script in action.

Before Detection: The original input from the webcam.
(You can add your 'before' image here)

After Detection: The script successfully identifies the number plate and draws a bounding box.
(You can add your 'after' image here)

🛠️ Technologies Used
Python 3.9


OpenCV: The core library used for all computer vision tasks.

Haar Cascade Classifier: A pre-trained model for detecting Russian number plates (haarcascade_russian_plate_number.xml).

⚙️ Setup and Usage
Follow these steps to get the project running on your local machine.

1. Prerequisites
Conda package manager installed.

2. Installation & Setup
First, clone the repository to your local machine:

Bash

git clone https://github.com/your-username/Car-Number-Plates-Detection.git
cd Car-Number-Plates-Detection
Next, create and activate a Conda virtual environment. This keeps the project's dependencies isolated.

Bash

# Create the environment
conda create -p ./venv python=3.9 -y

# Activate the environment
conda activate ./venv
Finally, install the required Python packages from the requirements.txt file.

Bash

pip install -r requirements.txt
3. Running the Script
Once the setup is complete, you can run the main detection script with the following command:

Bash

python number_plate.py
4. How to Use
A window will open showing your webcam feed.

Point the camera towards a vehicle's number plate.

The script will draw a green rectangle around any detected plates.

Press the 's' key to save the currently detected plate image to the plates/ directory.

Press the 'q' key to quit the program.

📄 How It Works
The number_plate.py script performs the following steps in a continuous loop:

Capture Frame: Reads a frame from the webcam.

Grayscale Conversion: Converts the color image to grayscale, as Haar Cascades work more efficiently on single-channel images.

Detect Plates: Uses the pre-trained haarcascade_russian_plate_number.xml classifier to detect plates in the grayscale image. The detectMultiScale function returns the coordinates of any detected plates.

Draw Bounding Box: For each detected plate, it draws a green rectangle on the original color frame.

Display ROI: It crops the detected plate (Region of Interest) and displays it in a separate window.

Save on Command: If the 's' key is pressed, the script saves the ROI to a file.

📜 License
This project is licensed under the MIT License. See the 

LICENSE file for more details.
