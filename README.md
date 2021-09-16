# テーブル設計

## usersテーブル

| Column    | Type   | Option     |
| ----------| -----  | -------    |
| email     | string | NOT NULL   |
| password  | string | NOT NULL   |
| name      | string | NOT NULL   |
| profile   | text   | NOt NULL   |
| occupation| text   | NOT NULL   |
| position  | text   | NOT NULL   |


### Association

- has_many  : prototypes
- has_many  : comments


## prototypesテーブル


| Column     | Type      | Option     |
| ---------- | -----     | -------    |
| title      | string    | NOT NULL   |
| catch_copt | text      | NOT NULL   |
| concept    | text      | NOT NULL   |
| image      |           |            |
| user       | reference |            |

### Association

- belongs_to : user
- has_many   : comments




## commentsテーブル

| Column     | Type      | Option     |
| ---------- | -----     | -------    |
| text       | text     | NOT NULL   |
| user       | reference |            |
| prototype  | reference |            |


### Association

- belongs_to : user
- belongs_to : prototype





