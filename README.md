# Discord24/7
Một Chương Trình Làm Cho Tài Khoản Discord Của Bạn Trong Phòng Voice 24/7

----
</br>

```py
import discord
import os
from discord.ext import commands

client=commands.Bot(command_prefix=':', self_bot=True, help_command=None)

GUILD_ID = ID_CUA_SERVER
CHANNEL_ID = ID_PHONGVOICE

@client.event
async def on_ready():
    os.system('clear')
    print(f'Đã Đăng Nhập Tài Khoản {client.user} ({client.user.id})')
    vc = discord.utils.get(client.get_guild(GUILD_ID).channels, id = CHANNEL_ID)
    await vc.guild.change_voice_state(channel=vc, self_mute=False, self_deaf=False)
    print(f"Đã Vào Thành Công {vc.name} ({vc.id})")

client.run(os.getenv("TOKEN"))
```
**Đừng Đưa Token Của Bạn Cho Thằng Nào, Tự Làm Tự Treo Đi**

Sử dụng [uptimerobot.com](https://uptimerobot.com) để treo cái Replit của bạn 24/7

</br>