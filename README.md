# chickenshelter
## Chicken Shelter: An Online Platform for Chicken Farming Partnership

<p align="center"><img src="https://s.w.org/images/core/emoji/2.4/svg/1f413.svg" width="300" height="300"></p>

[![license](https://img.shields.io/aur/license/yaourt.svg)]()

## List API

List resource yang dapat diakses antara lain:

| Name                  | URL                                | HTTP Method  |
| ----------------------|:----------------------------------:|:------------:|
| Register User         | `<your_url>/v1/register`           |   **POST**   |
| Login User            | `<your_url>/v1/login`              |   **POST**   |
| Logout User           | `<your_url>/v1/logout`             |   **GET**    |
| Get All Post          | `<your_url>/v1/posts`              |   **GET**    |
| Get Post Detail       | `<your_url>/v1/posts/<id_post>`    |   **GET**    |
| Update Post           | `<your_url>/v1/posts/<id_post>`    |   **PUT**    |
| Delete Post           | `<your_url>/v1/posts/<id_post>`    |   **DELETE** |
| Show All Users        | `<your_url>/v1/profile`            |   **GET**    |
| Show Profile Detail   | `<your_url>/v1/profile/<id_user>`  |   **GET**    |
| Update Profile Detail | `<your_url>/v1/profile/<id_user>`  |   **PUT**    |
| Delete Profile        | `<your_url>/v1/profile/<id_user>`  |   **DELETE** |
| Add Category          | `<your_url>/v1/categories`         |   **POST**   |
| Show All Categories   | `<your_url>/v1/categories`         |   **GET**    |
| Show All Posts Based on Categories | `<your_url>/v1/categories`         |   **GET**    |
| Show All Posts Based on Several Categories| `<your_url>/v1/3categoriesposts` |   **POST** |
| Add Bookmark          | `<your_url>/v1/bookmarks`          |   **POST**   |
| Delete Bookmark       | `<your_url>/v1/bookmarks/<id_post>`|   **DELETE** |
| Show Own Bookmarks    | `<your_url>/v1/bookmarks`          |   **GET**    |
| Show Own Profile      | `<your_url>/v1/ownprofile`         |   **GET**    |
| Show Own Posts        | `<your_url>/v1/ownposts`           |   **GET**    |
| Add Categories by User| `<your_url>/v1/owncategory`        |   **POST**   |
| Update Categories by User| `<your_url>/v1/owncategory`     |   **PUT**    |
| Delete Categories by User| `<your_url>/v1/owncategory`     |   **DELETE** |
| Get All Posts Based on User| `<your_url>/v1/profile/<id_user>/posts` |   **GET** |

# Penjelasan Aplikasi

## Autentikasi

Autentikasi sign up dilakukan dengan memasukkan input request yang berupa nama, email, dan password pada JSON body untuk disimpan ke dalam database. Password disimpan dalam database dengan enkripsi bcrypt. Setelah melakukan sign up, user bisa melakukan login dengan memasukkan email dan password pada input request dengan keluaran berupa token yang di-generate secara random.

## Operasi CRUD pada Posts, Users, Bookmarks, Categories, dan Comments

Operasi CRUD (create, read, update, dan delete) pada tabel posts, users, bookmarks, categories, dan comments dilakukan dengan menggunakan token yang didapatkan saat login. Token tersebut dimasukkan ke header bagian Authorization.

** File blueprint API : apiary.apib **
