# To-Do-List-Application
# This a program where you can view, add, remove any task in your task list

tasks = []

while True:
    print("\n To do list Menu" "\n 1. View Task list" "\n 2. Add Task" "\n 3. Remove Task" "\n 4. Exit")
    Choose = input("Choose an Option:").strip()

    if Choose == "1":
        if tasks:
            print("Your tasks:")
            for i, task in enumerate(tasks, 1):
                print(f"{i}. {task}")

        else:
            print("Task list empty.")

    elif Choose == "2":
        task = input("Enter a task:")
        tasks.append(task)
        print(f"{task} has been added to the task list")

    elif Choose == "3":
        task_number = int(input("Enter the task number to remove:"))
        if 0 < task_number <= len(tasks):
            removed_task = tasks.pop(task_number - 1)
            print(f"task '{removed_task}' removed.")

        else:
            print("Invalid task number.")


    elif Choose == "4":
        print("Task list Successfully Exit")

    else:
        print("Invalid Choose Option")
        break
