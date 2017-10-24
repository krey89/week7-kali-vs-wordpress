# Project 7 - WordPress Pentesting

Time spent: 3 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Cross Site Scripting
  - [ ] Summary:
    - Vulnerability types:Cross Site Scripting
    - Tested in version:4.2
    - Fixed in version: 4.6
  - [ ] GIF Walkthrough:
    [URL=/gif/-Y-_MQn][IMG]https://i.makeagif.com/media/10-24-2017/Y-_MQn.gif[/IMG][/URL]
  - [ ] Steps to recreate: 1) Create New Comment
                          2) Add <script>alert("XSS")</script> as a comment, alert will show up after refresh.
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)
1. (Required) XSS on HTML
  - [ ] Summary:
    - Vulnerability types:XSS
    - Tested in version:4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: [URL=/gif/-YIQmhD][IMG]https://i.makeagif.com/media/10-24-2017/YIQmhD.gif[/IMG][/URL]
  - [ ] Steps to recreate: In the comment field leave over 64 KB worth of text to cause page to change.
  - [ ] Affected source code:
    - [Link 1](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5622)
1. (Required) Authenticated Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary:
    - Vulnerability types:XSS
    - Tested in version:4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: [URL=/gif/-LqZJ_S][IMG]https://i.makeagif.com/media/10-24-2017/LqZJ_S.gif[/IMG][/URL]
  - [ ] Steps to recreate: Add https://youtube[.]com/watch?v=123<svg onload=alert(1)>
                          as a post.
                          Alert will show up after the page refreshes.
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)

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
