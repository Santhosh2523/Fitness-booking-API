# 🧘‍♀️ Fitness Booking API

A Django for booking fitness classes (Yoga, Zumba, HIIT) at a fictional studio.

---

## 📦 Features

- View available fitness classes
- Book a class with available slots
- View your bookings by email
- Handles overbooking errors
- Timezone-aware slots (IST)

---

## 🛠 Tech Stack

- Python 3.12.8
- Django
- SQLite
- Postman or cURL for testing

---

## 🚀 Setup Instructions

1. **Clone the repository**
bash
git clone https://github.com/Santhosh2523/Fitness-booking-API.git

cd Fitness-booking-API

2.Create a virtual environment

python -m venv booking

source venv/bin/activate  # On Windows: venv\Scripts\activate

3.Install dependencies

pip install -r requirements.txt

4.Apply migrations

python manage.py migrate

5.Seed sample data

python insert_db.py

6.Run the development server

python manage.py runserver

API Endpoints

1.GET /classes - (Returns a list of all upcoming fitness classes)

curl http://127.0.0.1:8000/classes/

2.POST /book - (Accepts a booking request)

curl -X POST http://127.0.0.1:8000/book/ \

  -H "Content-Type: application/json" \
  
  -d '{"class_id": 1, "client_name": "Alice", "client_email": "alice@example.com"}'

3.GET /bookings?email=alice@example.com - (Returns all bookings for a specific client.)

curl http://127.0.0.1:8000/bookings/?email=alice@example.com

⚠️ Error Handling

  Handles overbooking
  
  Validates missing fields
  
  Timezone management from IST

📥 Postman Collection

1. Download the file

➡️ Click to download FitnessBookingAPI.postman_collection.json

2. Import into Postman
   
Open Postman

Click Import (top left)

Choose File

Select the downloaded file

Click Import

3. Test Your API
   
You will see a collection with 3 pre-made requests:

✅ GET /classes

✅ POST /book

✅ GET /bookings?email=...

Just click Send to test your API running on http://127.0.0.1:8000.

✅ Author
Created by Santhosh Suresh.





