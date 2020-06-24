PAYMENT TO CVS
==========================

Creator
---------------
İlhan Yılmaz


Setup Development Environment:
==============================
\- Install python3, virtualenv
mkdir payment-cvs
cd payment-cvs
virtualenv env
source env/Scripts/activate

pip install psycopg2 django djangorestframework requests urllib3
git clone https://gitlab.com/ilhanylmaz1/kidguru-backend.git
git config --global core.autocrlf true / false ???
cd kidguru_backend
python manage.py makemigrations
python manage.py migrate
python manage.py createsu \-\-username <username\> \-\-email <email\> \-\-password <password\>
python manage.py initdb : initializes cities districts and neighbourhoods

winpty python manage.py createsuperuser
python manage.py runserver 192.168.1.8:8080 --nostatic
or
. ./runserver.sh

pip install awsebcli


Update Server & Commit
========================
git add .
git commit -m "message"
eb deploy kidguru-backend-dev
git push git@gitlab.com:ilhanylmaz1/kidguru-backend.git


Change local server ip command
==============================
sed -i 's/192.168.254.109/192.168.254.106/g' kidguru_backend/settings.py runserver.sh