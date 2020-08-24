---
layout: post
title:      "Making a better Seed"
date:       2020-08-24 04:20:58 +0000
permalink:  making_a_better_seed
---

If you've ever started a project and as you built and tested realized the data you have just created needs to be reworked you'll quickly look into creating a seed file. Recreating data over and over isn't just time consuming, but also adds insult to injury as you're recreating the data is often because you ran into an issue and had to drop your database and rework it. Although if you have a seed file you can quickly generate needed data to continue testing your app and move on your way. Simple enough right? Just make a seeds.rb file in your db folder and off you go, it'll even give you examples on how to do it:
```
Examples:

   movies = Movie.create([{ name: 'Star Wars' }, { name: 'Lord of the Rings' }])
   Character.create(name: 'Luke', movie: movies.first)
```

How nice right. Although sometime your apps will be a bit more complex and you'll need to add ids to your seed data to generate the data you'll need. For example what if in our example we also needed a user_id?

```
User.create(name: "Steven", password: "Jarjar")
Character.create(name: 'Luke', movie: movies.first, user_id: 1)
```

Sure we could hard code it as I have shown above, but what happens if we delete the User with an id of 1? Or like me you didn't start by seeding your database and created a seed file after a few failed attempts and there is no longer a User 1 in your database. Yes you could search in the console to find a valid user or you could let the database find that information for you. Okay let me explain instead of directly populating your seed file with data, why not ask the seed file to find a User for you:

```
User.create(name: "Steven", password: "Jarjar")
Character.create(name: 'Luke', movie: movies.first, user_id: User.first.id)
```

That's right the seed file can just seed itself for user_id by looking for the first user in the User class and then pulling out the id number for us and we know that data will be valid because it came directly from the database. 
  
