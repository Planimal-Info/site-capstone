# Project Plan

Pod Members: Amaar, Kevin, Valerie

## Problem Statement and Description

Problem Statement: 
New York State lacks a easy to use plant and animal database that academics and hobbyists can readily access.

We want students in high school and college, as well as educators to have an easy to use, searchable database of local plants and animals. By grabbing data from a public new york state database, parsing it and returning relevant information. We will also allow users to upload and share photos of either animals or plants that they find in New York.

## User Roles and Personas

User Roles:
- User 
- Administrator
- Viewer (Not Logged In)


User Persona’s: 

User: 
- John Use is a 20 year old Botony Student at the Cornell University. He wants to study local flora for a class project. He uses a phone mostly, and wants to use the site to research local plants and animals. Might not know how to navigate through the website. Another pain point is not finding a animal or plant he is looking for in the database. 

- Jane Use is a 28 year old local plant and animal enthusiast. They like to go out into national parks and look for interesting animals and plants they find. They want to use the website to record and post pictures of animals and plants they find out on their journeys. Pain points include picture not loading when they upload one. 

Administrator: 
- John Admin is a 40 year old is a Professor who has 20 years of experience in Botony. He uses the website as a tool in class and wants to keep photos of animals and plants accurate. His role as an administrator is to verify photos of animals and plants are accurate and can remove ones that dont match. 

- Jane Admin, 52, is the head of a non-profit organization that specializes in local animals and plants. They sponsor the website and use it to help achieve their goals as an organization. They also help make sure users can access their accounts and fix problems related to that. 

Viewer (Not Logged In)
- John View has a hobby of researching local animals and plants, and wants to be able to search and learn. He searches around and finds our website. Looks through the landing page and wants to use our website to learn more about his hobby.

- Jane View  is a gardener and wants to be able to share the cool photo’s they take on the job. They come to the website and register to be able to do so. 


## User Stories
User Stories:
[x] 1. As a Viewer, I want to create an account, so that I can post photos of animals I find. 
[x] 2. As a Viewer, I want to learn more about the website, to help me with my interests.
[ ] 3. As a Administrator, I want to verify photos are accurate, so that people have correct information. 
[ ] 4. As a Administrator, I want to help users access their accounts, so that people can use the website.
[ ] 5. As a Administrator, I want to remove post that shares inaccurate information, so that people have access to accurate information. 
[ ] 6. As a Administrator, I want to deactivate/ban users who use the website in a malicious way. 
[x] 7. As a User, I want to search for animals/plants and see related posts.
[ ] 8. As a User, I want to login and share photos I’ve taken to show my friends. 
[x] 9. As a User, I want to register and use the website, to research local animals and plants for my class.
[x] 10. As a User, I to be able to log out after posting the cool photo’s I’ve taken.
[x] 11. As a User, I want to get more info about a post, to learn more about the photo.
[ ] 12. As a User, I want to see all the posts i’ve made, to show my family and friends. 
[ ] 13. As a User, I want to see how many likes my posts got, to see how many people like it. 
[ ] 14. As a User, I want to like this post, because I like the photo.
[ ] 15. As a User, I want to update my profile information, because I changed my email.
[ ] 16. As a user, I want to delete my account, because I've finished my research paper




## Pages/Screens

List all the pages and screens in the app. Include wireframes for at least 3 of them.

- / (home page)
- /search/:search-term (input value of serch term)
- /login
- /register
- /upload
- /feed
- /profile
- /admin

[![SF3 Wireframe](https://github.com/Planimal-Info/site-capstone/blob/main/planning/sf3-wireframes.png)](https://www.figma.com/file/vaB5YDrFhAHKKJcsnYlLOn/SF3---Capstone-Wireframe?node-id=0%3A1)
*vertical scrolling in Preview for Search Results, Feed and Profile

## Data Model

Users:
| column name	  | type  | description |
| :------------ |:--------------- | :-----|
| id | INTEGER | primary key |
| is_admin | BOOLEAN  | check if user is admin |
| first_name | TEXT  | user's firat name |
| last_name | TEXT  | user's last name |
| email | TEXT | user's email |
| password | TEXT  | user's password |
| created_at | DATE  | date of user's account creation |

Likes:
| column name	  | type  | description |
| :------------ |:--------------- | :-----|
| id | INTEGER | primary key |
| user_id | INTEGER | foreign key to user table |
| user_post_id | INTEGER | foreign key to user posts table |

Users Posts:
| column name	  | type  | description |
| :------------ |:--------------- | :-----|
| id | INTEGER | primary key |
| photo | TEXT | image url |
| user_post_desc | TEXT | description of uploaded photo |
| user_id | INTEGER | foreign key to user table |
| likes | INTEGER | number of likes on post |
| created_at | DATE | date of user post creation |
| updated_at | DATE | date of user post update |
| user_post_title | TEXT | title of post |

Plant_And_Animals:
| column name	  | type  | description |
| :------------ |:--------------- | :-----|
|id | INTEGER | primary key |
| common name | TEXT | common english name of animal |
| scientific name | TEXT | scientific name of animal |
| last_seen | DATE | date animal was last spotted |
| conservation_rate | TEXT | conservation classification |

## Endpoints

Endpoints: 
| CRUD |	HTTP Verb |	Params | Description |	User stories |
| :------------ |:--------- |:----- | :-----| :----|
|Read | GET | auth/me | Gets User based on token in local storage | 8 |
|Create | POST | auth/login | Login User | 8 |
|Create | POST | auth/register | Register User| 1, 9 |
|Read | GET | search/user/:searchInput | Searches User Posts Database for Input | 2, 7 | 
|Read | GET | search/db/:searchInput | Searches Animal/Plants Database for Input | 2, 7 | 
|Create | POST | post/create | Creates a post from a user | 8, 10 |
|Delete | DELETE | post/delete | Delete user post |5|
|Read | GET | post/posts/:postId | Gets that post_id  | 11 | 
|Read | GET| post/user/:userId | Get all the posts from that user |12 | 
|Read | GET | post/likes/:postid | Get all the likes from a post | 13 |
|Update | PUT | post/updateLikes/:postid | Update Likes for a post | 14 |
|Read | GET | profile/:user_id | Get Profile information on a user | 15 |
|Update | PUT | profile/:user_id | Update user information | 15 |
|Delete | DELETE | profile/delete | Delete user profile |6, 16|
|Read | GET | admin/flaggedPosts |Get flagged posts|3|


***Don't forget to set up your Issues, Milestones, and Project Board!***
