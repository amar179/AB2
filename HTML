# main.py
echo "import os
from flask import Flask, render_template, request, jsonify
import openai

app = Flask(__name__)
openai.api_key = \"YOUR_KEY_HERE\"

@app.route('/')
def index():
    return render_template('index.html')

@app.route('/ai_help', methods=['POST'])
def ai_help():
    prompt = request.json.get('prompt','')
    try:
        resp = openai.ChatCompletion.create(
            model='gpt-3.5-turbo',
            messages=[
                {'role':'system','content':'तुम helpful कोड असिस्टेंट हो'},
                {'role':'user','content':prompt}
            ]
        )
        return jsonify({'code_suggestion': resp.choices[0].message.content})
    except Exception as e:
        return jsonify({'code_suggestion': f'❌ Error: {e}'})

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=int(os.environ.get('PORT', 3000)))" > main.py

# requirements.txt
echo "Flask==2.3.2
openai==1.14.2
gunicorn==20.1.0" > requirements.txt

# Procfile
echo "web: gunicorn main:app" > Procfile

# runtime.txt
echo "python-3.10.7" > runtime.txt

# templates/index.html
mkdir templates
echo "<!DOCTYPE html>
<html lang='en'>
<head>
  <meta charset='UTF-8'>
  <title>CodeBox AI</title>
  <script src='https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.5/codemirror.min.js'></script>
  <link rel='stylesheet' href='https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.5/codemirror.min.css'>
  <style>
    body, html { margin: 0; height: 100%; display: flex; }
    #editor { width: 50%; height: 100vh; }
    #output { width: 50%; height: 100vh; border: none; }
    .controls { position: absolute; top: 10px; left: 10px; z-index: 10; }
  </style>
</head>
<body>
  <div id='editor'></div>
  <iframe id='output'></iframe>
  <div class='controls'>
    <button onclick='runCode()'>🚀 Run</button>
    <button onclick='aiHelp()'>🤖 AI Help</button>
    <button onclick='exportCode()'>💾 Export</button>
  </div>
  <script>
    const editor = CodeMirror(document.getElementById('editor'), {
      value: '<!DOCTYPE html>\\n<html><body><h1>Hello World</h1></body></html>',
      mode: 'htmlmixed',
      lineNumbers: true
    });
    function runCode() {
      document.getElementById('output').srcdoc = editor.getValue();
    }
    async function aiHelp() {
      const promptText = prompt('AI से पूछिए:');
      if (!promptText) return;
      const res = await fetch('/ai_help', {
        method: 'POST',
        headers: { 'Content-Type':'application/json' },
        body: JSON.stringify({ prompt: promptText })
      });
      const data = await res.json();
      editor.setValue(editor.getValue() + '\\n\\n<!-- AI Suggestion:\\n' + data.code_suggestion + '\\n-->\\n');
    }
    function exportCode() {
      const blob = new Blob([editor.getValue()], { type: 'text/html' });
      const a = document.createElement('a');
      a.href = URL.createObjectURL(blob);
      a.download = 'code.html';
      a.click();
    }
  </script>
</body>
</html>" > templates/index.html
