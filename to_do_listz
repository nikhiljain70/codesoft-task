class ToDoList:
    def __init__(self):
        self.tasks = []

    def add_task(self, task):
        """Add a new task to the list."""
        self.tasks.append({"task": task, "completed": False})

    def view_tasks(self):
        """Display all tasks."""
        if not self.tasks:
            print("No tasks in your to-do list.")
        else:
            for index, task in enumerate(self.tasks, start=1):
                status = "✓" if task["completed"] else "✗"
                print(f"{index}. {task['task']} [{status}]")

    def mark_completed(self, task_number):
        """Mark a task as completed."""
        try:
            self.tasks[task_number - 1]["completed"] = True
        except IndexError:
            print("Invalid task number.")

    def delete_task(self, task_number):
        """Delete a task from the list."""
        try:
            self.tasks.pop(task_number - 1)
        except IndexError:
            print("Invalid task number.")

def main():
    todo_list = ToDoList()

    while True:
        print("\nTo-Do List Application")
        print("1. Add a task")
        print("2. View tasks")
        print("3. Mark a task as completed")
        print("4. Delete a task")
        print("5. Exit")
        choice = input("Enter your choice: ")

        if choice == '1':
            task = input("Enter the task: ")
            todo_list.add_task(task)
        elif choice == '2':
            todo_list.view_tasks()
        elif choice == '3':
            task_number = int(input("Enter the task number to mark as completed: "))
            todo_list.mark_completed(task_number)
        elif choice == '4':
            task_number = int(input("Enter the task number to delete: "))
            todo_list.delete_task(task_number)
        elif choice == '5':
            print("Exiting the application. Have a great day!")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
