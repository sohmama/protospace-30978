# テーブル設計

## usersテーブル

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| email      | string | null: false |
| password   | string | null: false |
| name       | string | null: false |
| profile    | text   | null: false |
| occupation | text   | null: false |
| position   | text   | null: false |

### Association
- has_many :title
- has_many :catch_copy
- has_many :concept
- has_many :prototype

## prototypesテーブル
| Column      | Type       | Options     |
| ----------- | ---------- | ----------- | 
| title       | string     | null: false |
| catch_copy  | text       | null: false |
| concept     | text       | null: false |
| image       |            |             |
| user        | references |             |

### Association 
- has_many :text
- has_many :user
- has_many :prototype

## commentsテーブル
| Column    | Type       | Options     |
| --------- | ---------- | ----------- |
| text      | text       | null: false |
| user      | references |             |
| prototype | references |             |