## For Studio:
1. Open RobloxStudioBeta.exe in HxD
2. Replace all strings
3. Find roblox.com, replace with rbolock.tk
4. Save

Make sure AppSettings.xml also has either:

To temporarily bypass SSL:
``<BaseUrl>https://localhost:2005</BaseUrl>``

Though, the v535 binary from Jetray had:
``<BaseUrl>https://rbolock.tk:2005</BaseUrl>`` It's what I changed to after realizing.

Worth noting that RFD does edit AppSettings.xml to change it to localhost.