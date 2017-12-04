## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

1. List the five common HTTP verbs and what the purpose is of each verb.
  post, delete, get, patch, put
2. What is Sinatra?
  Sinatra DSL is a simpler alternative to Ruby frameworks such as Ruby on Rails for quickly creating web applications with minimal effort.
4. What is MVC?
  model, controller, views
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  so they go to the right spot
6. What types of variables are accessible in our view templates without explicitly passing them?
local variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  ```ruby
  get '/horses' do
    @count = 1
    render locals: { name : 'Mr. Ed' }
    erb :index
  end
  ```
9. What's the purpose of ERB?
  To describe how data should be used to create HTML
10. Why do I need a development AND test database?
  So that any new records created in test dont affect the database and aren't stored in development
11. What is CRUD and why is it important?
  create.read.update.delete
12. What does HTTP stand for?
 hyper text transfer protocol
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<%= %> prints content.
<% %> doesnt print content.
14. What's an ORM?
  object relational mapping
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  active record
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
17. What's a migration?
  any kind of change to a database including creating a table, changing a table name adding and subracting columns and even changing data types.
18. When you create a migration, does it automatically modify your database?
  no
19. How does a model relate to a database?
  model reflects a table in a database.

20. What is the difference between `#new` and `#create`?
  `#new` simply creates a new instance. `#create` will create the new instance AND save it to the database.

Review Questions:
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?
`films = CSV.open './db/csv/films.csv', headers:true, header_converters: :symbol
films.each do |row|
  Station.create!(id: row[:id], title: row[:title], desciption: row[:description])
end`
22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?
  activities[:hiking][:supplies].unshift("granola bar")
23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  Encapsulation
  Abstraction
  Polymorphysism
  Anheritence


