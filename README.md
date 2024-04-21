# Google Forms Quiz Generator

## Overview
This project consists of a Google Apps Script that automates the creation of quizzes in Google Forms using AI to generate the questions. It reads specified inputs such as the number of questions, topic, and level from a Google Form, generates questions accordingly, and then creates a new Google Form quiz, ready for distribution.

## Technologies
- **Google Apps Script**: A scripting platform developed by Google for light-weight application development in the G Suite platform.
- **Google Sheets**: Part of Google Workspace, used for the input data storage and manipulation.
- **Google Forms**: Used to create and distribute quizzes automatically via script.

## Setup
To deploy and run this script, follow these steps:
1. **Google Form Setup**:
   - Create a Google Form intended to collect three inputs: the number of questions, topic, and level. There is a screenshot of my form for reference.
2. **Google Sheets Setup**:
   - The first time you respond, a Google Sheet is generated.
3. **Get an OpenAI API key**
   - See below
4. **Script Deployment**:
   - Open the Google Form and navigate to `Script editor` from the settings menu (three vertical dots).
   - Copy and paste the provided script into the script editor.
   - Replace `API key` with your actual OpenAI API key.
   - Setup the Trigger (See below)
   - Save and run the script to authorize and execute initial setup.

## Prerequisites
- **Google Account**: Required to access Google Forms, Google Sheets, and Google Apps Script.
- **OpenAI API key**
- **Knowledge of Google Apps Script**: Basic understanding of scripting with Google Apps Script for custom modifications.
- **Access to Google Workspace**: Ensure you have permissions to create and edit Forms and Sheets within your Google account or workspace environment.

## Steps to Get an API Key from OpenAI

Follow these steps to obtain an API key from OpenAI, which you'll need to authenticate requests to their API:

### 1. Create an OpenAI Account
- **Visit** [OpenAI’s website](https://www.openai.com/) and sign up for an account if you do not already have one.

### 2. Apply for API Access
- **Navigate** to the API section, typically found in your account or dashboard area, or directly go to [OpenAI API](https://platform.openai.com/signup).
- **Follow** the process to apply for API access. Depending on the current policies, this may involve a waitlist or immediate setup.

### 3. Set Up Billing (if required)
- **Note**: Some usage of OpenAI's API, especially for production-level use or high-volume requests, may require setting up billing. Provide payment information if necessary.

### 4. Retrieve Your API Key
- **Access** your API dashboard after your access is approved. Here, you can find your API key, which is used to authenticate your API requests.

### 5. Secure Your API Key
- **Keep** your API key secure and do not share it publicly. Use environment variables or secure app settings to store it in your projects.

## Trigger Setup

### Creating a Trigger for Form Submissions
1. **Open the Script Editor** from your Google Form.
2. Click on the **Clock icon** on the left panel to open the Triggers page.
3. Click **+ Add Trigger** in the bottom right.
4. Choose the function you want to trigger from the dropdown (e.g., `processData`).
5. Set the event source to **From form**.
6. Choose the trigger type, such as **On form submit**.
7. Click **Save** to activate the trigger.

### Usage Instructions
- **To Generate a Quiz**: Fill out the Google Form linked with this script with the required information about the quiz. The script will automatically generate a new Google Form quiz based on the latest form submission.
- **To Access Generated Quizzes**: Check the console log in the Google Apps Script editor for URLs of generated quizzes or refresh you Google Drive

This README outlines how to set up and use the Google Forms Quiz Generator script. Adjust the script and deployment details as per your specific needs and Google Workspace environment.
