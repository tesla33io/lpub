
# `lpub` - File Sharing Server

This Python script provides a convenient way to share a single file over your local network. It creates a simple HTTP server that serves the specified file to any device on the same network.

## Dependencies

This script needs a package `qrencode` ([link](https://fukuchi.org/works/qrencode/)) installed on your system to be able to display qr-code.

## Features

* Share a single file at a time.
* Displays the file URL and QR code (optional) for easy access on mobile devices.
* Shows transfer progress during the file download.

## Usage

```
python3 lpub <file_path> [port] [-qr] [-url]
```

**Arguments:**

* `<file_path>`: The path to the file you want to share.
* `[port]`: (Optional) The port number on which the server will listen. Defaults to 8000.
* `[-qr]`: (Optional) Display only the QR code for the file URL.
* `[-url]`: (Optional) Display only the file URL.

**Example:**

```
python3 lpub /path/to/your/file.txt
```

This will share the file `file.txt` located at `/path/to/your/file.txt` on port 8000 and display both the URL and QR code for accessing it.

## Download

### Linux/MacOS

You can download this script on your machine with the following command:

```wget
wget "https://raw.githubusercontent.com/tesla33io/lpub/refs/heads/main/lpub"
```

## Notes

* **Important:** This script does not implement any user authentication. It's intended for trusted local networks to share files securely. Avoid using it on public or untrusted networks.
* This script is designed for sharing files within a local network. The server will not be accessible from the internet.
* Make sure the file you want to share exists and you have permission to read it.
* This script has been tested on Linux. If you encounter issues on other operating systems, please raise an issue.
