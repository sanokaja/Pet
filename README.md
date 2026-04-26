# 🐾 Pet Haven – Dog Adoption & Sales Platform

A full-stack web application built during my Infosys Springboard internship (Nov 2024 – Jan 2025) for browsing and purchasing dogs, with a separate admin panel for managing listings and sales records.

---

## Features

**User side**
- Browse 10 dog listings across 5 breeds (Labrador, Poodle, Bulldog, Beagle, German Shepherd)
- View dog details with images
- Add dogs to cart and complete purchase
- User registration and login

**Admin side**
- Role-based access — admin and regular user are separated
- Add, edit, and remove dog listings
- Upload dog images
- View sales records and sale details

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python, Flask |
| ORM | SQLAlchemy |
| Database | SQLite |
| Frontend | HTML5, CSS3, JavaScript, Bootstrap |
| Templating | Jinja2 |
| Testing | pytest (`test_app.py`) |
| Version Control | Git, GitHub |

---

## Project Structure

```
Pet/
├── app.py              # Main Flask app — routes, models, auth logic
├── data.py             # Seed script using Faker to generate fake sales data
├── temp.py             # Utility/scratch file
├── test_app.py         # Unit tests
├── requirements.txt    # Python dependencies
├── static/             # CSS, images
├── templates/          # Jinja2 HTML templates
├── uploads/            # User-uploaded dog images
└── migrations/         # Flask-Migrate database migrations
```

---

## Database Models

- **User** — stores registered users with role field (admin / user)
- **Dog** — stores listing details: breed, price, image, availability
- **Sale** — records a completed purchase transaction
- **Sale_detail** — line-item details per sale (breed, dog_id, price)
- **Booking** — stores booking entries linked to sales

---

## How to Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/sanokaja/Pet
cd Pet
```

**2. Create and activate a virtual environment**
```bash
python -m venv venv
source venv/bin/activate        # Mac/Linux
venv\Scripts\activate           # Windows
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Run the app**
```bash
python app.py
```

Open your browser at `http://127.0.0.1:5000`

**5. (Optional) Seed fake sales data**
```bash
python data.py
```

---

## Default Admin Access

> Update these credentials in `app.py` before deploying.

| Field | Value |
|---|---|
| Username | admin |
| Password | admin123 |

---

## Running Tests

```bash
pytest test_app.py
```

---

## What I Learned

- Building role-based authentication (admin vs user) from scratch using Flask sessions
- Designing relational database schemas with SQLAlchemy ORM
- Handling file uploads (dog images) in Flask
- Writing a data seeder with the Faker library
- Structuring a Flask project with templates, static files, and migrations

---

## Author

**Sanofar Nasreen**  
MCA Student · Python Full-Stack Developer  
[github.com/sanokaja](https://github.com/sanokaja) · [linkedin.com/in/sanofar-nasreen](https://linkedin.com/in/sanofar-nasreen)

---

## Note

This project was built as part of the Infosys Springboard internship program. It is a learning project and not intended for production use.
