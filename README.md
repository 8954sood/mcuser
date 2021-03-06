# mcuser


[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)
> Module for parsing Minecraft playerdb.co

> testing python version 3.8

## Synchronous
```py
from mcuser import MCuser


def main():
    Main = MCuser.lookup("username or user uuid of id")
    Text = Main.user_check() #return dict
    User = Main.user_name() #return str
    Users = Main.user_names() #return json
    Userid = Main.user_id() #return str
    Userrawid = Main.user_rawid() #retrun str
    Useravatar = Main.user_avatar() #return str url

main() #return
"""
Text = {'code': 'player.found', 'message': 'Successfully found player by given ID.', 'success': True}
User = Name
Users = [{'name': '_Siu'}, {'name': 'Name', 'changedToAt': 1423044715000}, {'name': 'name', 'changedToAt': 1430030146000}, {'name': 'Name', 'changedToAt': 1482572974000}]
Userid = fa90ba90-9446-4141-83c5-6b31487112c3
Userrawid = fa90ba909446414183c56b31487112c3
Useravatar = https://crafatar.com/avatars/fa90ba909446414183c56b31487112c3
"""
```

## Asynchronous
```py
import asyncio
from mcuser import asyncMCuser


async def main():
    Main = await asyncMCuser.lookup("username or user uuid of id")
    Text = await Main.user_check() #return json
    User = await Main.user_name() #return str
    Users = await Main.user_names() #return json
    Userid = await Main.user_id() #return str
    Userrawid = await Main.user_rawid() #retrun str
    Useravatar = await Main.user_avatar() #return str url

asyncio.run(main())#return
"""
Text = {'code': 'player.found', 'message': 'Successfully found player by given ID.', 'success': True}
User = Name
Users = [{'name': '_Siu'}, {'name': 'Name', 'changedToAt': 1423044715000}, {'name': 'name', 'changedToAt': 1430030146000}, {'name': 'Name', 'changedToAt': 1482572974000}]
Userid = fa90ba90-9446-4141-83c5-6b31487112c3
Userrawid = fa90ba909446414183c56b31487112c3
Useravatar = https://crafatar.com/avatars/fa90ba909446414183c56b31487112c3
"""
```
