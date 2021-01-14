# README

## users テーブル

| Column     | Type   | Options     |
| --------   | ------ | ----------- |
| password   | string | null: false |
| email      | string | null: false |
| name       | string | null: false |
| profile    | text   | null: false |
| occupation | text   | null: false |
| position   | text   | null: false |

### Association
- has_many :comments
- has_many :prototypes







## comments テーブル

| Column    | Type       | Options                            |
| ------    | ------     | ---------------------------------- |
| text      | text       | null: false                        |
| user      | references | null: false, foreign_key: true     |
| prototype | references | null: false, foreign_key: true     |

### Association

- belong_to :user
- belong_to :prototype






## prototype テーブル

| Column     | Type       | Options                        |
| ------     | ---------- | -----------------------------  |
| title      | string     | null: false,                   |
| catch_copy | text       | null: false,                   |
| concept    | text       | null: false                    |
| user       | references | null: false ,foreign_key: true |
| image      |            |                                |

### Association

- has_many :comments
- belong_to :user
