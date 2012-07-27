configs
=======

config files for vanilla setups

###Initializing a rails app from template###

[the RailsAppComposer](https://github.com/RailsApps/rails_apps_composer) with some [custom recipes](https://github.com/agnessa/rails_apps_composer) allows to create a template file that can be used to initialize a new project. The current template has the following additions with respect to a default new rails app:
- uses pg
- has a brightbox deploy.rb
- has rspec with factory girl for testing
- has a .travis.yml file and travis build status icon in the README
- has a customised .gitignore
- has ruby-debug19

**To generate a new app from this template:**
  rails new app_from_template -m /path/to/template.txt  -T

To rebuild the template:
1. clone git@github.com:agnessa/rails_apps_composer.git
2. build the gem: 
  gem build rails_apps_composer.gemspec 
3. install the gem: 
  gem install rails_apps_composer-1.5.5.gem --local
4. create the template choosing from the available recipes:
  rails_apps_composer template ~/path/to/template.txt -r pg rspec_fg capistrano devel

