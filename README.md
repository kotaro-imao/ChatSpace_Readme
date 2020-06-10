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

## userテーブル  
|Column｜Type|Option|  
|-------|----|------|  
|email|strings|null: fales|  

|password|strings|null: fales|  
|user|strings|null: fales|  
### Association  
- has_many :massages  

## groupoes_usersテーブル  
|Column｜Type|Option|  
|------|-----|------|  
|user_id|integer|null: fales, foreign_key: true|  
|groupes_id|integer|null: fales, foreign_key: true|  
### Association  
- has_many :comments  

## massageテーブル  
|Column｜Type|Option|  
|------|-----|------|  
|body|text|null: fales|  
|image|string|null: fales|  
|time|integer|null: fales|  
|groupe_id|integer|null: fales, foreign_key: true|  
|user_id|integer|null: fales, foreign_key: true|  
### Association  
- belongs_to :user  