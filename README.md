# Telegram Magic 💛

## Setting up
Firstly, you need to get your _api_id_ and _api_hash_.
For that go to https://my.telegram.org/ and log in with your _phone number_. You will receive a _code_ in the Telegram.

Now click _API development tools_ and copy two parameters: `api_id` and `api_hash`.

When you have them, open `config.ini` and `main.py` in any text editor and write your APIs in the following format:

In **config.ini**
```ini
[pyrogram]
api_id = 79230203
api_hash = 782a3oe32aho234ddoeuae9i734dtdtd8
```
In **main.py**
```python
app = Client(
    "my_account",
    api_id=79230203,
    api_hash="782a3oe32aho234ddoeuae9i734dtdtd8"
)
```

## First launch
Open the folder in terminal and run

```python3 main.py```

It will ask you to enter your phone number, then enter the confirmation code from Telegram (and confirm with Telegram account password if you have one)

> This is an **official operation** and authorization session will be kept locally in the same folder as ```main.py```

## Run

When the program is launched, you will get the message in terminal telling you that your program is running. Now go to your messages and type ```heart text```. When the animation is over, the message will look like this: 

💛 _text_

> You can also only type ```heart``` and in the end there won't be any text after 💛.



## Limitations
Sometimes Telegram gives you flood wait and you are unable to edit messages. Usually it varies from 30 seconds to 300 seconds. You can experiment with `time_sleep` parameter in `main.py`.

By default it's:

```python
time_sleep = 0.325  # cooldown between frames
```

## Your own animations
You can edit/add new animations, for that create new python file and write frames in python list. You can examine example in `heart.py`.
