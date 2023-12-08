
# CSCI 567 - Indoor Fire Detection using CNNS
  
Aryan Pillai, Jeenisha Shrungare, Nouf Alsinan, Pranav Gangurde

## Drive Codebase Link ##

https://drive.google.com/drive/u/1/folders/0AKFVH_1P3xRuUk9PVA

## Operating Model File ##

### 1. Locating Colab File ###

From our project codebase in the google drive, open the given colab file depending on the model you want to run:   
Model 1: models/cnn_models_hsv/cnn_model_hsv.ipnyb  
Model 2: models/cnn_models_hsv/cnn_model.ipnyb   

### 2. Running the Colab notebook ###

In the colab file, you can run the prepocess, training and testing steps of the model by clicking "Runtime-->Run all" in the header bar.   
**Note:** Preprocessing and training the model takes a while due to the size of the dataset we are using for the model.

## Setting Up GUI Prediction System ##

### 1. Download the Project Codebase ###

Download all the files in the folder "Final Project" from the drive codebase to your local system. 

### 2. Download MySQL and XAMPP ###

Download and Install MySQL from the following link on your system:   
https://dev.mysql.com/downloads/mysql/   
    
Download and Install XAMPP for your system from the following link:   
https://www.apachefriends.org/download.html    
**Note:** This project works best on a Windows or Linux system

### 3. Install required Python Libraries ###

Install the necessary libraries for our project by running the following commands on your python terminal

```bash
pip install tk
pip install numpy
pip install keras
pip install opencv-python
pip install mysql-connector-python
```

### 4. Starting Apache and MySQL servers ###

Open "XAMPP Control Panel" from your applications list, and click on the start button for Apache and MySQL to start the respective servers on your system

### 5. Setting up the Database ###

In the database.py file in our project codebase, change the following code to match the configuration of mysql server on your system
```code
def __init__(self):
    mydb = mysql.connector.connect(
            host="localhost",
            user="root",
            passwd="password"
          )
```

```code
def getConnection(self):
    mydb = mysql.connector.connect(
        host="localhost",
        user="root",
        passwd="password",
        database="FireDatabase"
      )

    return mydb
```

To view and change your mysql credentials, visit www.localhost/phpmyadmin, and click on "user accounts" from the header bar

### 6. Setup the Video Simulation ###

To set up the video simulation on XAMPP, copy any video file given in the project codebase (Example: flashover_demonstration) and paste it in the folder that XAMPP is installed (Normaly C:\ in Windows).   
**Note:** Rename the video to simple words such as "firedemo" such that the later step is easy

### 7. Run the main.py python file ###

Once set up all requirements, you are free to run the "main.py" python file in our project codebase.    
After running the file, you will see our project GUI on your screen.   
1. First, Click on "Add new Camera" and enter the ID(any ID) and link of your uploaded video Simulation(localhost/video-name).   
2. Next, Turn On the model based predication system by clicking "Turn On".   
3. Finally, you will see your new room camera online (in green). You can start viewing the simulated video by clicking "watch"

### We have also 
