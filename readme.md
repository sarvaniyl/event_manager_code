# User Management System - Bug Fix Project

This repository contains bug fixes for a user management system, focusing on improving data validation, enhancing security, and addressing potential bugs in the codebase.

## Resolved Issues

The following issues have been identified and resolved:

1. [Password Validation](https://github.com/sarvaniyl/event_manager_code/issues/1) - Implemented comprehensive password strength validation with requirements for minimum length, uppercase, lowercase, digits, and special characters.  [code](app\schemas\user_schemas.py)


2. [Username Validation (Nickname)](https://github.com/sarvaniyl/event_manager_code/issues/3) - Added functionality to check for nickname uniqueness during user profile updates to prevent duplicate nicknames.
 [code](app\services\user_service.py)


3. [Password Handling During Updates](https://github.com/sarvaniyl/event_manager_code/issues/5) - Fixed a method call bug in the update service and added password validation to the update schema.
 [code](app\schemas\user_schemas.py)

4. [Profile Field Edge Case - URL Validation](https://github.com/sarvaniyl/event_manager_code/issues/9) - Enhanced URL validation with a more comprehensive regex pattern and automatic addition of https scheme when missing.  [code](app\schemas\user_schemas.py)

5. [Profile Field Edge Case - Bio Length](https://github.com/sarvaniyl/event_manager_code/issues/7) - Added validation to ensure bio text doesn't exceed the 500-character database limit.
 [code](app\schemas\user_schemas.py)

## Docker Image
The project image has been deployed to DockerHub and is available at:
[docker.io/sarvani07/event_manager_code:latest](https://hub.docker.com/repository/docker/sarvani07/event_manager_code/tags)

## Reflection

Throughout this project, I gained valuable experience in identifying and fixing security vulnerabilities and edge cases in a user management system. Working with FastAPI and SQLAlchemy in an asynchronous environment presented unique challenges, particularly when implementing proper validation for user data. I learned the importance of comprehensive input validation not only at the schema level but also at the service level, especially for operations like updates where uniqueness constraints need to be enforced.

The most challenging aspect was implementing robust password validation while maintaining good user experience. Finding the right balance between security requirements (complexity, length) and usability was critical. I also gained insights into proper URL validation, which is more complex than it initially appears due to the variety of valid URL formats. This project reinforced the principle that security is a multi-layered concern that needs to be addressed at various levels of the application.

From a collaborative perspective, working with Git and following a structured issue-based workflow improved my project management skills. Breaking down problems into discrete, well-documented issues made the development process more manageable and created a clear record of changes for team members. The practice of writing detailed issue documentation and creating focused test cases for each issue has strengthened my ability to communicate technical solutions effectively, which I believe is essential for successful team collaboration in software development.