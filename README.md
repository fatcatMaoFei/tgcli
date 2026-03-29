# tg

A dead-simple Telegram CLI. One file, no frameworks, just works.

```
tg send "John" "hey, what's up?"
tg read "John" 20
tg chats
tg search "dev group"
tg file "John" ./photo.jpg
```

## Setup

1. Get `api_id` and `api_hash` from [my.telegram.org](https://my.telegram.org)
2. Install dependency:
   ```
   pip install telethon
   ```
3. Create config file `~/.tg.conf`:
   ```
   TG_API_ID=12345
   TG_API_HASH=your_hash_here
   ```
   Or set environment variables `TG_API_ID` and `TG_API_HASH`.

4. Login:
   ```
   python3 tg login
   ```
   Enter your phone number and the verification code Telegram sends you. Done.

## Usage

| Command | Description |
|---|---|
| `tg send <chat> <message>` | Send a text message |
| `tg read <chat> [n]` | Read last n messages (default 10) |
| `tg chats [n]` | List recent chats (default 20) |
| `tg search <query>` | Search contacts/chats by name |
| `tg file <chat> <path>` | Send a file, image, or video |
| `tg unread` | Show all unread messages |
| `tg watch [interval]` | Poll for new messages (default 30s) |
| `tg login` | Login or verify your session |

`<chat>` can be:
- A display name: `"John Doe"` (exact or partial match)
- A username: `@johndoe`
- A phone number: `+1234567890`

## Install globally

```bash
chmod +x tg
sudo cp tg /usr/local/bin/
```

## Requirements

- Python 3.8+
- [Telethon](https://github.com/LonamiWebs/Telethon)

## License

MIT
