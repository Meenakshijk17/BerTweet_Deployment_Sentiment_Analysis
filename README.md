# Sentiment Analysis
Sentiment analysis categorizes text into positive, negative, or neutral sentiments.

## Objective

Develop an Automated Sentiment Analysis tool to predict sentiment and confidence scores in real-time via a web API, capable of handling multiple requests concurrently.

## Approach

  1. __Model__:  Utilize [Bertweet]((https://huggingface.co/finiteautomata/bertweet-base-sentiment-analysis?text=I+like+you.+I+love+you)), a [Roberta](https://arxiv.org/abs/1907.11692) model trained on the SemEval 2017 corpus for tweet sentiment analysis, leveraging Hugging Face's pipeline functionality for easy integration.
  
  2. __Flask__: Create a simple web app with Flask to provide a user interface for text input and result display.

  3. __Nginx__ and __Gunicorn__ : Optimize deployment with Nginx as a reverse proxy and Gunicorn as the application server, facilitating efficient handling of multiple requests.
   
  4. __Docker__ : Dockerize the components for portability and scalability, ensuring consistent performance across environments.

## Get Started
   
1. ```docker-compose up -d --build --scale app = 5```
   This command triggers Docker build. "*--scale app=5*" determines the number of containers running concurrently, adjustable for varying demand. Techniques like locust can further assess application responsiveness under load.
