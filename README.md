**COMPANY**: CODTECH IT SOLUTIONS
**NAME**: SHRAVANI ACHAL HENDRE
**INTERN ID**: CT08DTU
**DOMAIN**: CYBERSECURITY AND ETHICAL HACKING
**BATCH DURATION**: 25th Dec to 25th Jan
**MENTOR NAME**: NEELA SANTOSH

**Overview of the Project:**
The tool performs the following tasks:

1. Hash Calculation:  
It calculates the cryptographic hash (e.g., SHA-256) of each file in the given directory. This hash is used as a unique fingerprint for the file, allowing comparison over time to detect any changes.
It processes files in chunks of 8192 bytes to optimize memory usage, especially for large files.

2. Create/Update Hash Record:  
The tool generates a record of all files in a directory (and its subdirectories), along with their calculated hashes.
This record is stored in a JSON file (file_hashes.json), which serves as a reference for future integrity checks.

3. Check File Integrity:
The tool compares the current file hashes with those stored in the hash record to detect changes.

It checks for the following conditions:
- File Removed: If a file listed in the hash record no longer exists, it is flagged as removed.
- File Changed: If the current hash of a file differs from the recorded hash, it is flagged as modified.
- New File Detected: If a new file appears in the directory, it is flagged as a new addition. If no changes are detected, a message is shown indicating the files are intact.

Command-Line Interaction:
The program provides two main actions through user input:
1. Create Hash Records: Used to generate or update the hash record for all files in the monitored directory.
2. Check File Integrity: Used to compare current files with the recorded hashes and report any discrepancies.

Key Components:
- Hash Algorithm: SHA-256 (default) is used to generate the hash values for files, but other hash algorithms can be specified.
- JSON Storage: File hashes and paths are saved in a JSON format, making it easy to manage and update records.
- Directory Monitoring: It works on any directory (specified by the user) and includes subdirectories.

Example Usage:
- Create Hash Record:
- Run the tool with action "1" to create the initial hash record for a specified directory.
- Check Integrity:
- Run the tool with action "2" to verify the integrity of files by comparing their current hashes to the ones stored in the JSON record.

Use Case:
Ideal for security monitoring, backup validation, and ensuring that important files have not been tampered with.
