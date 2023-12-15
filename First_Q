def extract_digits(string):
    # Find the first digit in the string
    first_digit_index = next((i for i, c in enumerate(string) if c.isdigit()), None)

    # If a digit is found, extract it; otherwise, set it to 0
    first_digit = int(string[first_digit_index]) if first_digit_index is not None else 0

    # Find the last digit in the string
    last_digit_index = next((i for i, c in enumerate(string[::-1]) if c.isdigit()), None)

    # If a digit is found, extract it; otherwise, set it to the first digit
    last_digit = int(string[-last_digit_index - 1]) if last_digit_index is not None else first_digit

    return first_digit, last_digit


def main(file_path):
    # Initialize the sum
    total_sum = 0

    # Open the file and process each line
    with open(file_path, 'r') as file:
        for line in file:
            # Extract digits from the current line
            first_digit, last_digit = extract_digits(line.strip())

            # Concatenate the digits and add to the sum
            concatenated_number = int(str(first_digit) + str(last_digit))

            total_sum += concatenated_number

    # Print the result
    print(f"Sum of concatenated numbers: {total_sum}")


# Replace 'your_file.txt' with the actual path to your file
main('test.txt')
