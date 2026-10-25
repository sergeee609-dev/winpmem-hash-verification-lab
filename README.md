# WinPmem Preparation and Hash Verification Lab

## Project Overview
This project documents a digital forensics lab focused on preparing the WinPmem memory acquisition utility and verifying the integrity of its executable using SHA-256 hashing. Completed as part of digital forensics coursework, the lab demonstrates command-line navigation, file preparation, and consistent hash calculation across Windows Command Prompt and PowerShell.

## Tools and Technologies
- WinPmem
- Windows Command Prompt
- Windows PowerShell
- CertUtil
- Get-FileHash
- SHA-256

## Lab Workflow

### 1. Download and Extract WinPmem
Downloaded the instructor-provided WinPmem archive and extracted its contents into a working directory.

### 2. Prepare the Working Directory
Organized the files under a dedicated directory and used an elevated Command Prompt to navigate to the extracted files.

### 3. Calculate SHA-256 with Command Prompt
Used the Windows CertUtil utility to calculate the SHA-256 hash of the WinPmem executable.

```cmd
certutil -hashfile "C:\Evidence\winpmem\winpmem_mini_x64_rc2.exe" SHA256
```

### 4. Calculate SHA-256 with PowerShell
Used PowerShell's Get-FileHash cmdlet to independently calculate the SHA-256 hash of the same executable.

```powershell
Get-FileHash "C:\Evidence\winpmem\winpmem_mini_x64_rc2.exe" -Algorithm SHA256
```

### 5. Compare Hash Results
Compared the outputs from both utilities and confirmed that the SHA-256 values matched for the selected executable.

## Skills Demonstrated
- Preparing forensic acquisition utilities
- Navigating directories through the Windows command line
- Calculating SHA-256 file hashes
- Using CertUtil and Get-FileHash
- Comparing hash outputs for consistency
- Documenting forensic preparation workflows

## Project Documentation
[View the WinPmem Lab Portfolio (PDF)](WinPmem_Preparation_Hash_Verification_Portfolio.pdf)

## Project Scope
This educational lab demonstrates WinPmem preparation and hash calculation of an executable. It does not document an actual RAM acquisition, analysis of a memory dump, or verification against a separately trusted reference hash.
