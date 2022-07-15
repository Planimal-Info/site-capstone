# Project Plan

Pod Members: Amaar, Kevin, Valerie

## Problem Statement and Description

Insert the latest summary of your problem statement and app description.
- We want people to be able to enjoy nature and going on an adventure while also getting to share it with there friends and family or to anyone that wants to see. 

## User Roles and Personas

User Roles:
- User 
- Administrator
- Viewer (Not Logged In)


User Persona’s: 

User: 
- John Use is a 20 year old Botony Student at the University of Nowhere. He wants to study local flora for a class project. He uses a phone mostly, and wants to use the site to research local plants and animals. Might not know how to navigate through the website. Another pain point is not finding a animal or plant he is looking for in the database. 

- Jane Use is a 28 year old local plant and animal enthusiast. They like to go out into national parks and look for interesting animals and plants they find. They want to use the website to record and post pictures of animals and plants they find out on their journeys. Pain points include picture not loading when they upload one. 

Administrator: 
- John Admin is a 40 year old is a Professor who has 20 years of experience in Botony. He uses the website as a tool in class and wants to keep photos of animals and plants accurate. His role as an administrator is to verify photos of animals and plants are accurate and can remove ones that dont match. 

- Jane Admin, 52, is the head of a non-profit organization that specializes in local animals and plants. They sponsor the website and use it to help achieve their goals as an organization. They also help make sure users can access their accounts and fix problems related to that. 

Viewer (Not Logged In)
- John View has a hobby of researching local animals and plants, and wants to be able to search and learn. He searches around and finds our website. Looks through the landing page and wants to use our website to learn more about his hobby.

- Jane View  is a gardener and wants to be able to share the cool photo’s they take on the job. They come to the website and register to be able to do so. 


## User Stories
User Stories:
1. As a viewer, I want to create an account, so that I can post photos of animals I find. 
2. As a viewer, I want to learn more about the website, to help me with my interests.
3. As a Administrator, I want to verify photos are accurate, so that people have correct information. 
4. As a Administrator, I want help users access their accounts, so that people can use the website.
5. As a Administrator, I want to remove post that shares inaccurate information, so that people have access to accurate information. 
6. As a Administrator, I want to deactivate/ban users who use the website in a malicious way. 
7. As a user, I want to search for animals/plants and see related posts.
8. As a user, I want to login and share photos I’ve taken to show my friends. 
9. As a user, I want to register and use the website, to research local animals and plants for my class.
10. As a user, I to be able to log out after posting the cool photo’s I’ve taken.
11. As a user, I want to get more info about a post, to learn more about the photo.
12. As a user, I want to see all the posts i’ve made, to show my family and friends. 
13. As a User, I want to see how many likes my posts got, to see how many people like it. 
14. As a User, I want to like this post, because I like the photo.
15. As a User, I want to update my profile information, because I changed my email.
16. As a user, I want to delete my account, because I've finished my research paper




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
| id | xxx | xxx |
| is_admin | xxx | xxx |
| first_name | xxx | xxx |
| last_name | xxx | xxx |
| email | xxx | xxx |
| password | xxx | xxx |
| created_at | xxx | xxx |

Likes:
| column name	  | type  | description |
| :------------ |:--------------- | :-----|
| id | xxx | xxx |
| user_id | xxx | xxx |
| post_id | xxx | xxx |

Users_Posts:
| column name	  | type  | description |
| :------------ |:--------------- | :-----|
| id | xxx | xxx |
| photo | TEXT | image url |
| user_post_desc | xxx | xxx |
| user_id | xxx | xxx |
| likes | xxx | xxx |
| created_at | xxx | xxx |
| updated_at | xxx | xxx |
| user_post_title | xxx | xxx |
| image_title | xxx | xxx |

Plant_And_Animals:
| column name	  | type  | description |
| :------------ |:--------------- | :-----|
|id | xxx | xxx |
| common name | xxx | xxx |
| scientific name | xxx | xxx |
| last_seen | xxx | xxx |
| conservation_rate | xxx | xxx |

## Endpoints

List the API endpoints you will need to implement.
Endpoints: 

Authentication Endpoints:
| CRUD |	HTTP | Verb	Description |	User stories |
| :------------ |:--------------- | :-----| :----|
|id | xxx | xxx | xxx |

Gets the current user based off of token in local storage.
 - auth/me | Method: GET
Post request to register user and add to database.
 - auth/register | Method: POST
Post request to login uesr and store token. 
 - auth/login | Method: POST


Search Endpoints:

Searches both Animal/Plant databases and user post database and displays Animal/Plant info and related posts. 
 - search/:input | Method: GET

User-Post’s Endpoints

Post request to create post
 - post/create | Method: POST
Get request that gets the post with that specific post id
 - post/posts/:post_id | Method: GET
Get request to get all the posts made by a user
 - post/user/:user_id | Method: GET
Gets the likes for a post
 - post/likes/:post_id | Method: GET
Updates the likes for a post 
 - post/updateLikes/:post_id  | Method: POST | Input: Post_id, User_id, +1 or -1 to increment or decrement

Profile Endpoint:

Get request to get user information. 
- profile/user_id  | Method: Get
- Delete User Profile
-profile/delete/  | Method: Delete

Administrator Endpoints:

Get flagged posts:
- admin/flaggedPosts | Method: Get


***Don't forget to set up your Issues, Milestones, and Project Board!***
