# How to use rclone to transfer from Google Drive to Dropbox

## For Google drive/google services 
1. Create a gcloud project. You may have to add a credit card if you have never used Google Cloud Platform before, but it doesn't charge to your card.
2. Activate Google Drive API in API Library
3. Create OAuth Consent in credentials, store credentials and secret
4. Publish App

## rclone setup
5. Download and unpack rclone
6. Use rclone config in command line.
7. Set up remotes for google drive and Dropbox. Dropbox no need credentials
8. Exit config, use command line

### Example command line arguments

```
.\rclone.exe copy [gdrive remote]:[shared folder] [dropbox remote]:[shared folder]
//
.\rclone.exe copy --drive-shared-with-me --dropbox-batch-mode async gdrive:"Software Testing Mini Campaign/" dropbox:Folder/
```
You can remove the tags if you're not using shared folders on google drive, and not uploading large numbers/large files onto dropbox
## FAQ
Q: Free?
A: rclone is free. Google Drive API calls and gcloud project should be free. Dropbox is free (but paid larger storage plans are not). As far as I can tell, this method directly pipes the files to your new storage provider, preserving Modified Date etc. without storing on your local drive. It consumes network bandwidth though, so get a good connection (not free).

## Further links/Acknowledgements

https://forum.rclone.org/t/using-spaces-in-folder-name/16650
https://www.prashantkhurana.com/blog/rclone-copy-drive-dropbox/
https://rclone.org/drive/
https://rclone.org/dropbox/
https://forum.rclone.org/t/fatal-error-failed-to-mount-fuse/22119
https://rclone.org/commands/rclone_mount/#installing-on-windows
https://rclone.org/downloads/
