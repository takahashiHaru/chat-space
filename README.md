## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false, add_index|

### Association
- has_many :group_users
- has_many :messages
- has_many :groups, through: :group_users


## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string|null: false|
|group_user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group


## group_usersテーブル

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
|group_name|string|null: false|
|group_user_id|integer|null: falese|

### Association
- has_many :group_users
- has_many :users, through: :group_users
- has_many :messages
