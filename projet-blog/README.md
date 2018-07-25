## > Da Blog Project  <

Premier projet avec Rails la mif !

## Gems 
ActiveRecord pour gérer la database sqlite3 database, et la gem "Faker" pour donner un sens à notre database sur le fichier seed.

## Notre process
Utiliser les Rails pour produire des classes et des migrations pour Users, Articles, .

```ruby
$ rails generate model User
```
We then filled the migration and class files.

## Lance le projet

```ruby
$ bundle install
```

Seed the database with Faker names from the file db/seeds.rb created during the exercise

```ruby
$ rails db:seed
```

## Architecture
5 tables dans notre DataBase:

users :
- first_name
- last_name
- email

articles :
- title
- content
- user_id
- category_id

comments :
- content
- user_id
- article_id

categories :
- name

likes :
- user_id
- article_id

# Depuis la console Rails

Pour créer une nouvel utilisateur :

```ruby
> User.create(first_name: "name", last_name: "last_name", email: "email")
```
Pour créer un nouvel article

```ruby
> Article.create(user_id: user_id, title: "title", content: "content")
```
Pour avoir accès à base de donnée, tu peux utiliser DB Browser for sqlite3
