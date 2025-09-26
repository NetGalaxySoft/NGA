# Конфигуриране на Kubuntu 24.04

Този документ съдържа инструкции за настройка на Kubuntu 24.04 след инсталация.

---

### 1. Езикови настройки и клавиатурни комбинации

Проблем: по подразбиране комбинацията Alt+Shift отваря търсачката вместо да сменя езика.

### Решение:

1. Отворете настройките за бързи клавиши:  
   - Български интерфейс: **Системни настройки → Клавишни комбинации → KWin → KRunner**  
   - English interface: **System Settings → Shortcuts → KWin → KRunner**

2. Отворете настройките:  
   - Български: **KRunner**  
   - English: **KRunner**

3. Премахнете отметката:  
   - Български: ❌ **Alt+Интервал**  
   - English:   ❌ **Alt+Space**

4. Запишете настройката с бутона:  
   - Български: **Прилагане**  
   - English: **Save**

5. Отворете настройките на клавиатурните подредби:  
   - Български интерфейс: **Системни настройки → Клавиатура → Разширени**  
   - English interface: **System Settings → Keyboard → Layouts**

6. Отворете секцията:  
   - Български: **Switching to another layout**  
   - English: **Switching to another layout**

7. Поставете отметка на желаните комбинации (може да бъдат няколко). Например:  
   - ✅ **Alt+Shift**  
   - ✅ **Alt+Space**

### Резултат
- ✅ **Alt+Shift** → смяна на езика  
- ✅ **Meta+Space** → търсачка (KRunner)


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
