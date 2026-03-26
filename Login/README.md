# OAuth Login

Even after I had patched RŌBLOX v548's binary to patch out ``roblox.com`` links to ``rbolock.tk``, I noticed the log file still made a HTTP GET to ``apis.roblox.com``.

I was also unable to login yet.

```
[DFLog::HttpTraceLight] HttpRequest(#1 0000020FCCAD1D30) GET url:"https://apis.roblox.com/oauth/.well-known/openid-configuration" cachePolicy:0 external:0 retry:1

[DFLog::HttpTraceLight] HttpResponse(#1 0000020FCCAD1D30) time:179.0ms (net:179.0ms callback:0.0ms timeInRetryQueue:0.0ms)status:200 OK bodySize:1217 url:"https://apis.roblox.com/oauth/.well-known/openid-configuration" ip:128.116.32.3 external:0 numberOfTimesRetried:0
```

Searching for ``OAuth`` in HxD lead me to find ``StudioLogin.Start.Auto.Cached [nul] ApplicationConfig/OAuth2Config.json``

This is inside of Studio's directory!

1. Find .\ApplicationConfig\OAuth2Config.json

You'll see two links relating to OAuth, one is global, one is for China #1 glory to the somthin

2. Change the link. I changed it to ``apis.rbolock.tk:2005`` 