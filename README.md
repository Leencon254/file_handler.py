# file_handler.py

def read_and_modify_file(input_filename, output_filename):
    try:
        # Open the input file for reading
        with open(input_filename, 'r') as infile:
            content = infile.read()
        
        # Modify content: convert text to uppercase (you can choose other modifications)
        modified_content = content.upper()

        # Write modified content to new file
        with open(output_filename, 'w') as outfile:
            outfile.write(modified_content)

        print(f"File '{input_filename}' was read and modified content saved to '{output_filename}'.")
    
    except FileNotFoundError:
        print(f"Error: The file '{input_filename}' does not exist.")
    
    except Exception as e:
        print(f"An unexpected error occurred: {e}")


# Ask user for filenames
input_file = input("Enter the name of the file to read from: ")
output_file = input("Enter the name of the new file to write to: ")

# Call the function
read_and_modify_file(input_file, output_file)
