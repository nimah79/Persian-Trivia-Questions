# Persian Trivia Questions

This is a SQL databse, containing questions like the questions of [Quiz of Kings](https://quizofkings.com/) or [SnappQ](https://snappq.com/). The data is collected from [@hooshrobot](https://t.me/hooshrobot).

ATM, it contains 17736 four-answer choice questions.

## Requirements

+ MySQL 5+

## Installation

Import `persian_trivia.sql` into your database.

## Database schema

### Table `categories`

| Field | Type         | Null | Key | Default | Extra          |
|-------|--------------|------|-----|---------|----------------|
| id    | int(11)      | NO   | PRI | *NULL*  | auto_increment |
| title | varchar(255) | NO   |     | *NULL*  |                |

### Table `questions`

| Field       | Type         | Null | Key | Default | Extra                    |
|-------------|--------------|------|-----|---------|--------------------------|
| id          | int(11)      | NO   | PRI | *NULL*  | auto_increment           |
| category_id | int(11)      | NO   | MUL | *NULL*  | foreign key (categories) |
| difficulty  | tinyint(4)   | NO   |     | *NULL*  |                          |
| text        | text         | NO   |     | *NULL*  |                          |
| choice1     | varchar(255) | NO   |     | *NULL*  |                          |
| choice2     | varchar(255) | NO   |     | *NULL*  |                          |
| choice3     | varchar(255) | NO   |     | *NULL*  |                          |
| choice4     | varchar(255) | NO   |     | *NULL*  |                          |
| answer      | tinyint(4)   | NO   |     | *NULL*  |                          |
| creator     | varchar(255) | NO   |     | *NULL*  |                          |
