# YouTube-Like Platform

This project is a YouTube-like platform with features such as video upload, transcoding, and adaptive bitrate streaming. It leverages AWS S3 for storage, Kafka for message handling, Node.js for the backend, and Next.js for the frontend.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [System Design](#system-design)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Services](#services)
  - [Upload Service](#upload-service)
  - [Watch Service](#watch-service)
  - [Transcoder Service](#transcoder-service)
- [License](#license)

## Features
- Video upload with chunking and multi-part upload to AWS S3
- User authentication using OAuth (Google Sign-In)
- Video transcoding for adaptive bitrate streaming
- Secure video storage with signed URLs
- Database integration for storing video metadata
- Frontend for uploading, listing, and watching videos

## Technologies Used
- **Node.js**: Backend framework
- **Next.js**: Frontend framework
- **AWS S3**: Storage service
- **Kafka**: Message broker for handling video processing tasks
- **PostgreSQL**: Database for storing video metadata
- **FFMPEG**: Tool for video transcoding
- **OAuth**: User authentication

## System Design
The system consists of three main services:
1. **Upload Service**: Handles video uploads from the frontend, processes them in chunks, and uploads them to S3.
2. **Watch Service**: Manages video playback, generates signed URLs for S3 files, and retrieves video details from the database.
3. **Transcoder Service**: Converts video files into multiple formats and bitrates for adaptive bitrate streaming.

## Setup and Installation
### Prerequisites
- Node.js
- PostgreSQL
- AWS S3 bucket
- Kafka server


# Installation

Follow the steps below to install and setup the project:

1. **Clone the repository**

   Open your terminal and run the following command:

   ```bash
   git clone https://github.com/geekychandan/DocTalk.git
   ```

3. **Install Node.js**

   The project requires Node.js version 13.4.19 or later. You can download it from [here](https://nodejs.org/en/download/).

4. **Install the required dependencies**

   Run the following command to install all the required dependencies:

   ```bash
   npm install
   ```

   This will install all the dependencies listed in the `package.json` file, including Next.js, React, React DOM, Axios, Stripe, Tailwind CSS, and other specific dependencies.

5. **Setup environment variables**

    Create a `.env` file in the root directory of your project and add the required environment variables.

6. **Run the project**

    Now, you can run the project using the following command:

    ```bash
    npm run dev
    ```

  ## Services

    **Upload Service**
    -*Chunking*: Splits video files into chunks on the client side.
    -*Multi-Part Upload*: Uploads video chunks to S3 and reassembles them into a single file.

    **Watch Service**
    -*Signed URLs*: Generates signed URLs for secure video playback.
    -*Database Integration*: Retrieves video details from PostgreSQL.

    **Transcoder Service**
    -*Video Transcoding*: Uses FFMPEG to convert videos into multiple bitrates and formats.
    -*Adaptive Bitrate Streaming*: Generates HLS and Dash manifests for adaptive streaming.


## Made By

- [@geekychandan](https://github.com/geekychandan)