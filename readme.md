![Screenshot_1](https://github.com/user-attachments/assets/66dc4f87-d2b2-4a13-bf76-5f162a8aa1e9)

---

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
- Scraper (Full info included)
- Client Checker
- Equal Follower
- Mass Post Commenter
- Mass Comments Liker
- Mass Post Liker
- Mass Saves (post/reels)
- Mass Shares (posts/reels/stories)
- Mass views (posts/reels/stories)
- Mass Feed Poster

## Future:

- Any feature can and will be added on demand
- Account Generator separate from this tool. 

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
      is faster.

- **Caution:**
    - When logging into a session, keep that account in accounts.txt in case you need to re-login (refresh the session);
      the tool can do so.
  
- **Safety**
    -  When using sessions the tool will automatically re-login to these using the credentials of that session in 
       accounts.txt when needed.

## Account Functionalities

- **Profile Picture Changer:** Update the profile picture of your Instagram accounts.
- **Username Changer:** Change the username of your profiles.
- **Display Name Changer:** Change the display name of your profiles.
- **Bio Changer:** Modify the bio of your Instagram accounts.
- **URL Changer:** Update the URL in your Instagram profile.

## Scraper

- **Followers Scraper:** Scrape followers of a specified account and save data to `scraper/user_info.json`.
- **Likers Scraper:** Scrape users who liked specific posts. Save posts to `scraper/posts.txt`.

### Scraper Configuration:

- **Posts Format:** Use the full URL, e.g., `https://www.instagram.com/p/Cq4gcQGKwVX`, or just the post ID,
  e.g., `Cq4gcQGKwVX`.

## Mass DM

### Overview:

Automate sending direct messages to users scraped by the scraper feature or to a list of specified usernames or user
IDs.

### Prerequisites:

1. **Scraped Users:** Ensure users are scraped and saved in `scraper/user_info.json`.
2. **Usernames:** Alternatively, add usernames to `mass_dm/usernames.txt` or user IDs to `mass_dm/user_ids.txt`.
3. **Proxies:** Ensure proxies are set up correctly in the supported formats.

### Setup:

1. **Message Configuration:** Set up in `mass_dm/config.json` and `mass_dm/message.txt`. Emojis can be added like this
   ❤️.
2. **Attachments:** Store images and videos in `mass_dm/images` and `mass_dm/videos`.
3. **Use Scraped Users:** Set "use_scraped_users" to "true" in `mass_dm/config.json` to use users
   from `scraper/user_info.json`.

### How to Use:

1. **Run the Mass DM:** Launch the feature from the main menu.
2. **Configure Timing:** Set `seconds_before_dm` and `dm_limit_per_acc` in `mass_dm/config.json`. Instagram's daily DM
   limit is 100.
3. **Send Messages:** The tool will read the message configuration and attachments, and send DMs accordingly.

### Results:

- Successful messages are saved to `mass_dm/processed(user_ids/usernames)/success.txt`, and failed ones
  to `mass_dm/processed(user_ids/usernames)/failed.txt`. Duplicates are skipped on rerun.

## Client Checker

- **Overview:** Use the client checker to view all information about your clients in a searchable UI.
- **Functionality:** Includes threaded operations for checking clients.

## Account Issues

- **Flagged Accounts:** Flagged accounts are removed and saved to `flagged_accounts.txt`.
- **Bad Sessions:** Bad sessions are saved to `bad_sessions.txt`.

## Equal Follower

**Description:**

The Equal Follower feature allows you to distribute a list of usernames across multiple Instagram accounts,
ensuring that each account follows a unique set of users without any overlap.

**How It Works:**

1. **Upload Usernames:**
    - Fill `equal_follower/usernames.txt` with the usernames you want to follow. (1 per line)
   
2. **Setup Config:**
    - Fill `equal_follower/config.json` with the min and max seconds before follow.

3. **Set Parameters:**
    - Specify the number of clients (Instagram accounts) to use.
    - Define the number of usernames each client should follow.

4. **Distribute Follows:**
    - The Equal Follower will allocate usernames to each account sequentially, ensuring no duplicates.

**Usage Example:**

- You have a `usernames.txt` file of 500 usernames.
- You want to use 10 accounts, each following 50 users.
- Equal Follower will ensure each of the 10 accounts follows a unique set of 50 users.

## Mass Commenter

### Overview

Automate commenting on Instagram posts using multiple accounts. The tool facilitates posting comments on a 
specified Instagram post.

### Prerequisites

1. **Message Content:**
   - Ensure the comment message is stored in `mass_commenter/message.txt`.

2. **Post URL:**
   - Provide the post URL in the format: `https://www.instagram.com/p/POST_ID/`.

### Setup

1. **Message Configuration:**
   - Store the comment message in `mass_commenter/message.txt`.

2. **Post URL Validation:**
   - The tool will validate the post URL and fetch the required media information.

### How to Use

1. **Initialize the Mass Commenter:**
   - Provide the list of Instagram accounts and specify the post URL.

2. **Run the Mass Commenter:**
   - Execute the tool to start posting comments on the specified post.

### Results

- **Successful Comments:** Successfully posted comments will be logged, and you will receive updates on 
  the number of successful posts.


## Mass Feed Poster

### Overview

 Automatically posts images or videos with a message to Instagram feeds using multiple client accounts.

### Prerequisites

1. **Message Content:**
   - Ensure the post message is stored in `mass_feed_poster/message.txt`.

2. **Message Content:**
   - Ensure either images or videos are stored in `mass_feed_poster/images(videos)`

### Setup

1. **Message Configuration:**
   - Store the comment message in `mass_feed_poster/message.txt`.

2. **Media Configuration:**
   -  Place images in the `mass_feed_poster/images` directory or videos in the `mass_feed_poster/videos` directory.

### Results

- **Successful Comments:** Successfully posted comments will be logged, and you will receive updates on 
  the number of successful posts.


## Suggestions / Feedback

I'm open to any suggestions or feedback!

For questions, you can always contact me on [Telegram](https://t.me/MrGrassss).

---

https://github.com/MrGrasss/BlitzGram-InstagramTool/assets/132838549/2ce6caee-f623-4022-a83b-106a76b50e41

https://github.com/user-attachments/assets/093660a7-c293-4a92-bbfb-0bd134d246da
