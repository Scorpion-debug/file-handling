def modify_content(content):
    return content.upper()

def main():
    input_filename=input("Enter the name of the file to read: ")
    output_filename=input("Enter the name of the file to write to: ")

    try:
        with open("C:\\Users\\HP\\.spyder-py3\\testing.txt", 'r') as input_file:
            content=input_file.read()

            modified_content = modify_content(content)

            with open("C:\\Users\\HP\\.spyder-py3\\Testing1.txt"'w') as output_file:
                output_file.write(modified_content)

            print(f"file has been successfully modified and saved as {output_filename}.")

    except FileNotFoundError:
        print(f"Error: The file '{input_filename}' does not exist.")
    except IOError:
        print(f"Error: There was a problem reading or writing to the file.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")

if __name__ == "__main__":
    main()
