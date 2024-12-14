# AI-Powered Learning Assistant for Disabled Students

## Project Overview

### Why This Topic Was Selected?

In today's world, accessibility is a key factor in ensuring that everyone has equal opportunities for learning and communication. For disabled students, especially those with hearing or speech impairments, traditional methods of communication can be a significant barrier to education. The **AI-Powered Learning Assistant for Disabled Students** was developed to help overcome these barriers by offering a tool that can recognize sign language gestures and convert speech to text, making learning more accessible and interactive. 

This project focuses on building an AI-powered assistant that integrates multiple technologies to recognize sign language gestures, convert spoken language into text, and display the corresponding signs. By combining these features, this assistant can provide an inclusive educational environment for disabled students, aiding their communication with both machines and humans.


## Dataset

The dataset used for gesture recognition is the **ASL Alphabet Dataset**, which contains images of the 26 letters of the American Sign Language (ASL) alphabet. The dataset has been provided in a zip file (`asl_alphabet_test.zip`). It includes folders of images labeled by each letter (A-Z). This project does not include training or preprocessing steps, and assumes that the dataset is available for testing the gesture recognition part.

- **Dataset File**: [asl_alphabet_test.zip](asl_alphabet_test.zip)

## Detailed Steps Followed

### 1. Speech-to-Text (Speech Recognition)

The first step in the project involves converting spoken language into text. This feature was implemented using the `SpeechRecognition` library, which listens to audio from the microphone and converts it into text.

- **Process**: The microphone is used to capture audio input, which is then sent to the `SpeechRecognition` API. If speech is detected, the API converts it into text. If the speech is unclear or cannot be recognized, an error message is displayed.
- **Purpose**: This functionality allows the system to recognize speech and convert it into text, helping students with speech disabilities to interact with the application through voice commands.

### 2. Hand Gesture Recognition Using MediaPipe

The second part of the project uses **MediaPipe**, a library developed by Google, to detect and recognize hand gestures in real-time. The hand gestures are recognized as part of the **American Sign Language (ASL)** alphabet.

- **Process**: The webcam is used to capture live video frames. Each frame is processed using MediaPipe’s hand detection solution to detect hand landmarks (such as fingers, palms, etc.). The detected landmarks are then used to identify specific gestures corresponding to the ASL alphabet.
- **Purpose**: This step provides gesture-based interaction for users to communicate using sign language. It helps bridge the communication gap for users who cannot speak or hear, allowing them to input gestures that the system can understand and convert into text.

![Alt Text](Screenshot%202024-12-14%20085146.png)
![Alt Text](Screenshot%202024-12-14%20085414.png)
![Alt Text](Screenshot%202024-12-14%20085459.png)


### 3. Text-to-Sign Language Conversion

The final component of the project converts text into sign language gestures. This is done by mapping each character of the input text to its corresponding ASL gesture.

- **Process**: The program receives a string of text (e.g., "Hello"). For each letter in the text, the system looks up the corresponding image of the ASL letter from the dataset and displays it. This allows the system to show the user how to make the corresponding sign language gesture for each letter.
- **Purpose**: This feature is designed to convert text into sign language for users who might prefer or need visual representations of the text. It aims to support users who are learning sign language and provide a visual learning tool.

