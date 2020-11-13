# HumorMe!
A wonderful world of laughter connecting one sense of humor to another

## General Info

HumorMe! is a CLI application that allows users to create a profile, generate random jokes based on age and category, create a favorites list, and also create new jokes for other users to see! 

### Intro Video (currently unavailabe)
^^^^^^^^

## Technologies

* Ruby - version 2.6.1 
* ActiveRecord - version 6.0
* Rake - 13.0
* Sinatra - version 2.0
* Sinatra-activerecord - version 2.0
* SQLite3 - version 1.4
* tty-prompt  
* tty-box

## Set Up 
 To run this project, install it locally by cloning the Github repository and typing:
 ```ruby
ruby runner.rb
```

## Code Examples
```ruby
def sign_in
        user_input = tty_prompt.ask "Please enter your username..."
        found_user = User.find_by(name: user_input)
        if found_user
            self.user = found_user
            puts "====================="
            puts "Welcome back #{user.name}!"
            puts "====================="
        else
            puts "Username does not exist. Let's try this again..."
            have_you_been_here
        end
    end
```
```ruby
def add_joke_prompt
        puts "Please name your joke:"
        @name = gets.chomp
        puts "Enter your joke"
        @joke = gets.chomp
        @category = tty_prompt.select "Please choose a category:" do |menu|
            menu.choice :Naughty, "Naughty"
            menu.choice :Dad, "Dad"
            menu.choice :Knock_Knock, "Knock_Knock"
            menu.choice :Math, "Math"
            menu.choice :Wizard, "Wizard"
        end
        create_new_joke
    end
```
## Features
* Create Users with age specifications
* Generate random jokes based on category (and age)
* Add any generated joke to a User's Favorites list.
* Create new jokes for other users to enjoy!

To_do: 
* create intro video
* create delete favorites function

## Status
Project status : project requirements reached with options to expand functionality.

## Insperation 
The inspiration for HumorMe! comes from our love to make others laugh and also to instigate more of the same from others using clean code.
## Conatact
```ruby
Craeted by Colter Ulrich and Christopher Henderson
```
[Slack us @ Illicit Syntax :) ](https://flatironschool.zoom.us/j/98415124678?pwd=Ympwcy9oTDljUDlOakk1Mm1LL0YyZz09)

## License 
[Click to view](https://github.com/cju5025/HumorMe)

