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
