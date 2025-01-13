# Error Handling Lab: Ask for a filename and handle errors

def handle_file_errors():
    filename = input("Please enter the filename: ")

    try:
        # Try to open the file for reading
        with open(filename, 'r') as file:
            content = file.read()
            print(f"Content of {filename}:\n{content}")

    except FileNotFoundError:
        print(f"Error: The file {filename} does not exist.")
    except IOError:
        print(f"Error: There was an issue reading the file {filename}.")

# Call the function to handle errors
handle_file_errors()
