# CS465-fullstack Journal
## Architecture

Compare and contrast the types of frontend development you used in your full stack project, including Express HTML, JavaScript, and the single-page application (SPA).
- During the front-end development of our MEAN full-stack project, we used Express HTML, JavaScript, and a single-page application (SPA). Express HTML was used at the beginning of the project as a framework for setting up the client-facing side of the web application to create a framework to serve static HTML for us to use Javascript to code the web application's logic and behaviors. We then moved the static HTML site to dynamic JSON with Handlebars to implement the model-view-controller architecture pattern. Javascript was then used to create a module for our web application to access our NoSQL database with Mongoose to dynamically update the web application as the user interacts with the website. We then finally implemented a single-page application (SPA) for the admin-only side of the web application. The admin-only side only needed to update with new data when the trips were added, edited, or deleted, so the whole page did not need to reload, an advantage of SPAs since the whole HTML packet gets sent with the initial page load.
		
Why did the backend use a NoSQL MongoDB database?
- We used a NoSQL MongoDB database on the backend due to its efficient querying features. The NoSQL database is unstructured and scales horizontally. MongoDB also uses a JSON protocol, which works well with our front-end Javascript.
		
## Functionality

How is JSON different from Javascript and how does JSON tie together the frontend and backend development pieces?
- JSON was used to store and then display the data for my project. JSON is often utilized when transferring data to or from a server, and it formats the data into objects. JavaScript is used on the front end to control how websites operate. MongoDB stores data in a binary JSON format - BSON. The data may then be extracted using the MongoDB driver and formatted as JSON. Then, using Handlebars and TypeScript, we can utilize that data. JSON serves as a link between the front end and back end in this way.
		
Provide instances in the full stack process when you refactored code to improve functionality and efficiencies, and name the benefits that come from reusable user interface (UI) components.
- We had built the admin-only side to show trips in a card format. If the client wanted to have the option of the trips shown in another way, like a list, especially if there were a lot of trips being offered, we could add code to the trip listing component. This would make the component larger and less manageable. Using programming best practices, we refactored the logic to build a trip card component with Angular to provide the web application with the foundation for adding more features to the trip's UI in the future. The result did not look different to the user, but the code was much more comprehensible and manageable after the change.
		
## Testing

Methods for request and retrieval necessitate various types of API testing of endpoints, in addition to the difficulties of testing with added layers of security. Explain your understanding of methods, endpoints, and security in a full stack application.
- API endpoints are the points where the web application and the API communicate. Our security best practices started with user authentication and authorization on the admin side of the web application. Due to the importance of security, developers should use hashes over transferring raw passwords to and from the database on the admin side of the web application. Additionally, it's crucial to keep these hashes off of websites like GitHub when developing your code, so we created a .env file with our key and value pair. This file is used by JSON web token (JWT) to transfer JSON objects securely. Before permitting a user or admin to carry out methods like GET, POST, PUT, and DELETE using the API, we must additionally confirm their permissions by authorization. These two security aspects help us secure the API endpoints from nefarious users. 
		
## Reflection

How has this course helped you in reaching your professional goals? What skills have you learned, developed, or mastered in this course to help you become a more marketable candidate in your career field?
- While I enjoy each class at SNHU to varying degrees, each class teaches me that I can always learn something new. I'm not sure I want to be a full-stack developer, but I'm happy that this class gave us so much hands-on experience with code and different technologies we haven't used yet in our curriculum. I now have a better understanding of a MEAN stack and how it connects to create a complex web application.
