## > Da Blog Project  <

Premier projet avec Rails la mif !

## Doc & Gems
ActiveRecord pour gérer la database sqlite3 database, et la gem "Faker" pour donner un sens à notre database sur le fichier seed.

## Process
Utiliser les Rails pour produire des classes et des migrations pour Users, Articles, .

```ruby
$ rails generate model User
```
Puis on fignole les fichiers migration et les classes. 

## Lancer le projet

```ruby
$ bundle install
```

Nourris la database avec des faker noms depuis le fichier db/seeds.rb 

```ruby
$ rails db:seed
```

## Architecture du Doss
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
# Pour avoir accès à base de donnée, 

tu peux utiliser DB Browser for sqlite3
