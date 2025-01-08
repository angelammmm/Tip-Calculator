# Tip-Calculator

### Summary
In Python, the `if-else` statement is a powerful control structure that allows you to create decision-making logic in your program. It helps check whether certain conditions are met and then directs the flow of the program accordingly. This is particularly useful when you need to validate or process user input, as it allows the program to react differently based on specific criteria. If the conditions meet the specified requirements, the program proceeds with the next step. If not, it can take an alternative action, ensuring that your program handles different cases effectively and flexibly.

### Use Case
Imagine your company works with several different file formats, and many of your coworkers are unsure about which format certain files should be saved in. Your manager asks you to create a simple Python program that can help solve this problem. The program should prompt the user to input a file name, and then it should identify the correct format (such as `.jpg`, `.png`, `.pdf`, etc.) and output the appropriate MIME type for that file.

This is where the `if-else` statement becomes crucial. It allows the program to evaluate the file extension provided by the user and, based on that, provide an appropriate MIME type for the file. By using multiple conditions (`if`, `elif`, `else`), we can ensure that the program correctly handles a variety of file types and reacts accordingly. If the file extension matches one of the specified cases, it will print the corresponding MIME type; if it doesn’t match any of the defined cases, it will fall through to the `else` block, where we can handle invalid or unexpected file formats.

For example:

```python
filename = input("File name:")
new_filename = filename.lower()
#gif
if '.gif' in new_filename:
    print("image/gif")
#jpg
elif '.jpg' in new_filename:
    print ("image/jpeg")
#jpeg
elif '.jpeg' in new_filename:
    print("image/jpeg")
#png
elif '.png' in new_filename:
    print("image/png")
#pdf
elif '.pdf' in new_filename:
    print("application/pdf")
#text
elif '.txt' in new_filename:
    print("text/plain")
#zip
elif '.zip' in new_filename:
    print("application/zip")
#otherwise
else:
    print("application/octet-stream")
```

### Why the `if-else` Statement is Useful in This Example

1. **Flexible Input Handling**: The `if-else` statements enable the program to handle a wide variety of file types based on user input. Each `if` or `elif` statement checks for a specific file extension and maps it to a MIME type. This makes the program flexible enough to support different file formats without requiring complex logic.

2. **Conditional Execution**: With `if-else`, the program can make decisions on what to do next based on the file extension. For instance, if the file ends with `.jpg`, it will output `"image/jpeg"`, and the user can move on to their next task. If the input doesn't match any of the specified file extensions, the `else` statement provides a default action, letting the user know that the file format is unknown.

3. **Clear Decision Structure**: The structure of `if-else` ensures that only one block of code runs, making the program easier to read and understand. The flow is clear: check the file extension, and print the appropriate MIME type, or handle unknown extensions gracefully.

4. **Prevents Errors and Enhances User Experience**: Without the `else` statement, the program might fail to inform users when an unsupported file type is entered. The `else` block captures this scenario, preventing errors or confusion, and provides feedback to the user that their input is invalid.

5. **Scalability**: As new file types need to be supported in the future, the logic in the `if-else` block can be easily expanded by adding new `elif` conditions. For example, if the company starts using `.docx` files, you can simply add another `elif` clause to handle that case.

In summary, the `if-else` statement in this example is a critical part of the logic that ensures the program reacts to user input appropriately, handles different scenarios, and provides meaningful output based on the file type provided by the user.
