![Screenshot_1](https://github.com/user-attachments/assets/292f8000-8a8f-4b67-b0ca-0fa99cd635d6)

# BlitzGram

Welcome to the newest Instagram automation tool!  
This is a licensed tool and can be purchased by contacting [MrGrassss](https://t.me/MrGrassss).

## Features:

- Mass DM
- Profile Picture Changer
- Username Changer
- Display Name Changer
- Bio Changer
- URL Changer
- Scraper
- Account Generator

## Future:

- Any feature can and will be added on demand

# Extra Functionality Info

## Login & Setup

- **Accounts Format:** Supports multiple formats:
    - `username:pass:email:pass`
    - `username:pass`
    - `email:pass`
    - `phone:pass`

- **Sessions Format:** Use `acc_id:session` format.

- **Proxies:** Supports sticky/rotating proxies in the following formats:
    - `HOST:PORT@USERNAME:PASSWORD`
    - `HOST:PORT:USERNAME:PASSWORD`
    - `HOST:PORT`

- **Accounts:** Accounts from `accounts.txt` are logged in and saved to `sessions.txt`, ensuring no duplicates.

- **2FA:** Two-factor authentication is supported.

- **Files:**
    - `client_info/profile_pics`: Store profile pictures here.
    - `client_info/usernames.txt`: List of usernames.
    - `client_info/names.txt`: List of display names.
    - `client_info/bios.txt`: List of bios.
    - `client_info/site_urls.txt`: List of URLs to be used. URLs should have a correct schema,
      e.g., `https://github.com/`.

- **Threading:**
    - All functions are threaded except for logging in through `accounts.txt`, meaning that logging in through sessions
      is threaded.

## Account Generator

- **Overview:** Generate new Instagram accounts using HQ un-flagged proxies.
- **Saved Accounts:** Generated accounts are saved into `gen/accounts.txt`.
- **Saved Sessions:** Generated sessions are saved into `gen/sessions.txt`.
- **Email Usage:** Either use tempmail or kopeechka by setting "use_temp_mail" to "false" and inputting your "
  kopeechka_token"
- **Proxies:** Sticky residential proxies are needed and one thread equals one proxy. Entering more threads than
  available proxies will always cap the threads.
- **Config:** You will find "run_forever" in `gen/config.json`. This will loop threads with the same proxies. Make sure
  that you set your sticky proxies to by using "proxy_reset_delay" (seconds) in `gen/config.json` if "run_forever" is
  set to "true". You will also find the option "use_temp_mail" and "kopeechka_token" to enable kopeechka.

## Account Functionalities

- **Profile Picture Changer:** Update the profile picture of your Instagram accounts.
- **Username Changer:** Change the username of your profiles.
- **Display Name Changer:** Change the display name of your profiles.
- **Bio Changer:** Modify the bio of your Instagram accounts.
- **URL Changer:** Update the URL in your Instagram profile.

## Scraper

- **Followers Scraper:** Scrape followers of specified accounts and save data to `scraper/user_info.json`.
- **Likers Scraper:** Scrape users who liked specific posts. Save posts to `scraper/posts.txt`.

### Scraper Configuration:

- **Limit Per Account:** Set in `scraper/config.json`. Use `0` for unlimited.
- **Posts Format:** Use the full URL, e.g., `https://www.instagram.com/p/Cq4gcQGKwVX`, or just the post ID,
  e.g., `Cq4gcQGKwVX`.

## Mass DM

- **Overview:** Automate sending direct messages to users scraped by the scraper feature. `scraper/user_info.json`.
- **Message Configuration:** Set up in `mass_dm/config.json` and `mass_dm/message.txt`. Emojis can be added like this ❤️
- **Attachments:** Store images and videos in `mass_dm/images` and `mass_dm/videos`.
- **Usernames.txt** Instead of the scraped users in `scraper/user_info.json` add usernames to `mass_dm/usernames.txt` 
  or user_ids to `mass_dm/user_ids.txt` that will be messaged when "use_scraped_users" is set to "false" in 
  `mass_dm/config.json`
  

### Mass DM Configuration:

- **Timing:** Configure `seconds_before_dm` and `dm_limit_per_acc` in `mass_dm/config.json`. Instagram's daily DM limit
  is 100.
- **Attachments Usage:** Set `use_images` and `use_video` to `true` to send random images or videos with messages.
- **Results:** Successful messages are saved to `mass_dm/processed(user_ids/usernames)/success.txt`, and failed ones 
  to `mass_dm/processed(user_ids/usernames)/failed.txt`. Duplicates are skipped on rerun.
  

## Client Checker

- **Overview:** Use the client checker to view all information about your clients in a searchable UI.
- **Functionality:** Includes threaded operations for checking clients.

## Account Issues

- **Flagged Accounts:** Flagged accounts are removed and saved to `flagged_accounts.txt`.
- **Bad Sessions:** Bad sessions are saved to `bad_sessions.txt`.

## Suggestions / Feedback

I'm open to any suggestions or feedback!

For questions, you can always contact me on [Telegram](https://t.me/MrGrassss).

https://github.com/MrGrasss/BlitzGram-InstagramTool/assets/132838549/2ce6caee-f623-4022-a83b-106a76b50e41
