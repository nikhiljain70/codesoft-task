def calculator():
    # Prompt the user to enter two numbers
    num1 = float(input("Enter the first number: "))
    num2 = float(input("Enter the second number: "))

    # Display available operations
    print("Select operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")

    # Prompt the user to choose an operation
    operation = input("Enter the operation (1/2/3/4): ")

    # Perform the operation based on the user's choice
    if operation == '1':
        result = num1 + num2
        operation_sign = "+"
    elif operation == '2':
        result = num1 - num2
        operation_sign = "-"
    elif operation == '3':
        result = num1 * num2
        operation_sign = "*"
    elif operation == '4':
        # Handle division by zero
        if num2 == 0:
            return "Error: Division by zero is not allowed."
        result = num1 / num2
        operation_sign = "/"
    else:
        return "Invalid operation choice."

    # Display the result
    return f"{num1} {operation_sign} {num2} = {result}"

# Call the calculator function
print(calculator())
