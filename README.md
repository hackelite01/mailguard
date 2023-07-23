
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Stars](https://imailguard.shields.io/github/stars/gr33nm0nk2802/mailMeta?style=flat)
[![Category](https://img.shields.io/badge/Category-OSINT-green.svg)](https://shields.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/gr33nm0nk2802/mailMeta/blob/main/LICENSE)
[![Pull Requests](https://img.shields.io/badge/PullRequests-accepted-green.svg)](https://shields.io/)
[![Py Version](https://img.shields.io/badge/Python-3.8.5-green.svg)](https://shields.io/)

<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This is a forensic tool designed to facilitate the analysis of email headers, streamlining the process of identifying attackers swiftly. 


# Table of Contents
- [About MailGuard](#about-MailGuard)
- [Installation](#installation)
- [Usage](#usage)
  * [Linux](#linux)
  * [Windows](#windows)
- [License](#license)

## About MailGuard

- What is MailGuard?

**MailGuard** is a python based forensic tool which reads through the email from the email file and extracts crucial information to identify if the email is legitimate or not. 

-  What are the advantages of using MailGuard?

Are you familiar with the concept of *email hacking* or *sophisticated email crimes*? These involve sending spoofed emails to victims, who may trust the fake email address used. Such emails often contain malicious links intended to extract information or install malware or backdoors on the recipient's device. To protect users from such threats, we have developed MailGuard.

Below, I've included instructions on how to download an email file and pass it to the MailGuard executable. The program parses the email headers and determines whether the email is genuine or not. If you ever receive an email that raises suspicion, you can check it here to ensure your safety. MailMeta can be a valuable tool in many scenarios. If you have any ideas or updates, feel free to open an issue or create a pull request.
 
 - What are the information revealed by the MailGuard?
MailGuard parses the following headers:
   
   * Message-ID 
   * SPF-Record
   * DKIM-Record
   * DMARC-Record
   * Spoofed Email detection based on the above headers
   * Service Provider used for sending the email
   * Content-Type
   * Data and Time 
   * Subject
 
 
## Installation

You have two methods to use MailGuard. Either you can download the github repo and run the mailguard.py file from the command line. Make sure you have all requirements installed in this case like python3. You may also run the standalone binaries. This is for those who have very little technical knowledge.

<br>
1. Clone the repository

  ```(bash)
    git clone https://github.com/hackelite01/mailguard
  ```

2.  Running from the mailguard.py file

  ```(bash)
    cd mailguard
    python3 mailguard.py
  ```
<br>

Additionally you can directly download the executable from the [Releases](https://github.com/hackelite01/mailguard/releases/tag/1.0.0) and use them.
<br>

## Usage
<br>

Either you are on windows or linux first download the original metadata of the email using the **show original** / **view raw** / **download original** option. 

Then we pass the `eml` file to the executable.
<br>


### Linux

1. Use `mailguard.py` from the cloned repo. (Python is required)

```
python3 mailguard.py -f message.eml
```

or

2. Downloading the `MailGuard` executable for linux and giving it executable permissions. Then supplying the eml file to the pre-compiled binary. (No dependencies)

```
wget https://github.com/hackelite01/mailguard/releases/download/1.0.0/meta
chmod +x mailguard
mailguard -f message.eml
```
<br>


### Windows

1. Executing the precompiled binaries downloaded from the releases page. (No dependencies needed)

```
mailguard.exe -f .\message.eml
```


<br>

or

2. Running from the repository clonned (Python Required)

```
python3 mailguard.py -f message.eml
```



## License

This project is licensed under the [MIT license](https://github.com/hackelite01/mailguard/blob/main/LICENSE).
