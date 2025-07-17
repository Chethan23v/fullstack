Exercise 1 – Expressjs
(http Methods)

1.	Develop a basic Express.js application that simulates a simple user management system. The application should define a /users route that allows interaction through different HTTP methods. Begin by initializing an in-memory array to hold user objects, where each object includes three properties: id, name, and email. Implement functionality to return all users using the GET method on /users. Allow new users to be added via the POST method to the same route. Each new user should receive a unique ID that increments sequentially. Additionally, implement the DELETE method on /users/:id to remove a specific user by ID. Ensure that the application uses express.json() middleware to parse incoming JSON request bodies, and return appropriate JSON responses for each action. Include basic error handling to display a clear message when attempting to delete a user that does not exist.

2.	Create an Express.js application that manages a catalog of products. Start with a predefined array of products, each having the properties id, name, price, and stock. Implement a PUT route at /products/:id that updates an existing product’s details. The request body may contain any combination of the three updatable fields: name, price, and stock. Your application should update only the fields provided in the request and leave the rest unchanged. If a product with the given ID is not found, return a 404 status with a message indicating that the product does not exist. Ensure the use of express.json() middleware to process JSON bodies and return structured JSON responses that confirm the update and show the latest state of the product. Keep the application implementation in a single JavaScript file, without using a database or external files.






3.	Design and implement an Express.js application to manage a list of books. Each book must have an id, title, and author. Initialize the application with at least two predefined books stored in an in-memory array. The application must support the following functionalities:

a.	The GET /books route should return the list of all books.
b.	The POST /books route should accept a new book's title and author in the request body, assign it a unique id, add it to the array, and return a confirmation message.
c.	The PUT /books/:id route should update an existing book’s title and/or author based on the id provided in the URL. Only the fields present in the request body should be updated. If the book is not found, return a 404 status with an appropriate message.
d.	The DELETE /books/:id route should remove a book by its id. If the book does not exist, return a 404 error. Otherwise, return a success message indicating which book was deleted.
e.	Ensure proper use of express.json() middleware and return all responses in plain text format using res.send().
4.	Develop an Express.js application that provides basic functionality for managing student records. Each student should have an id, name, and course. Initialize the application with at least three student records in an in-memory array. The application must implement the following:
a.	The route GET /students should return a list of all students.
b.	The route GET /students/:id should return details of a single student based on the ID provided in the URL.
c.	The route POST /students should accept a new student's name and course via the request body, assign a unique ID, add the student to the array, and return a message confirming the addition.
d.	The route PUT /students/:id should update the student’s name and/or course for the given ID. If the student does not exist, the server should return a 404 error.
e.	The route DELETE /students/:id should remove a student from the list and return the details of the deleted student.
f.	Use express.json() middleware to parse JSON input, and use res.send() for all output. Ensure appropriate status codes and messages are used for both success and error responses.
5.	Create an Express.js application to simulate a simple task management system. Each task should have an id, title, description, and a status field (e.g., “pending”, “in-progress”, “completed”). Initialize the application with at least two tasks in an in-memory array.

a.	The application must implement the following functionality using appropriate HTTP methods:
b.	GET /tasks: Return the list of all tasks.
c.	GET /tasks/:id: Return details of a task by its ID.
d.	POST /tasks: Accept a new task's title and description from the request body, assign a unique ID, default the status to “pending”, and add it to the array.
e.	PUT /tasks/:id: Allow the user to update any of the task fields (title, description, or status). Only the provided fields should be updated.
f.	DELETE /tasks/:id: Remove a task by its ID. If the task doesn't exist, return a 404 error.
g.	Ensure use of express.json() middleware for parsing input, and use res.send() for all output messages.
6.	Develop an Express.js application that manages a library of movies. Each movie should include an id, title, genre, and rating (1–10). Use an in-memory array initialized with at least three sample movies.

a.	Implement the following routes using the appropriate HTTP methods:
b.	GET /movies: Retrieve all movie records.
c.	GET /movies/:id: Retrieve details of a specific movie.
d.	POST /movies: Add a new movie to the array with data from the request body.
e.	PUT /movies/:id: Update one or more fields (title, genre, rating) of a specific movie.
f.	DELETE /movies/:id: Remove the movie from the array by its ID. Return a clear message even if the movie doesn’t exist.
g.	Ensure all inputs are JSON and responses are returned in text using res.send(). Include error handling for invalid movie IDs.














Exercise 2 – Express JS
(Templating with EJS & Pug, Static Files, Form Handling, Multer)
1.	Create an Express.js app using EJS that renders a movie gallery:
o	Render a list of movies with titles and ratings.
o	Use a layout file with a header/footer and external CSS to style the cards.
o	Highlight movies with a rating above 8 in a different color using conditional rendering.
 
2.	Build a recipe page using Pug templating:
o	Pass dynamic recipe data (name, ingredients, steps) to the Pug view.
o	Apply external CSS for layout and inline CSS for highlighting ingredients.
o	Include a virtual path for serving images used in the recipe view (/assets).
3.	Design a feedback form for a travel website using Express and multer:
o	The form should collect name, email, and a screenshot of an issue.
o	Use multer.diskStorage() to save the image to an uploads/ folder.
o	On submission, display the input and image preview using EJS.





Exercise 3 – Express JS
(Covers Cookies, Sessions, Authentication)
1.	Create a student portal login system using Express.js
o	Create a /register route to add a student with a rollNo, name, and password.
o	Use express-session to store the session after successful login from /login.
o	On login, also set a cookie studentPortalAccess with the student's roll number and an expiry of 3 minutes.
o	Use middleware (cookie-parser and express-session) to manage cookies and sessions.
2.	Design a protected route /result that only logged-in students can access
o	Use session middleware to verify if the student is logged in.
o	If valid, show: "Hi [name], your results are available!".
o	If not, return: "Access denied: Please login to view results."
o	Add a /logout route to destroy the session and clear the cookie.
3.	Build a course enrollment route /courses with GET and POST
o	Use GET /courses to return a list of available courses (only if logged in).
o	Use POST /courses to enroll the logged-in student into a course.
o	On successful enrollment, create a cookie named lastEnrolledCourse (valid for 2 mins).
o	Add error handling for:
	Trying to enroll without being logged in
	Enrolling in a course already taken











Exercise 1 – Node JS
(Callbacks, Event Loop and Event Emmiter)
1.	Write a Node.js program that defines a function add(a, b, callback) which adds two numbers and returns the result via a callback. Chain this with another callback to multiply the result by 10 and log it. Finally, use fs.readFile() to read and display the contents of a file named info.txt.
2.	Create a countdown timer using setTimeout(), use setTimeout() and console.log() to demonstrate asynchronous behaviour, and add another setTimeout with 1000ms execute.
3.	Create an event emitter that emits a greet event and logs a message, and emit a login event with a username and log "<username> has logged in".

Exercise 2 – Node JS
(Buffers, Streams and File System)
4.	Create a buffer from the string "Node.js" and print it in hexadecimal form, then modify the first letter of the buffer from "N" to "C" and print the result.
5.	Use a readable stream to read data.txt and log chunks to the console, and explain the benefit of using streams instead of fs.readFile().
6.	Write a program to write "Welcome to Node.js" into a file named welcome.txt, and read the content of welcome.txt and log it using a callback.

















Exercise 1 – React JS 
(Components, Lists, Keys, prop validation and CSS)

1.	Develop a React-JS application using a functional component that renders a list of countries with their capitals using .map(). Each list item must have a unique key, and the list should be styled using an external CSS file.
2.	Create a class component in React-JS that displays a list of restaurants, where each restaurant contains a nested list of menu items and apply unique keys for each item.
3.	Create a functional component in React-JS that displays a 5 Vehicle Info Card in a row with details like Model, Manufacturer, Year, and Fuel Type. Use inline CSS to style the card layout and appearance.
 




 
Exercise 2 – React JS 
(Components, Lists, Keys, prop validation and CSS)


Exercise 1 – React JS 
(Components, Lists, Keys, prop validation and CSS)

1.	Develop a React-JS application using a functional component that renders a list of countries with their capitals using .map(). Each list item must have a unique key, and the list should be styled using an external CSS file.
2.	Create a class component in React-JS that displays a list of restaurants, where each restaurant contains a nested list of menu items and apply unique keys for each item.
3.	Create a functional component in React-JS that displays a 5 Vehicle Info Card in a row with details like Model, Manufacturer, Year, and Fuel Type. Use inline CSS to style the card layout and appearance.
 




 
Exercise 2 – React JS 
(Components, Lists, Keys, prop validation and CSS)

4.	Design a class-based React-JS component called CourseCard that receives props such as course title (string), duration in weeks (number), and instructor name (string). Use prop-types to validate that all props are required and of the correct type.

5.	Build a functional component in React-JS that renders a grid of famous landmarks (name, location, country). Use external CSS to apply styles like borders, spacing, and hover effects to each item.
6.	Design a React class component with prop validation using PropTypes to ensure correct data types for props?

  
 












Exercise 3 – React JS
(Forms, Events, Conditional Rendering, CSS)
1.	Design and develop a functional component called NewsletterSignup. The form should include fields for full name and email address. Use useState to control the form inputs. On form submission, display a thank-you message using conditional rendering. Style the form using an external CSS file with padding, border, and hover effects.
 
2.	Design and develop a functional component named UserStatusSwitcher that toggles a user's status between “Online” and “Offline” using a button. Use useState to manage status and onClick to update it. Display the current status with conditional rendering. Style the status text with inline CSS (e.g., green for online, red for offline).
 
3.	Design and develop a functional component called TechBugReportForm. The form should include the following fields:
o	Bug Title (text)
o	Description (textarea)
o	Affected Module (dropdown: e.g., UI, API, Database, Network)
Validate that all fields are filled before submission. Use conditional rendering to show inline error messages if any field is empty and display a submission success message otherwise. Apply external CSS to organize the form and highlight input errors.
 
 
Exercise 4 – React JS
(Forms, Events, Conditional Rendering, CSS)
4.	Design and develop a functional component named FeedbackPoll. Display a question such as “How would you rate our tech support?” with three buttons: Good, Neutral, Poor. When a user clicks one, use conditional rendering to show a thank-you message including their selected choice. Use external CSS to style the poll area, buttons, and feedback message.
       
5.	Design and develop a functional component called ExpenseTrackerInput. Include inputs for expense name and amount. Use useState for form control. Validate that the amount is a positive number. On form submission, show a success message or an error message using conditional rendering. Use inline CSS to highlight the amount field in red if validation fails.
 
6.	Design and develop a functional component named ThemeSelector. Provide two radio buttons: Light Mode and Dark Mode. Use useState to track the selected theme. Conditionally render a preview box styled with the appropriate theme (dark or light). Use external CSS classes to apply theme-based background and text styling.
 





Exercise 5 – React JS
(Forms, Events, Conditional Rendering, CSS)
1.	Design and develop a React functional component called TextInputTracker with a controlled text input. Display the current input text below the input as the user types, along with a character count. Use useState to track the input value. Restrict input to only letters and spaces—ignore any other characters. Include a clear button that resets the input and display. Keep the styling minimal: just some spacing and basic font styles to keep it clean and readable.
  
2.	Design and develop a functional component named ColorChanger with a button that cycles through a list of colors (["red", "green", "blue"]) each time it’s clicked. Use useState to manage the current color. Display a div with a fixed height and width, and apply the current color as its background using inline CSS. Also, include a label above the div showing the current color name.
 
3.	Design and develop a functional component named Counter that displays a number starting from 0. Add three buttons labeled "Increase", "Decrease", and "Reset". Clicking "Increase" should increment the number by 1 using useState. Clicking "Decrease" should decrement the number by 1. Clicking "Reset" should set the number back to 0. Use inline CSS to center the content on the page, apply padding, margin, and background color to the buttons, and make the displayed number bold with a slightly larger font size. 

 




Exercise 3 – React JS
(Forms, Events, Conditional Rendering, CSS)
1.	Design and develop a functional component called NewsletterSignup. The form should include fields for full name and email address. Use useState to control the form inputs. On form submission, display a thank-you message using conditional rendering. Style the form using an external CSS file with padding, border, and hover effects.
 
2.	Design and develop a functional component named UserStatusSwitcher that toggles a user's status between “Online” and “Offline” using a button. Use useState to manage status and onClick to update it. Display the current status with conditional rendering. Style the status text with inline CSS (e.g., green for online, red for offline).
 
3.	Design and develop a functional component called TechBugReportForm. The form should include the following fields:
o	Bug Title (text)
o	Description (textarea)
o	Affected Module (dropdown: e.g., UI, API, Database, Network)
Validate that all fields are filled before submission. Use conditional rendering to show inline error messages if any field is empty and display a submission success message otherwise. Apply external CSS to organize the form and highlight input errors.
 
 
Exercise 4 – React JS
(Forms, Events, Conditional Rendering, CSS)
4.	Design and develop a functional component named FeedbackPoll. Display a question such as “How would you rate our tech support?” with three buttons: Good, Neutral, Poor. When a user clicks one, use conditional rendering to show a thank-you message including their selected choice. Use external CSS to style the poll area, buttons, and feedback message.
       
5.	Design and develop a functional component called ExpenseTrackerInput. Include inputs for expense name and amount. Use useState for form control. Validate that the amount is a positive number. On form submission, show a success message or an error message using conditional rendering. Use inline CSS to highlight the amount field in red if validation fails.
 
6.	Design and develop a functional component named ThemeSelector. Provide two radio buttons: Light Mode and Dark Mode. Use useState to track the selected theme. Conditionally render a preview box styled with the appropriate theme (dark or light). Use external CSS classes to apply theme-based background and text styling.
 




  
 



