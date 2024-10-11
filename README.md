# To-Do-List-application
# CREATING TO-DO-LIST APPLICATIONS.
def task():
    tasks = []
    print ("______WELLCOME TO THE TO-DO-LIST APPLICATIONS______ :")
    total_task = int (input ("How many task you want to add = "))
    for i in range (1,total_task+1 ):
        task_name= input (f"enter task{i} =")
        tasks.append(task_name)
    print (f"Today task are \n{task}")
    while True:
        operation= int (input ("Enter 1-add\n2-update\n3-delete\n4-view\n5-exit/stop"))
        if operation==1:
            add= input ("Enter task you want to add =")
            tasks.append(add)
            print (f"task{add} has been successfull added.....")
        elif operation==2:
            updated_val= input ("Enter the task name you want to update =")
            if updated_val in tasks:
                up= input ("Enter new task=")
                ind= tasks.index(updated_val)
                tasks[ind]= up
                print (f"updated the task {task} ")
        elif operation ==3:
            del_val= input ("Which task do you want to delete =")
            if del_val in tasks:
                del tasks[ind]
                print (f"Task{del_val}has been deleted.....")
        elif operation==4:
            print (f"Total task ={tasks}")
        elif operation==5:
            print ("Closing the program.....")
            break
        else:
            print ("Invalid Input, Enter 1 to 5 any numbers")
task()
