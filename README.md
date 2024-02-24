# FIle Downloader
## Features 
 
- Download File
- Generate OneDrive DirectURL
- Generate GoogleDrive DirectURL


## Example
```csharp
var url = new URL("FILE URL");
string URL;
string filename;
//google drive
URL = url.GetGDriveDirectLink();
//other way
URL = url.GetGDriveDirectLink2();
//onedrive
URL = url.GetODriveDirectLink();

//google drive file name
filename = @$"file_path\{url.GetGDriveFileName()}";
//onedrive file name (manual)
filename = @$"file_path\test.txt";
//download
FileDownloader httpClient = new(URL, filename);
httpClient.ProgressChanged += (totalFileSize, totalBytesDownloaded, progressPercentage) => Console.WriteLine($"{progressPercentage}%");
await httpClient.StartDownload();
``` 
