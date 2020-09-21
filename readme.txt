1) Create virtual environment by using below command (Open folder path in python)
python3 -m venv myvenv

2) activate virtual environemnt by using below command
myvenv\Scripts\activate

3) install packages by using below command
pip install -r requirements.txt

4) start server by using below command
python manage.py runserver

5) open below URL in browser
http://127.0.0.1:8000/ipaddr/

6) Add below json payload into content section and click on post button, it will save that single IP address into database with "available" status.

{
	"ip_address": "10.0.0.1"
}

7) Add below json payload into content section and click on post button, it will save that multiple IP addresses (from 2 to 25) into database with "available" status.

{
	"ip_address": "10.0.0.2/25"
}

8) Open below URL in browser to fetch single record with "1" id
http://127.0.0.1:8000/ipaddr/1/

9) Add below json payload into content section to update status from "available" to "acquired" and click on put button. It will "Acquire" that IP 

{
    "ip_address": "10.0.0.1",
    "status": "acquired"
}

10) Add below json payload into content section to update status from "acquired" to "available" and click on put button. It will "Release" that IP 

{
    "ip_address": "10.0.0.1",
    "status": "available"
}


11) open below URL in browser and hit enter button to see list of IP address with current status.
http://127.0.0.1:8000/ipaddr/

12) If you provide incorrect range it will end up with error

{
	"ip_address": "10.0.0.30/26"
}

13) Open below URL in browser to fetch single record with "1" id and click on "Delete" button if you want to delete that record.
http://127.0.0.1:8000/ipaddr/1/

14) below super user is available
http://127.0.0.1:8000/admin/
username: admin
password: password

### Had extra time to add common usecase features like Delete, admin, error with code**








