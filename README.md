# Repositório de Aulas Práticas - Computação Quântica (Qiskit)

Este repositório reúne os notebooks usados nas aulas práticas da disciplina de Computação Quântica.

## Conteúdo

- `aula-prática-1-cq.ipynb`
- `projeto-simples-1-deutsch-jozsa-CQ.ipynb`

## Requisitos

- Python 3.10+
- pip atualizado

Arquivos de dependências no repositório:

- `requirements.in`: dependências diretas (editável pelos instrutores).
- `requirements.txt`: lockfile gerado automaticamente com versões travadas (usado pelos alunos).

## Instalação do ambiente

1. (Opcional, mas recomendado) criar e ativar um ambiente virtual:

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Instalar as dependências:

```bash
pip install -r requirements.txt
```

## Atualizar dependências (instrutores)

Quando for necessário atualizar versões para uma nova oferta da disciplina:

1. Edite o arquivo `requirements.in`.
2. Gere novamente o lockfile:

```bash
python -m pip install pip-tools
python -m piptools compile requirements.in -o requirements.txt
```

3. Teste os notebooks e faça commit dos dois arquivos.

## Como abrir os notebooks

1. Inicie o Jupyter:

```bash
jupyter lab
```

ou

```bash
jupyter notebook
```

2. Abra o notebook desejado.

## Uso no VS Code

1. Abra a pasta do repositório no VS Code.
2. Instale as extensões Python e Jupyter (caso ainda não tenha).
3. Com o ambiente virtual ativado e as dependências instaladas, abra um notebook.
4. No canto superior direito do notebook, clique em Select Kernel.
5. Escolha o interpretador Python do ambiente local (.venv).

### Verificação rápida no terminal

Para confirmar que o ambiente está correto:

```bash
python -c "import qiskit; import matplotlib; import numpy; print('Ambiente OK')"
```

Se esse comando funcionar, o kernel correto deve aparecer no VS Code.

## Solução de problemas comuns

- Erro ModuleNotFoundError: No module named 'qiskit':
- Ative o ambiente virtual e rode novamente pip install -r requirements.txt.
- Depois, no notebook, troque o kernel para o interpretador do .venv.
- Kernel não aparece no seletor:
- Execute python -m ipykernel install --user --name repo-aulas-cq --display-name "Python (repo-aulas-cq)".
- Feche e reabra o VS Code.
- Notebook abre com kernel errado:
- Use Command Palette -> Python: Select Interpreter e selecione o .venv.
- Reabra o notebook e selecione o mesmo kernel.

## Observações

- Se estiver usando VS Code, selecione o interpretador Python do ambiente virtual criado.
- Caso tenha problema com versão do Qiskit, verifique se o ambiente foi ativado antes da instalação.
