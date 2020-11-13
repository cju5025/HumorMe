# HumorMe!
A wonderful world of laughter connecting one sense of humor to another

## General Info

HumorMe! is a CLI application that allows users to create a profile, generate random jokes based on age and category, create a favorites list, and also create new jokes for other users to see! 

### Intro Video (currently unavailable)
^^^^^^^^

## Technologies

* Ruby - version 2.6.1 
* ActiveRecord - version 6.0
* Rake - 13.0
* Sinatra - version 2.0
* Sinatra-activerecord - version 2.0
* SQLite3 - version 1.4
* Tty-prompt  
* Tty-box

## Set Up 
 To run this project, install it locally by cloning the Github repository and typing:
 ```ruby
ruby runner.rb
```

## Code Examples
```ruby
    def have_you_been_here 
        user_input = tty_prompt.yes? "Welcome to HumorMe! Been here before?"
            user_input ? sign_in : sign_up
    end
```
```ruby
    def main_menu_choice
        case @menu_choice
        when "Jokes"
            select_joke_type
        when "Favorites"
            user.display_favorite_jokes
            main_menu_option
        when "Add"
            add_joke_prompt
        when "Exit"
            exit_app
        end
    end
```
## Features
* Create users with age specifications
* Generate random jokes based on category (and age)
* Add any generated joke to a user's Favorites list
* Create new jokes for other users to enjoy!

To_do: 
* create intro video
* create delete favorites function

## Status
Project status : project requirements reached with options to expand functionality.

## Inspiration 
The inspiration for HumorMe! comes from our love to make others laugh and also to instigate more of the same from others using clean code.
## Contact
```ruby
chenderson5280@gmail.com
cju5025@gmail.com
Created by Colter Ulrich and Christopher Henderson
```

## License 
[Click to view](https://github.com/cju5025/HumorMe)

