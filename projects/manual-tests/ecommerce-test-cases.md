# 🛒 E-commerce Test Cases

This document contains **manual test cases** for an e-commerce application, covering **Sign Up, Login, Cart, and Checkout flows**.  
Each test case follows a structured format: **ID, Scenario, Steps, Expected Result, Status**.  

---

## 📌 Module: Sign Up

| TC ID  | Test Scenario                   | Steps                                                                 | Expected Result                                    | Status   |
|--------|---------------------------------|----------------------------------------------------------------------|----------------------------------------------------|----------|
| TC-301 | Sign up with valid details       | 1. Go to Sign Up page <br> 2. Enter valid name, email, password <br> 3. Click Sign Up | Account created successfully, redirected to dashboard | Pass/Fail |
| TC-302 | Sign up with existing email      | 1. Enter email already registered <br> 2. Enter valid password <br> 3. Click Sign Up | Error message: *"Email already exists"*            | Pass/Fail |
| TC-303 | Sign up with invalid email format| 1. Enter `invalid@user` <br> 2. Enter valid password <br> 3. Click Sign Up | Validation error: *"Invalid email format"*         | Pass/Fail |
| TC-304 | Sign up with weak password       | 1. Enter valid email <br> 2. Enter `123` as password <br> 3. Click Sign Up | Error: *"Password must be at least 8 characters"*  | Pass/Fail |
| TC-305 | Mandatory fields validation      | 1. Leave all fields empty <br> 2. Click Sign Up                      | Validation messages shown under each field         | Pass/Fail |

---

## 📌 Module: Login

| TC ID  | Test Scenario                   | Steps                                                                 | Expected Result                                   | Status   |
|--------|---------------------------------|----------------------------------------------------------------------|---------------------------------------------------|----------|
| TC-001 | Login with valid credentials     | 1. Navigate to login page <br> 2. Enter valid username & password <br> 3. Click Login | User is redirected to dashboard/homepage          | Pass/Fail |
| TC-002 | Login with invalid password      | 1. Enter valid username <br> 2. Enter wrong password <br> 3. Click Login | Error message displayed: *"Invalid credentials"* | Pass/Fail |
| TC-003 | Login with empty fields          | 1. Leave both fields blank <br> 2. Click Login                       | Error message: *"Fields cannot be empty"*         | Pass/Fail |
| TC-004 | Login with invalid email format  | 1. Enter `user@invalid` <br> 2. Enter valid password <br> 3. Click Login | Validation error: *"Invalid email format"*       | Pass/Fail |

---

## 📌 Module: Cart

| TC ID  | Test Scenario                   | Steps                                                                 | Expected Result                               | Status   |
|--------|---------------------------------|----------------------------------------------------------------------|-----------------------------------------------|----------|
| TC-101 | Add item to cart                 | 1. Navigate to product page <br> 2. Click *Add to Cart*              | Item appears in cart with correct details      | Pass/Fail |
| TC-102 | Remove item from cart            | 1. Add product to cart <br> 2. Click *Remove*                        | Item is removed from cart                      | Pass/Fail |
| TC-103 | Update item quantity             | 1. Add product to cart <br> 2. Change quantity to 3                  | Cart updates subtotal correctly                | Pass/Fail |
| TC-104 | Cart persists after refresh      | 1. Add product to cart <br> 2. Refresh page                          | Cart still shows previously added items        | Pass/Fail |

---

## 📌 Module: Checkout

| TC ID  | Test Scenario                   | Steps                                                                 | Expected Result                                 | Status   |
|--------|---------------------------------|----------------------------------------------------------------------|-------------------------------------------------|----------|
| TC-201 | Checkout with valid payment      | 1. Add item to cart <br> 2. Proceed to checkout <br> 3. Enter valid payment details <br> 4. Confirm | Order placed successfully, confirmation page displayed | Pass/Fail |
| TC-202 | Checkout with invalid payment    | 1. Add item to cart <br> 2. Proceed to checkout <br> 3. Enter invalid payment details <br> 4. Confirm | Error message: *"Payment failed"*              | Pass/Fail |
| TC-203 | Checkout with empty cart         | 1. Navigate to checkout without adding products                      | System prevents checkout and displays message: *"Your cart is empty"* | Pass/Fail |
| TC-204 | Verify order confirmation email  | 1. Place valid order <br> 2. Check registered email                  | Order confirmation email is received            | Pass/Fail |

---

## 🔍 Exploratory Test Checklist 

- Verify responsiveness on mobile and tablet devices  
- Verify session timeout after inactivity  
- Verify cart is preserved after logout/login  
- Verify discounts/coupons are applied correctly  
- Verify accessibility (keyboard navigation, screen readers)  

---
