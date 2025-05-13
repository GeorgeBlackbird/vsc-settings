# ⚙️ VSC Settings Backup

Резервная копия моих пользовательских настроек Visual Studio Code:<br><br>
🔧 `settings.json`,<br>
🖱️ `keybindings.json`,<br>
📦 Список расширений,<br><br>
...и другие настройки.

---

## 🚀 Быстрая настройка на новом устройстве

### 1. 🔁 Клонируем репозиторий

```bash
git clone https://github.com/GeorgeBlackbird/vsc-settings.git
cd vsc-settings
```

### 2. 📦 Устанавливаем расширения

```bash
cat extensions.txt | xargs -n 1 code --install-extension
```

### 3. ⚙️ Копируем настройки

#### Windows
```bash
xcopy /Y settings.json "%APPDATA%\Code\User\settings.json"
xcopy /Y keybindings.json "%APPDATA%\Code\User\keybindings.json"
xcopy /E /Y snippets "%APPDATA%\Code\User\snippets\"
```

#### Linux
```bash
cp settings.json ~/.config/Code/User/settings.json
cp keybindings.json ~/.config/Code/User/keybindings.json
cp -r snippets/ ~/.config/Code/User
```

#### macOS
```bash
cp settings.json ~/Library/Application\ Support/Code/User/settings.json
cp keybindings.json ~/Library/Application\ Support/Code/User/keybindings.json
cp -r snippets/ ~/Library/Application\ Support/Code/User/
```

---

## 💾 Сохранение текущих настроек

Если ты хочешь обновить резервную копию:
```bash
code --list-extensions > extensions.txt
```
А затем скопируй актуальные:
* `settings.json`
* `keybindings.json`
* Папку `snippets/`

---

## 🛠 Альтернатива — автоматическая синхронизация

Можно использовать расширение [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync) для автоматической синхронизации через GitHub Gist.

---

## 📌 Полезные ссылки

* [VS Code User Folder Paths](https://code.visualstudio.com/docs/configure/keybindings#_keyboard-shortcuts-reference)
* [CLI команды VS Code](https://code.visualstudio.com/docs/configure/command-line)

---

> 🧠 **Помни:** После копирования настроек лучше перезапустить VS Code.
