# Agenda Diária — Timeline Planner

Interface moderna de **agenda diária** inspirada em timeline vertical. Adicione, edite e visualize eventos com ícones por categoria, detecção de conflitos de horário e persistência automática no navegador.

> **Stack:** HTML + CSS + JavaScript (puro).  
> **Persistência:** `localStorage` (sem back-end).  
> **Status:** MVP funcional.

---

## ✨ Recursos

- Linha do tempo vertical com **cartões** de eventos.
- **Adicionar/editar/excluir** eventos.
- **Conflito de horário** com 3 opções:
  1. Adicionar assim mesmo  
  2. Substituir conflito(s)  
  3. Sugerir novo horário
- **Categorias** com ícones (sono, acordar, tarefa, trabalho, compromisso, social, caminhada, academia, sauna, banho gelado, refeição).
- **Navegação de data** (◀/▶ e seletor de data).
- **Filtro por categoria**.
- **Exportar/Importar** JSON (backup/restore).
- **Carregar amostra** (preenche o dia com exemplos).
- **Persistência automática**: seus eventos ficam salvos mesmo fechando o navegador/computador.
- UI responsiva e tema escuro.

---

## 🖥️ Como rodar localmente

> Não há build. É um site estático.

1. Baixe/clonar o projeto.
2. Abra `index.html` em um navegador **ou** sirva a pasta com um servidor estático (recomendado para evitar bloqueios de alguns navegadores):
   - Python:
     ```bash
     python -m http.server 5500
     # depois acesse http://localhost:5500
     ```
   - Node (http-server):
     ```bash
     npx http-server -p 5500
     ```

### Deploy no GitHub Pages

1. Faça push do conteúdo para a branch `main` (ou `docs`).
2. Em **Settings → Pages**, selecione a branch e a pasta raiz.
3. Aguarde a publicação e acesse a URL gerada.

---

## 🧠 Como usar

- Clique em **“+ Adicionar evento”** e informe: título, data, início, fim, categoria e (opcional) descrição.
- Se houver choque de horário, escolha: **Adicionar mesmo assim**, **Substituir** ou **Sugerir novo horário**.
- Use **⋯** para **Exportar** (gera `.json`), **Importar** (lê `.json`), **Carregar amostra** e **Limpar dia**.
- **Esc** fecha o menu contextual.

---

## 🔒 Persistência dos dados

- Os dados são salvos no `localStorage` do navegador com a chave `agendaDataV1`.
- Isso garante que tudo continue lá ao fechar/reabrir o site, inclusive após reiniciar o computador.
- Os dados são **por navegador e dispositivo**. Para migrar:
  1. No dispositivo de origem, use **Exportar**.
  2. No destino, use **Importar** e selecione o arquivo `.json`.

> Dica: evite abas anônimas/privadas se quiser manter os dados.

---

## 🗂️ Estrutura do projeto

