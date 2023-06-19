# Requirement
- php 7.4
- laravel 8

# Auth
- Jwt
- Middleware

# Routes
```
+--------+----------+-------------------+------+----------------------------------------------+------------+
| Domain | Method   | URI               | Name | Action                                       | Middleware |
+--------+----------+-------------------+------+----------------------------------------------+------------+
|        | GET|HEAD | /                 |      | Closure                                      | web        |
|        | POST     | api/auth/login    |      | App\Http\Controllers\AuthController@login    | api        |
|        | POST     | api/auth/logout   |      | App\Http\Controllers\AuthController@logout   | api        |
|        |          |                   |      |                                              | auth:api   |
|        | POST     | api/auth/me       |      | App\Http\Controllers\AuthController@me       | api        |
|        |          |                   |      |                                              | auth:api   |
|        | POST     | api/auth/refresh  |      | App\Http\Controllers\AuthController@refresh  | api        |
|        |          |                   |      |                                              | auth:api   |
|        | POST     | api/auth/register |      | App\Http\Controllers\AuthController@register | api        |
+--------+----------+-------------------+------+----------------------------------------------+------------+
```