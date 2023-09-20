# FIle Downloader
## Features 
 
- Download File
- Generate OneDrive DirectURL
- Generate GoogleDrive DirectURL


## Example
```csharp
string url = "link";
string file_name = @"file_path";
//google drive
url = FileDownloader.GetGDriveDirectLink(url);

//onedrive
url = FileDownloader.GetODriveDirectLink(url);

//download
FileDownloader httpClient = new(url, file_name);
httpClient.ProgressChanged += (totalFileSize, totalBytesDownloaded, progressPercentage) => Console.WriteLine($"{progressPercentage}%");
await httpClient.StartDownload();
``` 
