# Use Cases Document - Nalu School BETA Version

## 1. Project Overview

This functional requirements document describes the business needs and system behavior for the development of the Nalu School digital platform.

Nalu School operates in the aquatic sports industry, offering activities such as:

- Surfing
- Kiteboarding
- Stand-Up Paddleboarding (SUP)
- Skateboarding

The business also provides:
- Personalized lessons
- Equipment rentals
- Product sales related to water sports

The platform must support web access across desktop and mobile devices (iOS and Android compatible browsers).

## 2. Business Problem

The client requires a responsive website aligned with its Kitesurf identity, including:

- Structured Header, Body, and Footer
- Product catalog
- Offers and promotions
- Booking system for lessons
- Equipment rental functionality
- User registration and authentication
- Shopping cart & checkout
- Social media integration
- Search functionality
- Responsive design

Orders should be processed within 24-48 hours. If delayed, the user must be notified via email.

# 3. General Site Rules & Business Constraints

## Functional Requirements

- The website must be fully responsive.
- The platform must follow accessibility standards.
- The system must be accessible from desktop, laptop, and mobile devices.
- If a page is unavailable, the system displays:
  “Working for you, see you in the water.”

## Business Rules

- Public users can browse without authentication.
- Only registered and logged-in users can complete purchases.
- Users must be redirected to login before checkout if not authenticated.
- Email confirmation is required after registration.
- Only users over 18 years old can complete purchases.
- Lesson reservations must be made at least 24 hours in advance.

# 4. Use Case - Homepage (Header)

## Preconditions
- Header must load correctly.
- All navigation links must be active.
- Must be accessible from supported browsers/devices.

## Main Flow

1. User views header.
2. Header displays:
   - Logo
   - Cart icon
   - Profile icon
   - Search icon
   - Social media icons
   - Navigation menu (School, News, Brands, Surf, Kitesurf, Skate, Classes)
3. User clicks a menu item.
4. System redirects to corresponding section.

## Alternative Flows

- If user clicks Profile:
  - If logged in → Redirect to profile.
  - If not logged in → Redirect to login page.
- If search returns no results:
  “No results found.”
- If cart is empty:
  “Cart is empty.”

# 5. Use Case – User Registration

## Preconditions
- User is not already registered.

## Business Rules
- Email must be unique.
- User must accept Terms & Conditions.
- Activation link expires in 48 hours.
- Password must contain:
  - 1 letter
  - 1 number
  - 1 special character

## Main Flow

1. User selects Register.
2. System displays registration form.
3. User fills required fields:
   - First Name
   - Last Name
   - Email
   - Password
4. System validates format.
5. System creates user in “Pending” status.
6. Activation email is sent.
7. User confirms email.
8. Account becomes Active.

# 6. Use Case - Login

## Preconditions
- User must be registered.
- Email must be confirmed.

## Business Rules
- Only confirmed users can log in.
- After 3 failed attempts - CAPTCHA enabled.
- Only users over 18 can purchase.

## Main Flow

1. User clicks Profile icon.
2. Login form is displayed.
3. User enters credentials.
4. System validates.
5. If valid - Redirect to profile.

## Alternative Flows

- Incorrect credentials - Error message displayed.
- Email not confirmed: 
  “You must confirm your email before logging in.”
- Forgot password:
  - User enters email.
  - System sends reset link.

# 7. Use Case – Shopping Cart & Checkout

## Preconditions
- User must be logged in.
- Product must be in stock.

## Business Rules
- Quantity cannot exceed stock.
- Cart persists after page exit.
- Purchase requires full personal information.

## Main Flow

1. User adds product to cart.
2. User opens cart.
3. System displays:
   - Product image
   - Name
   - Unit price
   - Quantity
   - Subtotal
4. User proceeds to checkout.
5. User confirms address & payment method.
6. User clicks “Complete Purchase”.
7. System generates order.
8. Confirmation message displayed:
  “Purchase completed successfully.”
9. Confirmation email sent.

# 8. Use Case - Classes Reservation

## Business Rules
- Must reserve at least 24 hours in advance.
- Reservation requires login.
- Slots deducted only after payment confirmation.

## Main Flow

1. User navigates to Classes.
2. System displays available classes by category.
3. User selects a class.
4. Class details displayed:
   - Description
   - Instructor
   - Schedule
   - Price
5. User clicks “Book Now”.
6. If logged in - Redirect to payment.
7. If not logged in - Redirect to login/registration.

# 9. Additional Modules

## School
Public information about instructors and disciplines.

## News
- Public access
- Sorted by most recent
- Shareable via social media

## Brands
- Alphabetical order
- Only active brands displayed

## Surf / Kitesurf / Skate
- Filter by category, brand, price
- Sorting options:
  - Price
  - Relevance
  - Newest
- Only active products with stock

# 10. Footer

## Functional Requirements
Footer must display:
- School name
- Address
- Contact phone
- Email
- Business hours
- Navigation links
- Social media icons

System year updates automatically.
Only valid social links are displayed.
