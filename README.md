ubuntu 16.04.4

     1  curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash -
     2  sudo apt-get install -y nodejs
     3  sudo apt-get install -y postgresql-9.5
     4  sudo apt-get install -y build-essential python3-dev python3-pip \
                                python3-cffi libcairo2 libpango-1.0-0 libpangocairo-1.0-0
     5  git clone https://github.com/jujinesy/initsaleor.git
     6  export LC_ALL=C
     7  pip3 install virtualenv
     8  virtualenv -p python3 venv
     9  source venv/bin/activate
    10  cd initsaleor
    11  pip install -r requirements_dev.txt
    12  export SECRET_KEY='<mysecretkey>'
    13  sudo -u postgres createuser -P -s saleor
    14  sudo -u postgres createdb saleor
    15  python manage.py migrate
    16  npm install
    17  npm run build-assets
    18  npm run build-emails
    19  python manage.py runserver 0.0.0.0:8000


mac 10.13.3 

    Node.js
    Version 8 or later is required.

    PostgreSQL
    Saleor needs PostgreSQL version 9.4 or above to work.

    xcode-select --install
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    brew install python3
    brew install git
    brew install cairo pango gdk-pixbuf libffi
    git clone https://github.com/jujinesy/initsaleor.git
    cd initsaleor
    pip install -r requirements_dev.txt
    export SECRET_KEY='<mysecretkey>'
    db 아디, 비번, 테이블명 saleor 
    npm install
    npm run build-assets
    npm run build-emails