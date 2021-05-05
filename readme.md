# File Manager for AWS S3
## Features:
* Manage file / folder easily via AWS S3

**Initiatization is required when app starts. Here is an example.**

```
FileManager.initialize("YOUR_AWS_REGION", "YOUR_S3_BUCKET_NAME", "STARTING_ROOT_FOLDER_NAME");
```

**Examples:**
```
// Get file or folder object
await FileManager.read("YOUR_FOLDER_OR_FILE_OBJECT_KEY");

// List all objects under a folder
await FileManager.list("YOUR_FOLDER_OBJECT_KEY");

// Count no. of objects under a folder
await FileManager.count("YOUR_FOLDER_OBJECT_KEY");

// Create folder with specific ACL
await FileManager.createFolder("YOUR_FOLDER_OBJECT_KEY", "public-read");

// Create file with default ACL
await FileManager.createFolder("YOUR_FILE_OBJECT_KEY", bufferData);

// Delete empty folder
await FileManager.deleteFolder("YOUR_FOLDER_OBJECT_KEY");

// Delete file
await FileManager.deleteFile("YOUR_FILE_OBJECT_KEY");

```