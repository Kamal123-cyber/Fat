This is Vendor Management System Project mainly backend of the project.

This includes the project project funcionality and api's working.

it consists the 3 models.
1. Vendor
2. Purchase_Order(PO)
3. HistoricalPerformance

and all three models have their own api view and urls and links.

For Base Operations.

first install the requirement.txt file in a virtual enviornment and then makemigrate all the models.
setup a superuser password using pyhon manage.py createsuperuser

After doing all neccessery steps then.

Hit the base url of the project , which hopefully will be 127.0.0.0:8000/api for you, the go through the api's one by one like 
1. /api/vendor/ ----> This api is create api when you can create Vendor
2. /api/vendor/list ----> This api list all the vendor's which resides inside the Vendor model.
3. /api/vendor/<uuid:vendor_code>/ ----- This api retrives the a single vendor details.
4. /api/purchase_orders/ ----> This api creates purchase order's and have Fk of Vendor model.
5. /api/purchase_orders/list -----> This api list all the purchase orders.
6. /api/vendor/<uuid:vendor_code>/performance -----> This api reterives the performance of the vendor , please use uid of the vendor to reterive
7. /api/vendor/performance -----> This api manually creates the performance of the vendor.
8. /api/purchase_orders/<uuid:po_num>/acknowledge -----> this api reterives the purchase order acknowledgement.
9. /api/purchase_orders/<uuid:po_num> -----> This gives you the detail of a single purchase orders object.


IN the Detail api's there is Update and Delete methods is added and required no seperate view.

the Performance Matric are hard coded in the view and also calculated performance in signals.py, all post save method you can find it here 
The Serializers file is in the app itself please find in there, 

Last but not least, i have deployed the app on aws ec2 instance, if you contact me to make it live then i will do it.so you can check.




