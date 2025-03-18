# DocuGen AI 🤖📄

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![HuggingFace](https://img.shields.io/badge/Model-Mistral--7B--Instruct-orange)

**DocuGen AI** é uma ferramenta de automação de documentação que utiliza IA para transformar repositórios de código em documentação clara e organizada. Ideal para desenvolvedores que desejam manter seus projetos bem documentados sem esforço manual.

---

## Funcionalidades Principais 🚀

- **Clonagem Automática de Repositórios**: 
  - Clona repositórios Git diretamente para análise.
- **Processamento com IA**:
  - Usa o modelo **Mistral-7B-Instruct** (4-bit quantizado) para gerar documentação contextual.
- **Resumo Inteligente de Código**:
  - Analisa os primeiros 10 linhas de cada arquivo `.py` para extrair contexto relevante.
- **Geração de README.md**:
  - Cria um arquivo `README.md` estruturado com seções como introdução, funcionalidades e exemplos.
- **Otimizado para Performance**:
  - Suporta até **4096 tokens** de contexto (equivalente a ~3000 palavras).

---

## Pré-requisitos 📋

- Python 3.8+
- Git
- 5 GB de espaço livre (para o modelo Mistral-7B)
- Bibliotecas: `gitpython`, `llama-cpp-python`, `matplotlib`

---

## Instalação ⚙️

```bash
# Clonar o repositório
git clone https://github.com/Ronbragaglia/DocuGen-AI.git
cd DocuGen-AI

# Instalar dependências
pip install gitpython llama-cpp-python matplotlib

# Nota: O modelo Mistral-7B será baixado automaticamente na primeira execução (~4.1 GB).

Como Usar 🛠️

Via Linha de Comando (CLI)
python docugen.py --repo https://github.com/seu-usuario/seu-repositorio.git

Personalização (Exemplo em Python)

from docugen import gerar_documentacao

documentacao = gerar_documentacao(
    repo_url="https://github.com/seu-usuario/seu-repositorio.git",
    modelo_personalizado="caminho/para/seu-modelo.gguf"
)
print(documentacao)

Estrutura do Projeto 📂
DocuGen-AI/
├── modelos/               # Modelos de IA baixados
├── meu_repositorio/       # Repositórios clonados
├── docugen.py             # Código principal
├── README.md              # Documentação gerada
└── requirements.txt       # Dependências

Personalização 🔧
1. Ajuste o Prompt
Modifique criar_prompt_inicial() em docugen.py para incluir instruções específicas:
prompt = "Gere uma documentação técnica em português com foco em arquitetura do sistema."

2. Altere o Resumo de Código
def summarize_code(code, max_lines=20): ...

3. Experimente com Modelos
Substitua o modelo padrão por outros GGUF compatíveis do Hugging Face:
modelo_url = "https://huggingface.co/TheBloke/Mixtral-8x7B-Instruct-v0.1-GGUF/resolve/main/mixtral-8x7b-instruct-v0.1.Q4_K_M.gguf"

Contribuição 🤝
Faça um Fork do projeto

Crie uma Branch (git checkout -b feature/nova-feature)

Commit suas Mudanças (git commit -m 'Adicionei uma feature incrível')

Push para a Branch (git push origin feature/nova-feature)

Abra um Pull Request

Licença 📜
Este projeto está licenciado sob a MIT License.

Contato 📧
Autor: Ronbragaglia

GitHub: Ronbragaglia

Projeto: DocuGen-AI

Feito com ❤️ e Python. Contribuições são sempre bem-vindas! 🚀



