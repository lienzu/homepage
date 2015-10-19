== README

This is the front page for testing.

Gemfile hints:

commands:

gem 'rb-inotify', :require => false
gem 'libnotify' if /linux/ =~ RUBY_PLATFORM

rails g scaffold Article order:integer title:string content:text public_at:datetime last_at:datetime new_edit:integer

rails g controller Comments
rails g controller Questions

rails g model Comment commenter_id:integer content:text create_at:datetime question:references

rails g model Question title:string content:text official_answer:text create_at:datetime if_finished:boolean author_id:integer article:references

rails g semantic:install #Configure Assets

1. Controller:
     articles_controller
     comments_controller
     questions_controller
2. Model:
     article.rb
     comment.rb
     question.rb
3. View:
     articles\
