# ollama-setup

Sure, I’ll help you create a well-structured README file for your GitHub repository. Here’s a template you can use:

## LLM Setup and Usage Guide

This repository contains instructions for setting up and using local large language models (LLMs) with the Ollama app on macOS. You will learn how to install the necessary software, run the models, and test them using curl commands or Postman.


## Table of Contents

1. [Introduction](#introduction)
2. [Setup Instructions](#setup-instructions)
   - [Prerequisites](#prerequisites)
   - [Installing Ollama App](#installing-ollama-app)
   - [Running Models](#running-models)
3. [Testing the Models](#testing-the-models)
   - [Using curl](#using-curl)
   - [Using Postman](#using-postman)
4. [Troubleshooting](#troubleshooting)
5. [Contributing](#contributing)
6. [License](#license)

## Introduction

This guide will walk you through the process of setting up and using two large language models, llama3 and phi3, using the Ollama app on macOS. You will learn how to run these models locally and test them with simple API requests.

## Setup Instructions

### Prerequisites

Before you begin, make sure you have the following:

	•	A macOS device
	•	Basic knowledge of terminal commands
	•	curl installed (usually pre-installed on macOS)
	•	Postman installed (optional, for API testing)


### Installing Ollama App

	1.	Download the Ollama app: You can download the Ollama app for macOS from the official website.
	2.	Install the app: Follow the on-screen instructions to install the Ollama app on your macOS device.


### Running Models

To run the models llama3 and phi3, use the following commands in your terminal:

	1.	Open your terminal.
	2.	Run the llama3 model:

```
ollama run llama3
```

	3.	Run the phi3 model:

```
ollama run phi3
```
Both models should now be running locally on your machine.


## Testing the Models

You can test the models using curl commands or by setting up API requests in Postman.

Using curl

	1.	Open your terminal.
	2.	Use the following curl command to test the llama3 model:

```
curl http://localhost:11434/api/chat -d '{
  "model": "llama3",
  "messages": [
    { "role": "user", "content": "why is the sky blue?" }
  ]
}'
```

### Using Postman

	1.	Open Postman.
	2.	Create a new POST request.
	3.	Set the URL to:

 ```http://localhost:11434/api/chat```
 	4.	In the body of the request, select raw and set the type to JSON. Enter the following JSON:
  
```
{
  "model": "llama3",
  "messages": [
    { "role": "user", "content": "why is the sky blue?" }
  ]
}
```

## Troubleshooting

If you encounter issues:

	•	Ensure the Ollama app is running and the models are started.
	•	Verify that your curl or Postman request is correctly formatted.
	•	Check your network settings to ensure no conflicts with port 11434.


## License

This project is licensed under the MIT License. See the LICENSE file for details.

Feel free to customize this template further to suit your needs. This README provides a clear guide for setting up, running, and testing the models using the Ollama app.
