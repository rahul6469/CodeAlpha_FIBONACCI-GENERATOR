# CodeAlpha_FIBONACCI-GENERATOR
def generate_fibonacci(n):
    fibonacci_sequence = [0, 1]
    for i in range(2, n):
        next_number = fibonacci_sequence[-1] + fibonacci_sequence[-2]
        fibonacci_sequence.append(next_number)
    return fibonacci_sequence

# Get user input for the desired length of the Fibonacci sequence
try:
    n = int(input("Enter the number of Fibonacci numbers to generate: "))
    if n < 0:
        raise ValueError("Please enter a non-negative integer.")

    # Generate and print the Fibonacci sequence
    fibonacci_result = generate_fibonacci(n)
    print(f"Fibonacci sequence for first {n} numbers:", fibonacci_result)

except ValueError as e:
    print(f"Error: {e}. Please enter a valid non-negative integer.")
