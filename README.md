# Leasing Application Backend Test

**Duration:** ~4-8 hours

**Objective:** Build a backend API to support a multi-step leasing application form.

## Tech Stack
- **Python**
- **Django** (Django Rest Framework for API)
- **Celery** (for asynchronous tasks)
- **PostgreSQL** (or SQLite for simplicity)
- **Docker** for containerization (optional)

## API Endpoints

### User Management
- **`/api/users/register/` (POST):** Register a new user.  
  Fields: username, email, password.

- **`/api/users/login/` (POST):** User login.  
  Fields: email, password.

- **`/api/users/profile/` (GET):** Retrieve user's profile details.

### Leasing Application
- **`/api/leasing/countries/` (GET):** Fetch list of countries.

- **`/api/leasing/models/` (GET):** Fetch product models based on the product type.

- **`/api/leasing/applications/` (POST):** Submit a new leasing application.

- **`/api/leasing/applications/{id}/` (GET, PUT, DELETE):** Manage existing application.

### File Management
- **`/api/files/upload/` (POST):** Upload documents.

- **`/api/files/{id}/` (GET, DELETE):** Manage uploaded documents.

## Celery Task

- **Send Confirmation Email:** Trigger a Celery task to send a confirmation email upon successful application submission.

## Features & Expectations

- JWT Authentication for secure endpoints.
- Use Django Rest Framework for API development.
- Perform validation on all data received from endpoints.
- Implement error handling and return appropriate HTTP status codes and messages.
- Use database transactions for application submissions to ensure data integrity.
- Asynchronous email sending with Celery.
- Dockerfile and docker-compose setup for easy deployment (optional).

## Evaluation Criteria

- Proper use of Django and Django Rest Framework features.
- Database design and query optimization.
- Celery configuration and task management.
- Code Structure and Python Best Practices.
- Security measures (e.g., authentication, input validation).
- Error handling and user-friendly messages.
- Documentation of API endpoints and how to run the project.


**React + TypeScript Test Project: Leasing Application Form**  
**Duration:** ~4-8 hours  
**Objective:** Build a multi-step leasing application form using React Hook Form. This form will be used by customers to apply for leasing products (e.g., cars, apartments, equipment).

**Tech Stack**  
- React (start with Vite or Create React App)  
- TypeScript  
- react-hook-form for form handling  
- schema validation  
- react-query or useEffect for fetching mock API data  
- Styling: Tailwind CSS / Styled Components (or plain CSS)

**Form Steps & Fields**  
**Step 1: Personal Information**  
- Full Name (required, min 3 characters)  
- Email (required, valid email format)  
- Phone (required, valid phone number)  
- Date of Birth (required, must be at least 18 years old)  
- Country (Dropdown, fetched from an API)  
**Step 2: Leasing Details**  
- Product Type (Car, Apartment, Equipment) (Dropdown)  
- Product Model (Auto-populated based on Product Type)  
- Lease Duration (1-36 months, number input, required)  
- Monthly Budget (required, min: $500)  
**Step 3: Additional Details & Submission**  
- Notes (Optional text area)  
- Upload Document (File Upload)  
- Agree to Terms & Conditions (required checkbox)  

Extra Challenge:  
- Dynamic Fields: The Product Model dropdown should be updated dynamically when Product Type changes.  
- Conditional Validation: If Lease Duration > 24 months, require Employer Name and Annual Income fields.

**Features & Expectations**  
- Multi-step Form with "Next" and "Previous" buttons  
- Validation using React Hook Form & Zod  
- Fetching Data from a Mock API  
- Save & Restore Form Data (LocalStorage or Context API)  
- Submit Data & Show Success Message  
- Clean & Reusable Component Structure  

**Evaluation Criteria**  
- React Hook Form Best Practices  
- TypeScript usage (Proper types, interfaces, etc.)  
- Performance Optimization (Avoid unnecessary re-renders)  
- Error Handling & User Experience (Form validations, error messages)  
- Code Readability & Maintainability  
- API Integration & Async Handling  

**Getting Started**  
1. Set up a React project (Vite or Create React App):  
   `npx create-react-app leasing-form --template typescript` or `npm create vite@latest leasing-form --template react-ts`  
   `cd leasing-form`  
   `npm install`  
2. Install dependencies:  
   `npm install react-hook-form zod @hookform/resolvers react-query axios`  
3. Create a multi-step form using react-hook-form.  
4. Fetch mock data (countries, product models) using an API. You can use this public API:  
   `https://restcountries.com/v3.1/all`  
5. Implement form validation with Zod schema validation.  
6. Ensure conditional fields and dynamic dropdowns work correctly.  
7. Store form progress in LocalStorage or Context API so the user doesn’t lose data when navigating between steps.  
8. Show a success message after submission.

**Submission**  
Once completed, submit the GitHub repository link with the project code and a short README explaining:  
- How to run the project  
- Any additional features implemented  
