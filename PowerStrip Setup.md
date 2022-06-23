# 1. Connect to the local Wi-Fi the server is on (two methods)
## The graphical way: 
Follow TP-link's guide https://www.tp-link.com/us/support/faq/2527/

## The programmatic way:
1. Install `python-kasa` package
```
pip3 install python-kasa
```
2. connect to the strip's own wifi, it usually starts with sth like `TP_LINK_blahblah`

3. Run this command:
```
kasa --host 192.168.0.1 wifi join [wifi ssid] [wifi password]'
```
If it's an open WiFi network, leave out the password. 

(Optional) If we want to name the power-strip (this would be changing the entity name in HA), run:
```
kasa --host [tp-ip] alias name_string
```
where `[tp-ip]=192.168.0.1` if this optional step is done before step 3; and if done after step 3`[tp-ip]=192.168.0.x` where `x` is the ip address assigned to the power strip.  

# 2. Add the Power Strip onto HomeAssistant
![](/attachements/2022-06-22%2022.42.28.gif)

# 3. Assign/Change Device Name and/or Entity ID
![](/attachements/2022-06-22%2022.42.28.gif)
