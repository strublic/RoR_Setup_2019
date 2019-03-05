# RoR_Setup_2019

## My Current Enviroment
###### Ruby on Rails
Ruby v2.5, Rails v5.2.2
###### Ruby GEMs to install
Devise
###### Database
Mysql, MongoDB
###### Other Techs
Bootstrap, HTML, APIs, Jquery, js,
###### IDE:
Sublime, ATOM, VSCode
###### Githost:
Github, GitLab, Bitbucket

## Common commands
- rails new project_name *//create a new project in rails*
- rails new project_name -d mysql *//create a new project in rails with mysql*
- rails new project_name -d postgresql *//create a new project in rails with postgres*
- rails server or rails s *//start server*
- rails console or rails c *//start console*
- bundle install      *//install all gems*
- gem install `rails -v 0.14.1`  *//install an specific gem*
- gem install `rails -v '~> 0.14.0'`  *//install an specific gem using a version equal or higher than 0.14.0*
  - version comparators like >= or ~>
- rails generate scaffold mvc_name field_name:type_field *//to create mvc structure ex. `rails generate scaffold post title:string content:text`*
- rails db:create db:migrate *//create project database and migration of your models*
- rails db *//access database*
- rails active_storage:install *//after run `rails db:migrate` to use Active Storage in rails 5.2*
- rake db:drop db:create db:seed *//can use all of them in this sequence*

## Especials commands
- bundle show **gem_name** *//check GEM version ex.: bundle show bootstrap*
- Open project in Atom Text Editor (if in the current project folder)
  - atom /
  - atom .

## Git commands
- git add . *//adds all modified and new (untracked) files in the current directory*
- git commit -m "comment about this changes" *//it like save the files, every time you save it creates a unique ID*
- git push origin <branch> *//how you transfer commits from your local repository to a remote repository*
- git pull *//update the main branch*
- git pull origin development *//update current branch using development branch as reference*
- git status *//check wich file still out of the commit*
- git checkout <branch> *//swap to another branch*
- git checkout -b [name_of_your_new_branch] *//create a new branch and will swap automatically*
  
  ## Commons errors to me
  - Error loading the 'sqlite3' Active Record adapter... (my current ruby version was 2.5.3)
  - Objects folder in .git is extremely large for my small project
