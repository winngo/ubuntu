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
## ZIP
- Install
  ```
  sudo apt-get install zip
  ```
- Zip file
  ```
  zip filename.zip file-need-to-zip
  ```
- Zip folder
  ```
  zip -r filename.zip foldername-need-to-zip
  ```
## COPY/CUT
- Copy file/folder
  ```
  By using -i for interactive you will be asked if you would like to replace the file:  
  cp -i /home/levan/kdenlive/untitelds.mpg /media/sda3/SkyDrive/  
  or you can use -b to create a backup of your file:  
  cp -b /home/levan/kdenlive/untitelds.mpg /media/sda3/SkyDrive
  Same as the above:  
  cp (-i or -b) /media/sda3/SkyDrive/untitelds.mpg /home/levan/kdenlive
  Use -R for recursive and -i for interactive:  
  cp -Ri ~/MyFolder /sda3/
  ```
- Move file/folder
  ```
  This last one can be done via the mv command, move is like cutting:
  mv -i ~/MyFile ~/OtherFolder/MyFile
  if you want to move a directory, use:  
  mv -Ri ~/MyDirectory ~/OtherDirectory/
  ```
