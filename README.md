<img src="https://github.com/idammi/tiktok-rest-api/blob/main/assets/tiktok.png" width=75 align=left> <h1>TikTok API Service</h1>
API Wrapper for TikTok private API access
<br>


## How does this work?
Monthly subscription of my private API service is required for this to function.


## Usage
```php

/////////// API  //////////
$debug = false;
$accessKey = 'YOUR_ACCESS_KEY';
$proxy = 'http://user:pass@proxy:port';
///////////////////////////
$tiktok = new \TikTokAPI\TikTok($debug);
$tiktok->setAccessKey($accessKey);
$tiktok->setProxy($proxy);
```


## Available methods
- `login` - Login user/resume logged in session `login($username, $password)`
- `like` - Like a post `like($awemeId)`
- `unlike` - Unlike a post `unlike($awemeId)`
- `comment` - Comment on a post `comment($awemeId, $commentText)`
- `follow` - Follow a user `follow($secUserId)`
- `unfollow` - Unfollow a user `unfollow($secUserId)`
- `getUserInfo` - Get user info `getUserInfo($secUserId)`
- `search` - Search for user `search($keyword)`


## TikTok Private API service subscription pricing

| Package | Cost(per month) | Quota(requests per day) | Quota (requests per month) |
| ------- | :---------------: | --------------: | -----------------: |
| **Pro** *(popular)* | 50 USD | 5,000 | ~150,000 |
| **Business** | 100 USD | 12,000 | ~360,000 |
| **Custom** | custom pricing | ? | ? |

- These quota counts doesn't include Account Login requests unless it's a new login which requires device registration.


## Private API backend functionalities

- Device registration for registering `device_id`, `install_id` also known as `iid` and `did`.
    - Proper `trace-id` header generation.
    - Proper `X-Gorgon` and `X-Khronos` header generation.
    - Proper `TTEncrypt`ing of data (v05).
    - Proper `XLog`ing of registered device_id (v02).

- Account Login
    - Complete device registration when logging in for the first time.
    - Account Login with username/password.
    - Automated captcha solver.


## Terms and conditions

- You will NOT use this API for marketing purposes (spam, botting, harassment, massive bulk messaging...).
- We do NOT give support to anyone who wants to use this API to send spam or commit other crimes.
- We reserve the right to block any user of this repository that does not meet these conditions.

## Legal

This code is in no way affiliated with, authorized, maintained, sponsored or endorsed by TikTok or any of its affiliates or subsidiaries. This is an independent and unofficial API. Use at your own risk.

##  Disclaimer
TikTok is always updating their API endpoints but I will keep updating this library. I take no responsibility if your IP or your acccount gets banned using this API. It's recommended that you use proxy.

If you want, you can reach me on Telegram: https://t.me/dologbonjaye