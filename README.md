# Fill Colors

A Django web application that automatically colorizes black-and-white images using AI.

## Features

- Upload black-and-white images
- AI-powered automatic colorization using Replicate API
- Asynchronous processing with webhook callbacks
- Simple and clean web interface

## How it Works

1. Upload a black-and-white image through the web interface
2. The image is sent to Replicate's AI colorization model
3. Results are received via webhook callbacks
4. View and download your colorized image

## Prerequisites

- Python 3.8+
- Django
- Replicate API account
- ngrok (for local development)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/navdeep545/Fill-colors.git
cd Fill-colors
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Set up environment variables:
```bash
export REPLICATE_API_TOKEN=your_replicate_api_token
export WEBHOOK_SECRET=your_webhook_secret
```

4. Run migrations:
```bash
python manage.py migrate
```

5. Start the development server:
```bash
python manage.py runserver
```

6. In another terminal, start ngrok to expose your local server:
```bash
ngrok http 8000
```

## Usage

1. Open your browser and navigate to the application
2. Upload a black-and-white image
3. Wait for the AI to process and colorize your image
4. Download the colorized result

## Configuration

The application uses webhooks to receive results from Replicate. Make sure to:

- Configure your Replicate webhook URL to point to your ngrok tunnel
- Set up proper webhook authentication using secret keys

## Contributing

Feel free to submit issues and pull requests.

## License

This project is open source and available under the MIT License.
