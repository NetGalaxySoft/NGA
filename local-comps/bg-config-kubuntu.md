# Конфигуриране на Kubuntu 24.04

Този документ съдържа инструкции за настройка на Kubuntu 24.04 след инсталация.  
Фокусът е върху най-важните стъпки за курса в NetGalaxy Academy.

---

## 1. Езикови настройки и клавиатурни комбинации

Проблем: по подразбиране комбинацията Alt+Shift отваря търсачката вместо да сменя езика.  

### Решение:
1. Отворете **System Settings → Shortcuts → KWin → KRunner**  
   - Намерете *Activate KRunner*  
   - Променете комбинацията на **Meta+Space**

2. Отворете **System Settings → Keyboard → Layouts**  
   - Активирайте *Configure Layouts*  
   - В *Switching Options* изберете **Alt+Shift**

### Резултат:
- Alt+Shift → смяна на езика  
- Meta+Space → търсачка (KRunner)

---

## 2. Инсталиране на VSCodium

Инсталирайте VSCodium от официалното хранилище:

```bash
sudo apt update
sudo apt install -y wget gpg apt-transport-https
wget -qO - https://gitlab.com/paulcarroty/vscodium-deb-rpm-repo/-/raw/master/pub.gpg \
  | sudo gpg --dearmor -o /usr/share/keyrings/vscodium-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/vscodium-archive-keyring.gpg] \
  https://download.vscodium.com/debs vscodium main" \
  | sudo tee /etc/apt/sources.list.d/vscodium.list
sudo apt update
sudo apt install -y codium
