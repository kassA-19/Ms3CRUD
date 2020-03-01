CRUD
#path to xml file: /Ms3CRUD/ms3crud/src/main/mule/m3input.xm

# # This API has four Specification 

#The First Specification is to Create a Customer using a post Method
#The customer will be providing the necessary details and it will be inserted into the database.
#The Method has to be post and the Body should contain the json file and has to be send to the path /customerCreate
#SQL statement: insert into ms3.Customer values (:ID, :FirstName, :LastName, :DOB, :Gender, :Title, :AddressType, :AddressNumber, :Street, :Unit, :City, :State, :ZipCode, :Email, :PhoneNumber)

#the second specification is to read customer information using a get method. 
#the customer will be specifying an ID and depending on the ID the necessary  details will be fetched for the customer. We use /GetCustomer path to perform this method
#SQL statement: SELECT * FROM ms3.Customer where ID=:id

#the third specification is to update a customer here we used (id) as A primary key :- 
      The customer ID will be specified using Uri-parameters 
      i have used input parametere  to update the customer information.  
#the customer ID will be specified for which the update need to be perform along with that the Field name and the corresponding value will be specified the update will be perform the customer ID.
#the path we use to specify /UpdatingCustomer
SQL statement: UPDATE ms3.Customer SET DOB =:DOB, FirstName =:FirstName, AddressType =:AddressType, HomeNumber =:HomeNumber, Street =:Street, City =:City, State =:State, Zipcode =:Zipcode, Email =:Email, PhoneNumber =:PhoneNumber, Unit =:Unit, LastName =:LastName, Title =:Title, Gender =:Gender
WHERE ID =:id

#the final specification is to Delete a customer from database. For this we use a path /CustomerDelete
#the customer id will be specified using qureyParameter and the entire customer information will be deleted from the database.
#SQL statement: DELETE FROM ms3.Customer WHERE ID=:id
