## EX - 6  Metadata extraction using tools like exiftool, timeline analysis with log2timeline, searching for hidden data using steganography tools

## AIM :
To Metadata extraction using tools like exiftool, timeline analysis with log2timeline, searching for hidden data using steganography tools
## DESIGN STEPS:
### Step 1:
Use exiftool to extract metadata from files such as images, documents, and videos.

### Step 2:
Use log2timeline and plaso to create and analyze event timelines from system logs and file metadata.

### Step 3:
Apply steganography detection tools like steghide, zsteg, or binwalk to uncover hidden data in media files.




# A. Using ExifTool – for file metadata

 Install:
```
sudo apt update
sudo apt install exiftool -y
```
 Extract metadata from a file:
```
exiftool image.jpg
```
 Batch process a folder:
```
exiftool -r /path/to/folder
```
 # Useful flags:

-G: Show metadata group

-time:all: Show only timestamps

-GPSLatitude -GPSLongitude: Extract GPS data

![image](https://github.com/user-attachments/assets/75dc64ee-7af7-4765-9ecf-0ee8eafec4af)

# install log2timeline
```
sudo apt install plaso -y
```
```
sudo apt install steghide -y
```
# Embed data
```
steghide embed -cf /home/kali/Downloads/wallpaper.jpg -ef /home/kali/Downloads/secret.txt
```
<img width="1422" height="249" alt="embed 2" src="https://github.com/user-attachments/assets/4bed1f96-9f5f-41d5-91f7-2126b0c337af" />



Extract hidden data:
```
steghide extract -sf hidden.jpg
```
<img width="1920" height="375" alt="extracted 3" src="https://github.com/user-attachments/assets/56aafc98-2e5b-40a5-a066-751e87184223" />


# Using binwalk – for file analysis

```
sudo apt install binwalk -y
binwalk suspicious.jpg
```
<img width="1572" height="472" alt="binwalk 4" src="https://github.com/user-attachments/assets/3d14b0c2-b01e-4241-9159-147d1b892735" />



## RESULT:
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.

