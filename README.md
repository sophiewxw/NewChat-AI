# NewChat-AI```

*2. CSS (style.css):*

```css
body {
  margin: 0;
  font-family: 'Segoe UI', sans-serif;
  background: #0f0f1b;
  color: white;
}

.login-screen {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  gap: 10px;
}

input, button, select {
  padding: 10px;
  font-size: 1em;
  border: none;
  border-radius: 5px;
  outline: none;
}

button {
  background: #4b00ff;
  color: white;
  cursor: pointer;
}

.chat-container {
  display: flex;
  height: 100vh;
}

.sidebar {
  width: 200px;
  background: #1e1e2f;
  padding: 20px;
}

.chat-area {
  flex: 1;
  display: flex;
  flex-direction: column;
  background: #141427;
}

.chat-messages {
  flex: 1;
  padding: 20px;
  overflow-y: auto;
}

.chat-input {
  display: flex;
  padding: 10px;
  background: #1e1e2f;
}

.chat-input input {
  flex: 1;
  margin-right: 10px;
}

.hidden {
  display: none;
}
```

*3. JavaScript (script.js):*

```javascript
function login() {
  const user = document.getElementById('username').value;
  const pass = document.getElementById('password').value;

  if (user && pass) {
    document.getElementById('loginScreen').classList.add('hidden');
    document.getElementById('chatContainer').classList.remove('hidden');
  }
}

function sendMessage() {const input = document.getElementById('chatInput');
  const message = input.value.trim();
  if (message) {
    const chatBox = document.getElementById('chatMessages');
    const msg = document.createElement('div');
    msg.textContent = `Você: ${message}`;
    chatBox.appendChild(msg);
    input.value = '';
  }
}
```
