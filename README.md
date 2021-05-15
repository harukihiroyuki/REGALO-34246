# README
<<<<<<< Updated upstream
## usersテーブル

| Column               | Type       | Options                       |
| ------               | ------     | -----------                   |
| name                 | string     | null: false                   |
| email                | string     | null: false, unique :true     |
| encrypted_password   | string     | null: false                   |
| lastname             | string     | null: false                   |
| firstname            | string     | null: false                   |
| birthday             | date       | null: false                   |
| age_id               | integer    | null: false                   |
| gender_id            | string     | null: false                   |
- has_many :items
- has_many :sends



## itemsテーブル

| Column            | Type       | Options                         |
| ------            | ------     | -----------                     |
| name              | string     | null: false                     |
| category_id       | integer    | null: false                     |
| item_condition_id | integer    | null: false                     |
| country_id        | integer    | null: false                     |
| send_day_id       | integer    | null: false                     |
| user              | references | null: false, foreign_key: true  |
| text              | text       | null: false                     |
- belongs_to :user
- has_one :send
## sendsテーブル

| Column     | Type       | Options                           |
| ------     | ------     | -----------                       |
| item       | references | null: false, foreign_key :true    |
| user       | references | null: false, foreign_key :true    |

- belongs_to :user
- belongs_to :item
- has_one :address


## addressesテーブル

| Column           | Type          | Options                          |
| ------           | ------        | -----------                      |
| send              | references    | null: false, foreign_key :true  |
| prefecture_id    | integer       | null: false                      |
| city             | string        | null: false                      |
- belongs_to :send


This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version
rails _6.0.0_
* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions