print("""
  __  __                            
 / _|/ _|_ __ _ __ ___   __ _ _ __  
| |_| |_| '__| '_ ` _ \ / _` | '_ \ 
|  _|  _| |  | | | | | | (_| | | | |
|_| |_| |_|  |_| |_| |_|\__,_|_| |_|
                                    

 <!!> Telegram : @ffrman""")
print("-----------------------------------")

import random
import requests
import time
import threading
a = 0
f = open("user.txt","r").read().splitlines()
def king_givt():
    for username in f:
        global a
        p = []
        for i in open("p.txt", "r").read().splitlines():
            p.append(i)
        newproxy = {
            'http': 'http://{}'.format(p),
            'https': 'https://{}'.format(p)}
        try:
            proxy = str(random.choice(p))
            url = (f"https://accounts.snapchat.com/accounts/get_username_suggestions?requested_username={username}&xsrf_token=_W2GHDQLlCXbXPlWAMuOeQ")
            headers = {
                "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.14; rv:66.0) Gecko/20100101 Firefox/66.0",
                "Accept": "*/*",
                "Accept-Language": "en-US,en;q=0.5",
                "Referer": "https://accounts.snapchat.com/",
                "Cookie": "xsrf_token=_W2GHDQLlCXbXPlWAMuOeQ; sc-cookies-accepted=true; web_client_id=b1e4a3c7-4a38-4c1a-9996-2c4f24f7f956; oauth_client_id=c2Nhbg==",
                "Connection": "keep-alive",
                "Content-Type": "application/x-www-form-urlencoded; charset=utf-8",
            }
            r = requests.post (url, headers=headers)
            a+=1
            if r.text.find('"status_code":"OK"') >= 0:
                print("\متاح:",username)
                time.sleep(1)
            else:
                print(f"\rغير متاح:{a}  = {username}",end="")
                time.sleep(1)
                proxy = str(random.choice(p))
        except Exception as e:
            print(e)

king_givt()
