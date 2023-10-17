# ubuntu
Note commands when work

## Download from Google Drive
[Reference](https://stackoverflow.com/questions/25010369/wget-curl-large-file-from-google-drive/50670037#50670037)
- Install it with the following command:
```pip install gdown```
- After that, you can download any file from Google Drive by running one of these commands:
```
  gdown https://drive.google.com/uc?id=<file_id>  # for files
  gdown <file_id>                                 # alternative format
  gdown --folder https://drive.google.com/drive/folders/<file_id>  # for folders
  gdown --folder --id <file_id>                                   # this format works for folders too
```
- Example: to download the readme file from this directory

```
gdown https://drive.google.com/uc?id=0B7EVK8r0v71pOXBhSUdJWU1MYUk
```
- The file_id should look something like 0Bz8a_Dbh9QhbNU3SGlFaDg. You can find this ID by right-clicking on the file of interest, and selecting Get link. As of November 2021, this link will be of the form:
```
   # Files
   https://drive.google.com/file/d/<file_id>/view?usp=sharing
   # Folders
   https://drive.google.com/drive/folders/<file_id>
```
```
Caveats
Only works on open access files. ("Anyone who has a link can View")
Cannot download more than 50 files into a single folder.
If you have access to the source file, you can consider using tar/zip to make it a single file to work around this limitation.
```
## UNZIP
- Install
  ```
  sudo apt-get install unzip
  ```
- How to use
  ```
  unzip file.zip -d destination_folder
  ```
- If you want to extract to a directory with the same name as the zip in your current working directory, you can simply do:
  ```
  unzip file.zip
  ```
