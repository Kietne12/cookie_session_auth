# Test cookie_session_auth

1. Gửi request:  
POST http://localhost:3000/auth/register
Body: `username=admin, password=12345`  
![Register Request](public/results/register.png)
![User in Mongo after Register](public/results/user_db.png)

2. Gửi request:  
POST http://localhost:3000/auth/login 
Body: `username=admin, password=12345`  
![Login Request](public/results/login.png)
![Login in Mongo after Register](public/results/login_db.png)

3. Gửi request:  
GET http://localhost:3000/auth/profile
![Profile Response](public/results/profile.png)

4. Gửi request:  
GET http://localhost:3000/auth/logout
![Logout Response](public/results/logout.png) 
Kiểm tra lại trong DB → session đã bị xoá:  
![DB After Logout](public/results/db_after_logout.png)

5. Truy cập profile sau khi logout:  
GET http://localhost:3000/auth/profile
![Profile After Logout](public/results/profile_after_logout.png)