# Polls System - Backend Implementation

*פרויקט זה מהווה 15% מהציון הכללי. ציון עובר הינו 70 ומעלה.*

## תנאי הגשה:
1. יש לעקוב אחר כל ההנחיות, ולבנות את הפרויקט לפיהן.
2. יש להכין קובץ בדיקות שיכיל בתוכו צילומי מסך עפ הדרישות שיפורטו למטה.

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


polls-system-backend/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── firstProject/
│   │   │           ├── controller/
│   │   │           │   └── UserController.java
│   │   │           ├── service/
│   │   │           │   ├── UserService.java
│   │   │           │   └── UserServiceImpl.java
│   │   │           ├── repository/
│   │   │           │   ├── UserRepository.java
│   │   │           │   └── UserRepositoryImpl.java
│   │   │           ├── model/
│   │   │           │   ├── User.java
│   │   │           │   └── Status.java
│   │   │           └── PollsSystemApplication.jav



## קובץ בדיקות: (צילומי מסך/וידיאו)

בסוף הפרויקט לפני שאתם מגישים תעברו על כל ההנחיות פה למטה ותצרפו לפרויקט תיקייה בשם "בדיקות" והיא תכיל את כל התמונות ומה שצריך.

* אין צורך בצילומי קוד אלא רק בבקשות שעבדו (כולל בקשות שמטפלות בשגיאות בלי להקריס את השרת)

1. **תמיכה ב-קרוד מלא למשתמשים:**
   - יצירת משתמש (צילום מסך)
   - עדכון משתמש (צילום מסך)
   - מחיקת משתמש (צילום מסך)
   - קבלת מידע על המשתמש (צילום מסך)

2. **תמיכה בקרוד מלא לשאלות:**
   - יצירת שאלה (צילום מסך)
   - עדכון שאלה (צילום מסך)
   - מחיקת שאלה (צילום מסך)
   - קבלת מידע על שאלה (צילום מסך)

3. **שמירת תשובות משתמשים לשאלות סקר (להראות שנשמרים תוצאות)**

4. **טיפול בשגיאות כמו חוסר תשובות לכל השאלות (צילומי מסך)**

5. **מידע סטטיסטי על תשובות המשתמשים: (צילום מסך של הבקשה שעבדה, לא של הקוד)**
   - מספר המשתמשים שבחרו כל אפשרות בשאלה (צילום מסך)
   - מספר המשתמשים שענו על שאלה ספציפית (צילום מסך)
   - קבלת תשובות ממשתמש מסוים לכל השאלות (צילום מסך)
   - מספר השאלות שהמשתמש ענה עליהן (צילום מסך)
   - קבלת כל השאלות ומספר הבחירות בכל אפשרות (צילום מסך)

**Good Luck!**
