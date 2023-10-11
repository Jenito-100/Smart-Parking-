# Smart-Parking-

Create a Vehicle Parking Management Project in Python
 PRANJAL DEV  JUNE 5, 2022
Create a Vehicle Parking Management in PythonIntroduction
Hello friends, welcome to copyassignment.com. In this tutorial, we are going to Create a Vehicle Parking Management in Python. This project helps maintain the details of the vehicle owner, number, type, date, and the amount of time the vehicle is parked in the area. Accordingly, the bill generates for the particular vehicle parked in the area. This information is useful for all those who want to maintain a database of the individual who has parked their vehicles in the surroundings.

We are providing the complete code and detailed information about this project in this article.

Let us understand this project

1. Import Function and Initializing the variables

#Import Time
import time

Vehicle_Number=['XXXX-XX-XXXX']
Vehicle_Type=['Bike']
vehicle_Name=['Intruder']
Owner_Name=['Unknown']
Date=['22-22-3636']
Time=['22:22:22']
bikes=100
cars=250
bicycles=78
In this code block, we are importing the time module to implement its methods and function in the project. We have initialized the variables vehicle number, vehicle type, vehicle name, owner name date, and time to some default value. As well as bikes, cars, and bicycles with some initial value.

2. Create a while loop block to display the options in Vehicle Parking Management Project
def main():
    global bikes,cars,bicycles
    try:
        while True:
            print("-----------------------------------------------------")
            print("\t\tParking Management System")
            print("-------------------------------------------------------")
            print("1.Vehicle Entry")
            print("2.Remove Entry" )
            print("3.View Parked Vehicle ")
            print("4.View Left Parking Space ")
            print("5.Amount Details ")
            print("6.Bill")
            print("7.Close Programme ")
            print("+---------------------------------------------+")
            ch=int(input("\tSelect option:"))
In this code block, we have initialized the bikes, cars, and bicycles as global variables. They are accessible through the entire main block. Here we are providing the options to choose the service options from the list, for the vehicle parking management system.

Now we will understand each service option in detail.

Code for vehicle number entry
if ch==1:
    no=True
    while no==True:
        Vno=input("\tEnter vehicle number (XXXX-XX-XXXX) - ").upper()
        if Vno=="":
            print("###### Enter Vehicle No. ######")
        elif Vno in Vehicle_Number:
            print("###### Vehicle Number Already Exists")
        elif len(Vno)==12:
            no=not True
            Vehicle_Number.append(Vno)
        else:
            print("###### Enter Valid Vehicle Number ######")
Ch is for choice, Once we select the ch option as 1 which is for vehicle entry number, then we provide the while loop. while the number(no is True). We will store the vehicle number in Vno. If the vno is empty i.e vno==“”.The user asks to enter the vehicle number, else If the vno entered is already present in the vehicle number then it prints the vehicle number already exists. Else if len(vno)==12, It will ask to append the info to the vehicle number variable.

Code to enter the vehicle type
typee=True
while typee==True:
    Vtype=str(input("\tEnter vehicle type(Bicycle=A/Bike=B/Car=C):")).lower()
    if Vtype=="":
        print("###### Enter Vehicle Type ######")
    elif Vtype=="a":
        Vehicle_Type.append("Bicycle")
        bicycles-=1
        typee=not True
    elif Vtype=="b":
        Vehicle_Type.append("Bike")
        bikes-=1
        typee=not True
    elif Vtype=="c":
        Vehicle_Type.append("Car")
        cars-=1
        typee=not True
    else:
        print("###### Please Enter Valid Option ######")
Here we have to initialize the typee variable to true. While the condition is True, the system asks to enter the vehicle type i.e a,b, or c which will accept the input in the lower case. Here A is for bicycle, B is for Bike and C is for Car. Any vehicle type you enter is stored in the variable Vtype. If the Vtype==””(empty). It will ask to enter the vehicle type.  According to the type of variable you enter the vehicle type will be stored in the variable and typee variable is set to not True.

Code to enter the vehicle name
name=True
while name==True:
    vname=input("\tEnter vehicle name - ")
    if vname=="":
        print("########Please Enter Vehicle Name ########")
    else:
        vehicle_Name.append(vname)
        name=not True
Here we have set the name== True. While the name == True i.e until we enter the name.vname store the value i.e. vehicle name.  if the vname is empty system asks to enter the vehicle name, else it will store the name using the append function to the vehicle name variable The name variable is initialized to not True.

Code to enter the owners name
o=True
while o==True:
    OName=input("\tEnter owner name - ")
    if OName=="":
        print("###### Please Enter Owner Name ######")
    else:
        Owner_Name.append(OName)
        o=not True
O is initialized to True. While the condition satisfies the Owner’s name is stored in the OName variable. If the OName is empty it system asks to enter the owner name else it will store the Owner name in the owner name variable. O is now initialized to Not True.

Code enter the date and time
d=True
while d==True:
    date=input("\tEnter Date (DD-MM-YYYY) - ")
    if date=="":
        print("###### Enter Date ######")
    elif len(date)!=10:
        print("###### Enter Valid Date ######")
    else:
        Date.append(date)
        d=not True
t=True
while t==True:
    time=input("\tEnter Time (HH:MM:SS) - ")
    if t=="":
        print("###### Enter Time ######")
    elif len(time)!=8:
        print("###### Please Enter Valid Time ######")
    else:
        Time.append(time)
        t=not True
print("\n............................................................Record")
Similarly, we have to create a while loop to enter the date and time initializing d and t to 0. Date variable stores the date and the time-variable stores time. The date and time variable checks the condition and accordingly execute further.


Code to remove the entry from the register
elif ch==2:
    no=True
    while no==True:
        Vno=input("\tEnter vehicle number to Delete(XXXX-XX-XXXX) - ").upper()
        if Vno=="":
            print("###### Enter Vehicle No. ######")
        elif len(Vno)==12:
            if Vno in Vehicle_Number:
                i=Vehicle_Number.index(Vno)
                Vehicle_Number.pop(i)
                Vehicle_Type.pop(i)
                vehicle_Name.pop(i)
                Owner_Name.pop(i)
                Date.pop(i)
                Time.pop(i)
                no=not True
                print("\n............................................................Removed Sucessfully..................................................................")
            elif Vno not in Vehicle_Number:
                print("###### No Such Entry ######")
            else:
                print("Error")
        else:
            print("###### Enter Valid Vehicle Number ######")
