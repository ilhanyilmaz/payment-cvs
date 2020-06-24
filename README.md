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

#pip install psycopg2 django djangorestframework requests urllib3
git clone https://github.com/ilhanylmaz/payment-cvs.git
#git config --global core.autocrlf true / false ???


Update Server & Commit
========================
git add .
git commit -m "message"
eb deploy kidguru-backend-dev
git push git@gitlab.com:ilhanylmaz1/kidguru-backend.git


Change local server ip command
==============================
sed -i 's/192.168.254.109/192.168.254.106/g' kidguru_backend/settings.py runserver.sh