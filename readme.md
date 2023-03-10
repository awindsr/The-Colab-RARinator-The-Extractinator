# The Colab RARinator: The Extractinator

This Python script is designed to extract RAR files that are split into multiple parts. It uses the `rarfile` module to open and extract the RAR files, and `os` module to work with the file system. It is intended to be used on Google Colab to access RAR files from Google Drive and save the extracted files back to Google Drive.

## Getting Started

### Prerequisites

This script requires the following modules to be installed:

* `rarfile`

You can install the `rarfile` module using the following command:

!pip install rarfile


### Setup

To use this script, you need to mount your Google Drive and set the following variables:

* `dir_path`: The directory path containing the subfolders with the splitted RAR files in Google Drive.
* `extract_dir`: The path of the directory where the extracted files will be saved in Google Drive.
* `password`: The password for the password-protected RAR files.

## Usage

To use this script, simply run it on Google Colab. It will automatically extract all RAR files that are split into multiple parts in the specified directory and save the extracted files to the specified extract directory.

The script will keep running until all RAR files have been extracted. During each loop iteration, it checks all subfolders in the directory and all RAR files in each subfolder. If a RAR file with a filename ending in `.part1.rar` or `.part01.rar` is found, it extracts all files to a folder with the same name as the subfolder in the extract directory.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

This script was inspired by a Geeks for Geeks article on [How to Extract Multiple RAR Files at Once in Python](https://www.geeksforgeeks.org/how-to-extract-multiple-rar-files-at-once-using-python/).
