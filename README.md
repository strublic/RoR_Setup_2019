# RoR_Setup_2019

## Atualizar com:
###### RVM (Ruby Version Manager)
###### PostgreSQL install step (https://r00t4bl3.com/post/how-to-install-postgresql-11-on-linux-mint-19-tara)
###### RDBMS PostgreSQL DBeaver (https://dbeaver.io/download/)

## My Current Environment
###### Ruby on Rails
Ruby v2.6.1, Rails v5.2.2
###### Ruby GEMs to install
Devise, bootstrap, jquery-rails, jquery-ui-rails, pry-byebug, cocoon, client_side_validations, rails-i18n, cancancan
###### Database
Mysql, MongoDB, PostgreSQL
###### Other Techs
Bootstrap, HTML, APIs, Jquery, js,
###### IDE:
Sublime, ATOM, VSCode
###### Githost:
Git, Github, GitLab, Bitbucket
###### Test:
RSpec
###### Terminal:
Terminator, zsh


# First of All

## Setup a Linux environment (Ubuntu/Mint)
  ### Upgrade your terminal
   *//update all packages*
  - sudo apt-get update
  - sudo add-apt-repository ppa:gnome-terminator/nightly-gtk3
  - sudo apt-get update
  - sudo apt-get install terminator
  => link: https://www.edivaldobrito.com.br/emulador-de-terminal-terminator-no-ubuntu/
  
  ### Install zsh on the terminal
  - sudo apt-get install zsh curl git
  - sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
  => link: hhttp://www.boekhoff.info/how-to-install-zsh-and-oh-my-zsh/
  
  ### Install git
   *//update all packages*
  - sudo apt-get update
  
   *//install Git and others dependencies*
  - sudo apt-get install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev libxml2-dev libxslt1-dev libcurl4-openssl-dev software-properties-common libffi-dev 
  
  ### Install rbenv
  - git clone https://github.com/rbenv/rbenv.git ~/.rbenv
  - echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
  - echo 'eval "$(rbenv init -)"' >> ~/.bashrc
  - exec $SHELL
  - git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
  - echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
  - exec $SHELL
  - rbenv version
  
  ### Install Ruby
  *//intalling ruby in rbenv*
  - rbenv install 2.6.1 
  
  *//check version*
  - ruby -v 
  
  *//set as global*
  - rbenv global 2.6.1 
  
  ### Install bundler gem (dependency manager)
  - gem install bundler
  - rbenv rehash
  
  ### Config git
  *//git command colorful*
  - git config --global color.ui true 
  - git config --global user.name "your name here"
  - git config --global user.email "email@example.com"
  
  ### Generate SSH key and copyng repo
  - ssh-keygen -t rsa -b 4096 -C "email@example.com"
  
  *//show ssh key then select with your mouse and copy it*
  - cat ~/.ssh/id_rsa.pub 
  
  *//connecting with github*
  - ssh -T git@github.com 
  - Go to github site in your browser then go to SSH page and add your ssh key that you already copied
  
  ### Install Rails
  - gem install rails -v 5.2.2
  - rails -v
  
  ### Install PostgreSQL
  *//get a example ropository*
  - sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ xenial-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
  - wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
  - sudo apt-get update
  *//install postgresql*
  - sudo apt-get install postgresql-common
  - sudo apt-get install postgresql-9.5 libpq-dev
  
  ### Config Postgre user
  - sudo -u postgres createuser set_here_user_name
  
  ### Install Node.js
  - curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.2/install.sh | bash
  - source ~/.bashrc
  - nvm install 4.4.7
  
  ### First Rails project
  - mkdir projects
  - cd projects
  - rails new app
  - cd app
    
  ### Running Rails project
  - bundle exec rails db:migrate
  - rails s
  
  *//in your browser*
  - localhost:3000 

  ### Create Github repository
  - Go to github site > create new repository > set the name of you project/repository > click in Create
  - Follow the instructions that github provide to setup in your local terminal
  
## Extras
### Common commands
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

### Especials commands
- bundle show **gem_name** *//check GEM version ex.: bundle show bootstrap*
- Open project in Atom Text Editor (if in the current project folder)
  - atom /
  - atom .

### Git commands
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
