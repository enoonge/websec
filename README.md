# Project 7 - WordPress Pentesting

Time spent: **4** hours spent in total

> Objective: Find, analyze, recreate, and document **three or more vulnerabilities (up to five)** affecting an old version of WordPress

## Pentesting Report

1. (Required) 4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.1
    - Fixed in version: 4.213
  - [x] GIF Walkthrough: <img src='https://i.imgur.com/Yf6oCQx.gif' title='GIF Walkthrough' width='800' alt='GIF Walkthrough' />
  
  - [x] Steps to recreate: 
    * Login
    * Create a new post with any youtube link embed and append XSS payload at end (escaped)
    * Ex: [embed src='https://youtube.com/embed/link\x3csvg onload=alert(1)\x3e'][/embed]
  
  - [x] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/f72b21af23da6b6d54208e5c1d65ececdaa109c8)
  
2. (Required) Authenticated Stored Cross-Site Scripting (XSS Shortcode)
  - [x] Summary: 
    - Vulnerability types:XSS
    - Tested in version:4.1
    - Fixed in version: 4.2.3
  - [x] GIF Walkthrough: <img src='https://i.imgur.com/pCUKleg.gif' title='GIF Walkthrough' width='800' alt='GIF Walkthrough' />
  - [x] Steps to recreate: 
    * Make a new text post
    * Escape HTML tag with shortcode tag and insert XSS payload
  - [x] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/f72b21af23da6b6d54208e5c1d65ececdaa109c8)
    
    
  
3. (Required) Unauthenticated Stored Cross-Site Scripting (XSS)
  - [x] Summary: 
    - Vulnerability types:XSS
    - Tested in version:4.1
    - Fixed in version: 4.1.2
  - [x] GIF Walkthrough: <img src='https://i.imgur.com/XzH9KOZ.gif' title='GIF Walkthrough' width='800' alt='GIF Walkthrough' />
  - [x] Steps to recreate: 
    * Create post
    * Comment on post with html tag with XSS payload inserted after the tag
    * XSS payload will execute when viewed by user/admin
  
  

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
