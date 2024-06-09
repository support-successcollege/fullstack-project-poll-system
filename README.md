# Polls System - Backend Implementation

*This project constitutes 15% of the final grade. A passing grade is 70 or above.*

## Submission Requirements:
1. Follow all instructions and build the project accordingly.
2. Prepare a test file containing screenshots as per the requirements detailed below.

## Instructions:

Your mission is to create a poll system that will be used to ask the company customers any questions they want and process calculations about the data.

### Example Questions:
1. **Between the following, what do you most love to do?**
   - a. Watch TV
   - b. Play the computer
   - c. Hanging out with friends
   - d. Travel the world

2. **Where is your preferred place to travel?**
   - a. USA
   - b. France
   - c. South America
   - d. Thailand

### Services:

#### User Service
Responsible for saving all the data about system users, including:
- Unique user id
- User first name
- User last name
- User email
- User age
- User address
- User joining date

Only registered users can answer poll questions. If a user is not registered, they cannot submit answers. If a user deletes themselves from the system, all their answers should also be deleted.

**CRUD Implementation:**
- Create a user
- Update a user
- Delete a user
- Get user info

#### Poll Service
Responsible for saving all poll questions and user answers for each question. Each question is a multiple-choice question with four options.

**Poll Question Data:**
- Unique question id
- Question title
- First answer option
- Second answer option
- Third answer option
- Fourth answer option

**CRUD Implementation:**
- Create a question
- Update a question
- Delete a question
- Get question info

**Additional Requirements:**
- Save user answers to each question
- Support for scenarios where not all users answer all questions or some questions have no answers

### API Requirements:
- By question id:
  - Return how many users chose each option
  - Return the total number of users who answered the question
- By user id:
  - Return the user's answers to each question
  - Return the number of questions the user answered
- Return all questions and the number of users who chose each option for each question

**Implementation Notes:**
- Backend only, no UI needed
- Use Java and Spring Boot framework
- Use H2 database
- Follow best practices learned in the course
  - Use MVC architecture (Controller, Service, Repository)
  - Use configuration when needed
  - Write valid Java class names and SQL table names
  - Use the Request to Response flow as learned in class

**Service Communication:**
- Services should communicate using the API endpoints created
- Each service should connect to its own H2 database and save relevant data

## Test File: (Screenshots/Video)

At the end of the project, before submission, go through all the guidelines below and add to the project a directory named "tests" containing all the necessary images.

* No code screenshots are needed, only screenshots of requests that worked (including error-handling requests that do not crash the server).

1. **Full CRUD support for users:**
   - Create a user (screenshot)
   - Update a user (screenshot)
   - Delete a user (screenshot)
   - Get user info (screenshot)

2. **Full CRUD support for questions:**
   - Create a question (screenshot)
   - Update a question (screenshot)
   - Delete a question (screenshot)
   - Get question info (screenshot)

3. **Saving user answers to poll questions (show that results are saved)**

4. **Error handling such as lack of answers for all questions (screenshots)**

5. **Statistical information on user answers: (screenshot of the request that worked, not the code)**
   - Number of users who chose each option for a question (screenshot)
   - Number of users who answered a specific question (screenshot)
   - Get answers from a specific user for all questions (screenshot)
   - Number of questions a user answered (screenshot)
   - Get all questions and the number of users who chose each option (screenshot)

**Good Luck!**
