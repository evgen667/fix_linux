# fix_linux


gsettings set org.gnome.desktop.wm.keybindings switch-input-source "['<Shift>Alt_L']"  или  "['<Alt>Shift_L']"   -- фикс в Gnome переключение раскладки клавиатуры

# Интеграция keepassxc в LibreWolf (не работает с Flatpak)
  
 ln -s ~/.mozilla/native-messaging-hosts ~/.librewolf/native-messaging-hosts

sudo ln -s /usr/lib/mozilla/native-messaging-hosts /usr/lib/librewolf/native-messaging-hosts

// https://librewolf.net/docs/faq/

# Запуск Rofi в kde по shortcut

sudo nano /usr/local/bin/rofi-run 
--------------------------------
#!/bin/bash 
export LC_ALL="C" 
rofi -show run 2>&1 | tee /tmp/rofi-run.log 
exit 0
--------------------------------
sudo chmod +x /usr/local/bin/rofi-run 
