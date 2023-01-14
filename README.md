# ChatGPT Powered

--- Write to ChatGPT ---> Write me a python code for search for doc, pdf, jpg, png and gifs and copy them to temp folder in windows if found.

If you want you can add ftp or mail transfer.

```python

import os
import shutil

# Specify the directory to search in
search_dir = "C:\\example\\directory"

# Specify the temp folder to copy the files to
temp_folder = "C:\\temp"

# List of file extensions to search for
extensions = [".doc", ".pdf", ".jpg", ".png", ".gif"]

# Search for files with the specified extensions in the search directory
for root, dirs, files in os.walk(search_dir):
    for file in files:
        if any(file.endswith(ext) for ext in extensions):
            # Construct the full file path
            file_path = os.path.join(root, file)
            # Copy the file to the temp folder
            shutil.copy2(file_path, temp_folder)

```
