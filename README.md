# RoWifi Python Client

`rowifi-python` is an asynchronous Python client for the [RoWifi API](https://rowifi.xyz/docs/api).  
It allows you to interact with RoWifi services, including managing members, denylists, ranks, and more.

## Features

- Async API requests using `aiohttp`
- Easy access to RoWifi endpoints
- Pydantic models for structured responses
- Supports authentication via API token

## Installation

```bash
pip install rowifi-python
```
## Usage

```python
import asyncio
from rowifi import RoWifiClient

async def main():
    # Initialize client with your API token
    client = RoWifiClient(token="your_api_token_here")

    # Example: fetch a user by Roblox ID
    user_data = await client.get_user(user_id=123456)
    print(user_data)

    # Example: fetch the denylist
    denylist = await client.get_denylist()
    print(denylist)

asyncio.run(main())
```
## Notes

All methods are asynchronous; use `await` or run inside `asyncio.run()`.

Replace "your_api_token_here" with your actual RoWifi API token.