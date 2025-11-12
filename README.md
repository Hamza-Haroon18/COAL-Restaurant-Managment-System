
# 🍔 SF CAFE – Assembly Language Restaurant Billing System

### 📘 Description

**SF Café** is a menu-driven restaurant billing managment system written in **x86 Assembly Language** using the **Irvine32 library** (MASM32 environment).
It allows the user to:

* Browse through multiple food categories (Fast Food, BBQ, Drinks, and Side Orders)
* Select items with quantity
* Automatically calculate the total bill
* Display a final receipt showing ordered items and total price

---

## ⚙️ Requirements

Before running this project, make sure you have the following setup:

* **MASM32 Assembler** (Microsoft Macro Assembler)
* **Irvine32 Library** installed and properly linked
  (Available with Kip Irvine’s *Assembly Language for x86 Processors* package)
* **Windows OS (32-bit or 64-bit)**
* **Visual Studio** or **EMU8086** with MASM support

---

## 📁 File Structure

```
SF_CAFE/
│
├── SF_CAFE.asm           # Main Assembly source code
├── Irvine32.inc          # Library include file
├── Irvine32.lib          # Irvine library (required for linking)
└── README.txt            # This file
```

---

## 🧩 Features

### 🏠 Main Menu

Displays the following options:

1. Fast Food
2. BBQ
3. Cold Drinks and Juices
4. Side Orders
5. Make the Bill

---

### 🍟 Fast Food Menu

| Option | Item                     | Price |
| ------ | ------------------------ | ----- |
| 1      | Nuggets (6 pieces)       | 150   |
| 2      | Fries (Medium)           | 100   |
| 3      | Fried Chicken (2 pieces) | 350   |

---

### 🍢 BBQ Menu

| Option | Item                | Price |
| ------ | ------------------- | ----- |
| 1      | Tikka (1 piece)     | 250   |
| 2      | Beef Boti (1 plate) | 300   |
| 3      | Kabab (1 plate)     | 200   |

---

### 🥤 Drinks Menu

| Option | Item  | Price |
| ------ | ----- | ----- |
| 1      | Pepsi | 50    |
| 2      | 7UP   | 50    |

---

### 🍚 Side Orders

| Option | Item            | Price |
| ------ | --------------- | ----- |
| 1      | Rice (1 plate)  | 100   |
| 2      | Salad (1 plate) | 70    |
| 3      | Raita           | 50    |

---

## 💵 Billing System

When the user chooses **“Make the Bill”**, the program:

* Displays each ordered item with quantity and subtotal
* Calculates and displays the **total bill**
* Prints a **thank-you message**

---

## 🧠 Program Flow

1. **Start Screen:**
   Displays a welcome message — “WELCOME TO SF CAFE”

2. **Menu Display:**
   Shows main menu options using labeled procedures (`fastfoodMenu`, `bbqMenu`, `drinkMenu`, `sideMenu`).

3. **Item Selection:**
   User enters item number → program asks for quantity → subtotal is calculated and stored.

4. **Billing:**
   When the user selects *Make the Bill*, all purchased items are displayed with total cost.

5. **Exit:**
   Displays a thank-you note and ends the program.

---

## 🧾 Example Output

```
**********WELCOME TO SF CAFE**********

MENU OPTION
(1)FAST FOOD
(2)BBQ
(3)COLD DRINKS AND JUICES
(4)SIDE ORDER
(5)MAKE THE BILL

ENTER THE OPTION WANT TO SELECT : 1

(1)NUGGETS         Price:150(6 pieces)
(2)FRIES           Price:100(medium)
(3)FREID CHICKEN   Price:350(2 pieces)
(4)BACK

ENTER THE OPTION WANT TO SELECT : 1
ENTER THE QUANTITY : 2

...

TOTAL BILL-------------------------------------------
700

*******************THANK YOU FOR ORDERING. YOUR ORDER WILL BE READY SOON*******************
```

---

## 🔧 Key Procedures

| Procedure                                          | Description                                     |
| -------------------------------------------------- | ----------------------------------------------- |
| `start`                                            | Displays welcome message                        |
| `menu`                                             | Main menu navigation                            |
| `fastfoodMenu`, `bbqMenu`, `drinkMenu`, `sideMenu` | Display respective category menus               |
| `bill`                                             | Calculates and displays the final bill          |
| `cursor1`, `cursor2`                               | Handle text positioning on console              |
| `delayfunc`                                        | Adds delay between screens for user readability |

---

## 🧮 Data Structures

* `arrff`, `arrbbq`, `arrcd`, `arrside` – arrays to store total cost for each item type
* `quan` – stores quantity of each ordered item
* `total` – stores overall total bill

---

## 👨‍💻 Author

**Muhammad Hamza Haroon**
Bachelors in Computer Science, FAST NUCES Karachi

---

DME.txt** file for you?
