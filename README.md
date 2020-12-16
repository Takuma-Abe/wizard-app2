# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

# DB setting

* user table
|column name|type|option|
|nickname|string|null: false|
|family_name|string|null :false|
|first_name|string|null :false|
|family_kana|string|null :false|
|first_kana|string|null :false|
|birthday|date|null :false|
※ password & email are default in devise

* user model association
- has_one :address, dependent: :destroy

* address table
|column name|type|option|
|prefecture|integer|null :false|
|postal_code|string|null :false|
|city|string|null :false|
|address|string|null :false|
|building|string|----|
|phone_number|string|null :false|
|user|references|foreign_key:true|

* address model association
- belongs_to :user
