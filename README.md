# Download videos from the web using PowerShell

This PowerShell script is designed to download a youtube video from a URL on the clipboard and save it to the downloads folder (``%downloads%``). 

Here is a step-by-step description of how the script works:


1. First, the script determines the path to the downloads folder (%downloads%) using the Windows registry.

2. Then it tries to retrieve the URL from the clipboard.

3. If the URL was found, it calls the `yt-dlp.exe` utility (an alternative to youtube-dl) to download the video from the specified URL. The `-f "b"` option specifies that only a ladder list of the best formats should be downloaded. The `--autonumber-size 3` option specifies the number of digits for automatic file numbering. The `-P` option specifies the path to save the files. The `-o` option specifies the format of the file name to be saved.

4. After the download completes, the script checks the yt-dlp completion code. If the code is not 0, the script waits for the Enter key to be pressed.

5. If the download is successful, the script displays a completion message in the console.

6. Finally, the script clears the clipboard.

For the script to work correctly, you must make sure that you have yt-dlp and ffmpeg installed, and they are either in the same folder as the script or added to the PATH environment variable.

To add a description of how the script works to the README.md file on GitHub, you can create the following section:

## Instructions

1. Make sure you have yt-dlp and ffmpeg installed on your computer. You can download them from the official websites:

   - [yt-dlp Builds](https://github.com/yt-dlp/yt-dlp/releases)
   - [ffmpeg Builds](https://github.com/yt-dlp/FFmpeg-Builds/releases)

2. Copy the contents of the [yt-dlp.ps1](yt-dlp.ps1) file to your computer.

3. Run the script as follows:

```powershell
   ./download-video.ps1
```
4. The script will check the clipboard for a URL. If the URL is found, the script will download the video and save it to the downloads folder (``%downloads%``).


