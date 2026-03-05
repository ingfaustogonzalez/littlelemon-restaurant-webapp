# 🍋 Little Lemon Restaurant Web App

## 📌 Repository Name
**littlelemon-restaurant-webapp**

## 📖 Description
Full-stack Django web application for a fictional restaurant. Includes dynamic menu pages, detailed menu item views using URL parameters, booking functionality, admin panel integration, and template inheritance.

---

# 🚀 Project Overview

This project is a restaurant website built using the Django framework. It demonstrates full-stack development concepts including:

- Django Models & Migrations  
- Dynamic Views  
- URL Routing with Parameters  
- Template Inheritance  
- Django Admin Panel  
- Database Integration (SQLite)  
- Static Files Management  
- Form Handling  

The application simulates a real-world restaurant website called **Little Lemon**, a Mediterranean restaurant owned by Mario and Adrian.

---

# 🏗️ Website Layout Structure

## 🔝 Header
- Displays the **Little Lemon logo with name**, centered at the top.
- Below the logo is a horizontal navigation bar with links:
  - Home
  - About
  - Menu
  - Book  

All navigation links appear side-by-side in a clean horizontal layout.

---

## 🔻 Footer
- Left side: Little Lemon logo (without the name).
- Right side:  
  `Copyright Little Lemon`

---

# 🌐 Web Pages

---

## 🏠 1. Home Page

The Home page uses a **2-row by 3-column layout**.

### 🔹 First Row (Spans all 3 columns)
Displays:
- **SPECIAL OFFER**
- *30% Off This Weekend*
- Functional **“Book Now”** button

### 🔹 Second Row

#### Column 1 – Our New Menu
- Representative image  
- Description of seasonal Mediterranean items  
- Link: **See our new menu**

#### Column 2 – Book a Table
- Representative image  
- Description encouraging reservations  
- Link: **Book your table now**

#### Column 3 – Opening Hours
- Representative image  
- Weekly schedule:
  - Mon–Fri: 2pm – 10pm  
  - Sat: 2pm – 11pm  
  - Sun: 2pm – 9pm  

### 📸 Home Page Screenshot
![Home Page](assets/Screenshot_1_home.png)

---

## 👨‍🍳 2. About Page

Displays restaurant background and story:

- Family-owned Mediterranean restaurant  
- Based in Chicago, Illinois  
- Inspired by Italian, Greek, and Turkish cuisine  
- Seasonal rotating menu (12–15 items)  
- Rustic, relaxed atmosphere  
- Owned by Mario and Adrian  

Right side:
- Image of the two owners  
- Caption: *Little Lemon owners Mario and Adrian*

### 📸 About Page Screenshot
![About Page](assets/Screenshot_2_about.png)

---

## 🍽️ 3. Menu Page

Displays all menu items dynamically from the database.

Each item shows:
- Item name (clickable link)  
- Price formatted as: `$XX.00`

Example:
Bruschetta
$11.00


### 📸 Menu Page Screenshot
![Menu Page](assets/Screenshot_3_menu.png)

---

## 🍲 Menu Item Detail Page

When clicking a menu item (e.g., Bruschetta), the page displays:

- Breadcrumb navigation:  
  `Home / Menu / Item Name`
- Item Name  
- Full description  
- Formatted price: `Price: $11.00`  
- Image of the dish (loaded dynamically from static folder)

This page uses:
- URL parameter (`pk`)
- `objects.get(pk=pk)` query
- Dynamic template rendering

### 📸 Menu Item Screenshot
![Menu Item](assets/Screenshot_4_menu_item_1.png)

---

## 📅 4. Book (Reservation) Page

Displays a reservation form:

- First Name  
- Last Name  
- Guest Number  
- Comment  
- Submit Button  

Right side:
- Interactive Google Map (zoomable & movable)

### 📸 Booking Page Screenshot
![Booking Page](assets/Screenshot_5_book.png)

---

# 🗄️ Database Integration

The application uses **SQLite** as the database.

---

## 📌 Booking Table

After submitting the reservation form, data is stored in the `restaurant_booking` table.

Fields:
- `id`
- `first_name`
- `last_name`
- `guest_number`
- `comment`

### 📸 Booking Table Screenshot
![Booking Table](assets/Screenshot_6_booking_table.png)

---

## 📌 Menu Table

The `Menu` model stores:

- `id`
- `name`
- `price`
- `menu_item_description`

### 📸 Menu Table Screenshot
![Menu Table](assets/Screenshot_7_menu_table.png)

---

# 🛠️ Technologies Used

- Python  
- Django  
- SQLite  
- HTML5  
- CSS3  
- Django Template Language (DTL)  
- Django Admin Panel  

---

# ▶️ How to Run the Project

```bash
# Clone the repository
git clone https://github.com/yourusername/littlelemon-restaurant-webapp.git

# Navigate into project directory
cd littlelemon-restaurant-webapp

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py migrate

# Create superuser (optional)
python manage.py createsuperuser

# Run server
python manage.py runserver
```

# Open in browser:
http://127.0.0.1:8000/
