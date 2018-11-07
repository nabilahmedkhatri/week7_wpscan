# Project 7 - WordPress Pentesting

Time spent: **4** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Cross Site Scripting Through Comments
  - [X] Summary:
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [X] GIF Walkthrough: <img src="https://i.imgur.com/jzk6YuU.gif">
  - [X] Steps to recreate:
    - Make a comment post with the following text <script>alert('XSS')</script>
    - Post Comment
    - Script runs when the page is loaded
  - [X] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/branches/4.2/src/wp-includes/comment.php?rev=3230)
1. (Required) Getting Usernames from the Login Page
  - [X] Summary: Finding valid usernames from brute-forcing the login page
    - Vulnerability types: User enumeration
    - Tested in version: 4.2  
    - Fixed in version: 4.2.9
  - [X] GIF Walkthrough: <img src="https://i.imgur.com/ySxjBlw.gif"></img>
  - [X] Steps to recreate:
    - Guess usernames in login field and enter wrong password
    - When username is valid, the error message says wrong password for 'valid' usernames
    - Shows invalid username error when username is not valid
  - [X] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/blob/4.2-branch/wp-login.php)
1. (Required) Image Title Attribute Cross Site Scripting
  - [ ] Summary: In the image title attribute can use XSS.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.21
  - [X] GIF Walkthrough: <img src="https://i.imgur.com/E0VcXY0.gif"></img>
  - [X] Steps to recreate:
    - Modify title attribute to malicious script
  - [X] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)
1. (Optional) Non-Sanitized Post Body x
  - [X] Summary: Unfiltered HTML in post body
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.3.1
  - [X] GIF Walkthrough: <img src="https://i.imgur.com/AxCtE6R.gif"></img>
  - [X] Steps to recreate:
    - Enter unfiltered html in post body (in this case a script alert)
  - [X] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/blob/4.2-branch/wp-includes/post-template.php)
1. (Optional) Non Sanitized Post Title
  - [X] Summary: Unfiltered HTML in post title
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.3.1
  - [X] GIF Walkthrough: <img src="https://i.imgur.com/9nxDmHD.gif"></img>
  - [X] Steps to recreate:
    - Enter unfiltered html in post title (in this case a script alert
  - [X] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/blob/4.2-branch/wp-includes/post-template.php)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

I did not have the skills to try out many of the vulnerabilities documented.

## License

    Copyright [2018] [Nabil Ahmed Khatri]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
