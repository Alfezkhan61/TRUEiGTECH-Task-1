
Deployment link
LINK - https://trueigtech-task-1.onrender.com/login

Screenshots - 
![alt text](<Screenshot (24).png>) ![alt text](<Screenshot (25).png>) ![alt text](<Screenshot (26).png>) ![alt text](<Screenshot (27).png>) ![alt text](<Screenshot (28).png>)


📸 Instagram Mini Clone – Backend (Task 1)
This project is a basic Instagram-style backend built as part of Task 1 for the TRUEiGTECH assignment.
It focuses on implementing core backend functionalities such as authentication, posts, likes, comments, follow system, and feed generation.
The goal of this project is to demonstrate backend logic, database relationships, and REST API design.

🚀 Features
🔐 User Authentication


User signup and login


Password hashing for security


Token-based authentication (JWT)


Protected routes for authenticated users


👥 Follow System


Users can follow other users


Users can unfollow


Maintains proper follower–following relationships


🖼️ Post Management


Authenticated users can create posts


Each post contains:


Image URL


Caption




Users can view posts created by followed users


❤️ Likes


Users can like a post


Users can unlike a post


Prevents duplicate likes from the same user


💬 Comments


Users can comment on posts


Each comment stores:


Comment text


Commented user details




📰 Feed


Personalized feed API


Shows posts only from users the logged-in user follows


Includes likes and comments data



🗄️ Database Design
The project uses a relational/NoSQL database (based on implementation) with the following core entities:
User


_id


username


email


password (hashed)


followers (array of user IDs)


following (array of user IDs)


createdAt


Post


_id


userId (reference to User)


imageUrl


caption


likes (array of user IDs)


createdAt


Comment


_id


postId (reference to Post)


userId (reference to User)


commentText


createdAt


Relationships used:


User ↔ User (Many-to-Many) → Follow system


User ↔ Post (One-to-Many)


Post ↔ Comment (One-to-Many)


User ↔ Post (Many-to-Many) → Likes



🔌 API Design
Authentication APIs


POST /api/auth/signup – Register a new user


POST /api/auth/login – Login user and return token


User & Follow APIs


POST /api/users/follow/:userId – Follow a user


POST /api/users/unfollow/:userId – Unfollow a user


Post APIs


POST /api/posts – Create a new post


GET /api/posts/feed – Get feed for logged-in user


Like APIs


POST /api/posts/:postId/like – Like a post


POST /api/posts/:postId/unlike – Unlike a post


Comment APIs


POST /api/posts/:postId/comment – Add comment to post



All protected routes require a valid authentication token.


▶️ How to Run the Project
Prerequisites


Node.js installed


npm installed


Database configured (MongoDB / other as used)


Steps to RUN
# install packages
npm run install-frontend

# start server
npm run start

The server will start on the configured port (default mentioned in .env).

👤 Author
Alfez Khan
B.Tech CSE
Task Submission – TRUEiGTECH (Task 1)



