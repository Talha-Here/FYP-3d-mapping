# 3D Mapping Of Buildings For Inspection

## Description
This project focuses on synchronizing video recordings with Inertial Measurement Unit (IMU) data using the [OpenCamera Sensors](https://github.com/prime-slam/OpenCamera-Sensors) Android app. The collected data (videos and IMU readings) are uploaded to a dedicated website, where they are stored in [Firebase](https://firebase.google.com/). The backend then downloads the data, extracts frames from the video, and downscales both the frames and IMU data to match timestamps. The downscaled frames are utilized to reconstruct a 3D model using Structure from Motion (SfM) techniques, and camera poses are estimated from the IMU data.

The system then assesses the scale consistency of the reconstructed model, calculating the scale factor using the reconstructed data and camera poses. This factor is incorporated into the 3D model, which is formatted for visualization and made available to the frontend.

![image](https://miro.medium.com/v2/resize:fit:3840/1*Up2Dqt9zmwohz6GYVbyy1Q.png)

## Project Flow
1. **Data Collection:**  
   Use the "OpenCamera Sensors" Android app to record synchronized video and IMU data.
   
2. **Data Upload:**  
   Upload the recorded data to the project website where it's stored in Firebase.

3. **Backend Processing:**  
   - Download and process the video and IMU data.
   - Extract frames from the video.
   - Downsample both the frames and IMU data to align timestamps.

4. **3D Reconstruction:**  
   Use Structure from Motion (SfM) techniques to reconstruct a 3D model from the frames.  
   Estimate camera poses from the downsampled IMU data.

5. **Scale Estimation:**  
   Estimate scale consistency using the camera poses and reconstructed model.  
   Calculate the scale factor and integrate it into the 3D model.

6. **Model Output:**  
   Convert the 3D model into a format suitable for visualization on the frontend.

## Usage
1. **Recording:**  
   Record video synchronized with IMU data using the "OpenCamera Sensors" app.
   
2. **Upload:**  
   Upload the recorded data to the project website.
   
3. **Visualization:**  
   After backend processing, the 3D model will be available for visualization on the website.

## Repositories
- **Backend Repository:**  
  [Backend Code Repository](https://github.com/Talha-Here/3d-Reconstruction-FYP)  
  *Note: This repository might be private due to patent-pending features.*

- **Frontend Repository:**  
  [Frontend Code Repository](https://github.com/Talha-Here/FYP-3D-Frontend)

![image](https://github.com/user-attachments/assets/9adbc947-6a43-415b-ad5d-e54c7a18d090)


## Notice
This project is in active development. We are continuously adding features, improving the performance, and fixing bugs. Please check back for updates. If you have suggestions or would like to contribute, feel free to open an issue or submit a pull request.

