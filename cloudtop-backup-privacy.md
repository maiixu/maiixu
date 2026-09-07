# CloudTop Backup

CloudTop Backup is a personal backup client operated by Mai Xu for his own Google account. It uses restic and rclone on his own computers to store encrypted backup snapshots in Google Drive. It is not a service offered to other users.

## Google Drive access

The client requests the `drive.file` scope. It can create and manage the files it creates, rather than requesting access to every existing Drive file. Backup contents and filenames inside the restic repository are encrypted on the computer before upload. Google Drive stores the encrypted repository.

## Data handling

The client does not sell backup data, provide it to advertisers, or use it to train models. It does not send backup contents to the restic or rclone projects. Google processes the stored repository under the account holder's existing Google agreement.

OAuth credentials and the working encryption key stay on the owner's computers. A recovery copy of the encryption key is kept in the owner's Bitwarden vault, separately from Google Drive. Private filenames, account records and credentials are not published in this document.

## Retention and access

Snapshots remain until the owner deliberately removes them. The client does not automatically prune snapshots. The owner can revoke the client in Google Account permissions to stop access; revocation does not itself remove existing encrypted backup files. The owner can remove the repository through Google Drive.

## Contact

Owner: [Mai Xu](https://github.com/maiixu). This client is for the owner's personal use only.

