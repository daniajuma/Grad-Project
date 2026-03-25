# Karam — A Food-Rescue App

> Connecting budget-conscious consumers with local restaurants to rescue surplus food, reduce waste, and fight food insecurity in Jordan.

---

## Overview

**Karam** is a mobile application that links consumers with local restaurants, bakeries, and eateries that have surplus pre-packaged or ready-to-eat food by end of day. Businesses list their leftover items at a discounted price; users browse, order, and either pick up or receive delivery — reducing food waste while saving money.

Built as a graduation project at **Princess Sumaya University for Technology**, King Talal School of Business Technology, 2024.

---

##  Problem Statement

- Jordan wastes an estimated **93 kg of food per person annually**
- Over **50% of Jordanian households** face some form of food insecurity
- The food industry accounts for **34% of its own supply** going to waste
- Food prices in Jordan have risen faster than household income growth

Karam directly addresses both sides of this equation: helping businesses recoup losses from unsold inventory while giving consumers access to affordable, quality meals.

---

## Features

### For Consumers
- GPS-enabled browsing of nearby restaurants and eateries
- "Surprise bundles" — mystery items at further discounted prices
-  Push notifications for new listings nearby
-  Favorites tab and personalized recommendations
-  Order history and user profiles
- Secure in-app payment (card & cash on delivery)
- Dietary preference filters and food category browsing
-  Review and rating system

### For Businesses
- Business dashboard to track sales and manage listings
- Menu management system for uploading surplus items
- Analytics and inventory insights
- Access to a new, cost-conscious customer segment

### For Admins
- Backend panel for platform management
- Management reports and oversight tools
- User and business account administration

---

## System Design

### Tech Stack
- Frontend / Mobile: Flutter (cross-platform iOS & Android)
- Maps: Google Maps API (GPS and location services)
- Methodology: SDLC — Waterfall framework
- Design Tools: FlutterFlow, Wireframes

### Architecture
The app follows a standard food-ordering data flow:

```
Customer → Karam App → Restaurant → Delivery Service → Customer
                  ↕
           App Admin Panel
```

Key data flow phases:
1. User validation — login & session management
2. Item browsing — GPS-filtered restaurant listings
3. Order & payment — secure transaction processing
4. Order confirmation — receipt sent to customer
5. Delivery / pickup — real-time status updates

### Database Design (ERD Entities)

| Entity | Key Fields |
|---|---|
| `User` | user_id, name, email, password, address |
| `Products` | product_id, name, description, price, quantity, expiry_date, restaurant_id |
| `Restaurant` | restaurant_id, name, address, order_id |
| `Order` | order_id, order_date, user_id, delivery_service_id, status |
| `Delivery Service` | delivery_service_id, order_id, status, contact_info |
| `Category` | category_id, category_name, category_type |
| `Feedback` | feedback_id, user_id, restaurant_id, rating, comment |
| `Location` | location_id, order_id, city, district, street, postal_code |

---

##  Market Research

Survey conducted with 78 respondents in Jordan.


Top features users want:
1. Discounted food from nearby restaurants
2. Clear expiry dates and food descriptions
3. User reviews and ratings
4. Variety of food options
5. Upfront pricing with no hidden fees


---

##  Limitations

- Cultural barrier — social stigma around near-expiry food may deter some users
- Technology gap — limited smartphone access or digital literacy in some demographics
- Supply dependency — relies on consistent participation from local businesses
- Logistics — requires partnerships with local delivery services for physical fulfillment
- Infrastructure — GPS accuracy issues in some areas of Jordan

---

##  Future Work

- [ ] AI/ML integration for predicting unsold inventory and personalizing offers
- [ ] Loyalty and referral points system
- [ ] Expansion to other Jordanian cities beyond Amman
- [ ] Potential integration with Careem / Talabat
- [ ] Addition of supermarket pre-packaged goods (sandwiches, sushi, salads)
- [ ] Collaboration with environmental agencies to measure waste reduction impact
- [ ] Economic impact analysis for low-income communities

---

## Team

| Name | Role | Email |
|---|---|---|
| Dania Juma | Project Manager | dan20201001@std.psut.edu.jo |
| Anmar Rawashdeh | Data Analyst | anm20200074@std.psut.edu.jo |
| Siraj Sawaf | IT Manager | sir20200780@std.psut.edu.jo |

Supervised by: Dr. Ahmad Abushakra
Institution: Princess Sumaya University for Technology — King Talal School of Business Technology
Year: 2024

---

## License

This project was developed as an academic graduation project at Princess Sumaya University for Technology. All rights reserved by the team members.
