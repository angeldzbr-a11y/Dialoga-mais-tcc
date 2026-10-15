# Dialoga+

Plataforma educacional (TCC FAMETRO) para praticar situações de convivência escolar e receber feedback baseado na Comunicação Não Violenta (CNV).

- **Estudantes:** escolhem um tema, passam por 3 níveis de 4 situações e recebem um feedback educativo.
- **Professores:** criam salas privadas com código. Os alunos aparecem de forma anônima e as respostas não são exibidas.

## Estrutura

```
docs/   front-end (HTML, CSS e JavaScript) publicado no GitHub Pages
api/    API em Python com Flask (feedback pela IA, contas, salas e níveis)
```

## Como rodar no seu computador

```
cd api
python -m venv venv
venv\Scripts\activate        # Mac/Linux: source venv/bin/activate
pip install -r requirements.txt
$env:ANTHROPIC_API_KEY="sua_chave"     # Mac/Linux: export ANTHROPIC_API_KEY="sua_chave"
python app.py
```

Depois abra `docs/index.html` no navegador. A API fica em `http://127.0.0.1:5000/api/health`.

## Observações

- Os dados ficam na memória do servidor e são apagados quando ele reinicia (versão de demonstração, sem banco de dados).
- A chave da IA fica só no servidor, em variável de ambiente. Nunca a envie para o GitHub.
- Use apenas dados fictícios na demonstração.
