# GL-AR750S-Ext
```sh
# Put the pw before running /pasting 
rm $home/.ssh/known_hosts  
ssh root@192.168.1.1
pw='WRITE PASSWORD HERE'
echo -e "$pw\n$pw" | passwd 
uci set wireless.default_radio0.ssid='Un birra mas por favor'
uci set wireless.default_radio0.encryption='sae-mixed'
uci set wireless.default_radio0.key="$pw"
#uci set wireless.default_radio0.disabled=0
uci set wireless.default_radio1.ssid='Un birra mas por favor'
uci set wireless.default_radio1.encryption='sae-mixed'
uci set wireless.default_radio1.key="$pw"
#uci set wireless.default_radio1.disabled=0
uci set wireless.radio0.disabled=0
uci set wireless.radio1.disabled=0
uci commit wireless
wifi
```


