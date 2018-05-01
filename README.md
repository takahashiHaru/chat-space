<<<<<<< HEAD
## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|e-mail|string|null: false, add_index unique: true|

### Association
- belongs_to :group
- has_many :group_user
- has_many :messages
- has_many :groups, through::user_group
- has_many :groups, through::group_user
=======
# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:
>>>>>>> parent of 58f440d... edit readme.md

* Ruby version

<<<<<<< HEAD
## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string|null: false|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group
=======
* System dependencies

* Configuration

* Database creation
>>>>>>> parent of 58f440d... edit readme.md

* Database initialization

## user_groupテーブル
<<<<<<< HEAD
## group_userテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|groupe_name|string|null: false|
|user_id|integer|null: false, foreign_key: true|
|message_id|integer|null: false, foreign_key: true|

### Association
- has_many :users, through::user_group
- has_many :messages
- has_many :users, through::group_user
- has_many :group_user
=======
* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
>>>>>>> parent of 58f440d... edit readme.md
