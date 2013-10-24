Onenote-duplicates-remover
==========================

A simple to find out duplicated OneNote pages and remove them.

Motivation
----------
* As time passed, my OneNote collection grows too much and I had left many duplicated pages as they were. The pages are incidentally created by a synchronization process. The number of duplicated pages was 15,000. It couldn't be resolved by hands.
* Of course, there were many existing excellent file duplication checkers. However, in OneNote file format, there are varying attributes such as 'GUID' or 'Last Modified'. Although file contents were the exactly same, the attributes might be different so its file hash value was completely different.
* This tool uses API provided by Microsoft OneNote to determine duplicated set, i.e., to calculate file hash without considering any meta data. Meta data **does not** mean text styles, colors and embedded images.

Requirements
------------
* Microsoft Office OneNote 2010 or 2013
* .NET framework 4.5 (2.0 would be okay, but the solution is generated by VS 2012)

Usage
-----
** PLEASE BACKUP YOUR ONENOTE FILES BEFORE PROCEEDING ANY REMOVAL OPERATION **
* I've tested many cases such as password protected pages, pages in the SkyDrive, shared pages. However, I can’t guarantee every corner cases. So that's why I strongly recommend to backup your data. If you feel suspicious, please review the code and report a bug. (Always welcome!)

* Press 'Scan your duplicated OneNote files' button and wait for finish.
* If the tool displays duplicated sets, rearrange your folder preference for selecting pages. A folder containing unwanted pages should be below.
* Press 'Select all except one' will check your pages **which are going to be deleted**. [IMPORTANT] If you check **every** pages, this tool wouldn't care about it. **Make sure your selection does not mean 'delete everything'**.
* Finally, Press 'Remove the selected pages' button to remove your selected pages.

Tip
---
* Enabling 'Navigate to the highlighted page automatically' means any existing OneNote instance will open the page automatically. It can help you to take account of importance of the page.

License
-------
* MIT License

Download
--------
* I didn't implement a late binding of COM object, so you may choose the followings according to your office version.

* [office 12 (2007)](https://github.com/relue2718/onenote-duplicates-remover/blob/master/publish/12.zip)

* [office 14 (2010)](https://github.com/relue2718/onenote-duplicates-remover/blob/master/publish/14.zip)

* [office 15 (2012)](https://github.com/relue2718/onenote-duplicates-remover/blob/master/publish/15.zip)
