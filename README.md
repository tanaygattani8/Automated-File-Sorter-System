Of course. Here is a professional `README.md` file for your Automated File Sorter project, based on the `main.py` script provided.

-----

# Automated File Sorter System

This project is a simple yet powerful Python script that automatically organizes files in a specified directory. It scans a folder and moves files into subdirectories based on their file extension, helping to keep your directories clean and tidy.

## ✨ Features

  * **Automatic Organization**: Sorts files into designated folders based on their type (e.g., `.csv`, `.jpg`, `.txt`).
  * **Folder Creation**: Automatically creates necessary subdirectories if they don't already exist.
  * **Lightweight**: Built with only standard Python libraries, requiring no external dependencies.
  * **Easily Customizable**: Simple to extend and add new rules for different file types.

## 🛠️ Requirements

  * Python 3.x
  * No external packages are needed. The script uses the built-in `os` and `shutil` libraries.

## 🚀 Setup and Usage

Follow these steps to get the file sorter working on your machine.


The script will execute, create the necessary folders (`csv files`, `image files`, `text files`), and move the corresponding files.

## 🔧 Customization

You can easily customize the script to handle more file types.

For example, to add a rule for sorting PDF files into a "pdf files" folder:

1.  **Add the new folder name** to the `folder_names` list in `main.py`:
    ```python
    folder_names = ['csv files', 'image files', 'text files', 'pdf files']
    ```
2.  **Add a new `elif` condition** to the loop that handles file moving:
    ```python
    for file in file_name:
        if ".csv" in file and not os.path.exists(path + "csv files/" + file):
            shutil.move(path + file, path + "csv files/" + file)
        elif ".jpg" in file and not os.path.exists(path + "image files/" + file):
            shutil.move(path + file, path + "image files/" + file)
        elif ".txt" in file and not os.path.exists(path + "text files/" + file):
            shutil.move(path + file, path + "text files/" + file)
        # Add this new condition
        elif ".pdf" in file and not os.path.exists(path + "pdf files/" + file):
            shutil.move(path + file, path + "pdf files/" + file)
    ```

## 🤝 Contributing

Contributions are welcome\! If you have ideas for improvements or have found a bug, please open an issue or submit a pull request.
