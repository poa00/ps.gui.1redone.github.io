---
title: "WSUS, No checkbox to 'Import Update directly into Windows Server Update Services'"
date: "2013-12-02"
redirect_from : /2013/12/02/wsus-no-checkbox-to-import-update-directly-into-windows-server-update-services
tags: 
  - "sccm"
  - "updates"
---

This was something of a puzzle for a few earlier today.

For a client, we needed to manually add an update to WSUS, to sync with SCCM for deployment. As one would expect, I launched Update Services, then right-clicked my server to launch the import update UI.

![](../assets/images/2013/12/images/wsus02.png)

However, upon launching the Update Catalog, no checkbox is available to 'Import directly into Windows Server Update Services'. Instead, the only option is to download the update content to a local directory, which is much less useful.

![wsus03](../assets/images/2013/12/images/wsus03.png) Missing Checkbox? There is no way to Import into WSUS as you see here.

**Symptom**: When launching the Microsoft Update Catalog from WSUS, no checkbox is available to allow for importing content into WSUS.

**Cause**: As seen below " You must be logged on to the computer as an administrator to import the hotfixes.

From <http://technet.microsoft.com/en-us/library/cc708583> "

**Solution**: Make sure you run the Windows Server Update Services console as an administrator.

This was pretty simple!  Make sure you run the WSUS Console as an Administrator.

![wsus04](../assets/images/2013/12/images/wsus04.png)
