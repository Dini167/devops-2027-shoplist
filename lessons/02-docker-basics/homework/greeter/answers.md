1. docker build -t greeter:v1 .

2. docker run -d --name greeter -p 9000:8000 greeter:v1

3. מוסיפים לפקודה: -e GREETING=Shalom

4. התשובה:
{"message": "Shalom, Rivka!"}

5.  אם משנים רק את app.py:
- שלבי התקנת Flask נשארים ב־Cached, כי requirements.txt לא השתנה.
- שלב COPY app.py מתבצע מחדש, כי הקובץ השתנה.
כך Docker חוסך זמן ולא מתקין מחדש חבילות ללא צורך.