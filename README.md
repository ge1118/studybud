# StudyBuddy

## Project Overview
StudyBuddy is a collaborative platform built using Django and Python, designed to facilitate the creation of study rooms for learning various programming languages and development frameworks. It features user authentication, CRUD operations for rooms and messages, user profiles, a search function, and tracking of recent activities within rooms. This makes it easier for users to engage in active and focused study sessions. StudyBuddy leverages SQLite for database management and AWS S3 for serving static and media files, ensuring a robust and scalable user experience.

## Live Demo
Experience StudyBuddy live on Heroku: [StudyBuddy](https://studybuddy-1f2d333417a5.herokuapp.com/)

Feel free to register an account, explore existing study rooms, or create your own.

## Key Features
- User Authentication (Login, Register, Log Out)
- CRUD Functionality for Rooms and Messages
- User Profiles with Editable Features and Profile Picture Updates
- Search Functionality for Rooms, Messages, and Topics
- Recent Activity Tracking to Highlight Active Discussions
- Static and Media Files Served via AWS S3

## Technologies
- Python 3.12.1
- Django 5.0.1
- SQLite (Development)
- AWS S3 (Static and Media Storage)
- HTML, CSS, JavaScript (Frontend)
- Git (Version Control)
- Heroku (Deployment)
- requirements.txt (Dependency Management)

## Getting Started

### Prerequisites
- Python
- Django
- AWS Account for S3 Bucket Access
- Virtual Environment (recommended)

### Setup
1. Clone the repository
```
git clone https://github.com/ge1118/studybud.git
```

2. Set up a virtual environment
```
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. Install dependencies
```
pip install -r requirements.txt
```

4. Configure AWS S3 Bucket
- Create an AWS S3 bucket and note your bucket name and region.
- Configure your bucket for static and media file hosting.
- Create IAM credentials (access key ID and secret access key) with permissions to access the bucket.

5. Set up environment variables
- Copy .env.example to a new file named .env.
- Fill in the .env file with your specific values, including your Django SECRET_KEY, AWS credentials, and any other necessary configuration.
```
SECRET_KEY=your_secret_key_here
DEBUG=False  # Set to True for development
ALLOWED_HOSTS=.yourdomain.com,127.0.0.1

AWS_ACCESS_KEY_ID=your_aws_access_key_id_here
AWS_SECRET_ACCESS_KEY=your_aws_secret_access_key_here
AWS_STORAGE_BUCKET_NAME=your_aws_storage_bucket_name_here
AWS_S3_REGION_NAME=your_aws_s3_region_name_here
```

6. Database Migrations
```
python manage.py migrate
```

7. Run the Development Server
```
python manage.py runserver
```
Access the application at http://127.0.0.1:8000/.

## .env and .env.example
- .env: This file contains your project's environment-specific settings, including secret keys and credentials. It's crucial for the security of your project that this file is never committed to version control.
- .env.example: A template showcasing the required environment variables without actual values. This file should be committed to your repository to guide setup for other developers.

## AWS S3 Configuration
Static and media files in StudyBuddy are served via AWS S3. Ensure you have correctly set up your AWS S3 bucket and provided the necessary credentials in your .env file as described in the setup section.

## Contributing
Interested in contributing to StudyBuddy? We welcome contributions in the form of bug reports, feature requests, or pull requests. Please feel free to contribute!

## License
This project was inspired by [divanov11's StudyBud tutorial](https://github.com/divanov11/StudyBud/) and includes modifications and enhancements such as the integration of AWS services. This project is shared for educational purposes, and I've made improvements based on the tutorial content. No explicit license is applied to these modifications at this time. Please feel free to view and learn from the code.
