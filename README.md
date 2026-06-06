# nicho-bot

Construtor + simulador de chatbot de WhatsApp **pré-treinado por nicho**. MVP 100% client-side: um único `index.html`, sem servidor, sem chave de API, sem build, custo zero.

## O problema que resolve
Dor #2 do mercado: **PME perde lead no WhatsApp fora do horário.** O nicho-bot deixa o pequeno negócio montar, em minutos, um atendente virtual já treinado para o setor dele — respondendo dúvidas e capturando leads/agendamentos 24h.

## O que é (e o que NÃO é no MVP)
- **É:** um construtor de fluxo + simulador de conversa que gera um roteiro pronto e um arquivo de configuração (JSON).
- **NÃO é (ainda):** uma conexão real ao WhatsApp. Como não há servidor nem API paga no MVP, o produto não envia mensagens de verdade — ele entrega o bot **montado e testado** para você instalar depois.

## Como usar
1. Abra o `index.html` em qualquer navegador (duplo clique). Nada para instalar.
2. **Escolha o nicho** (Odontologia, Salão/Estética, Advocacia, Imobiliária, Restaurante/Delivery ou Genérico). Ele já vem com perguntas, respostas e tom de voz do setor.
3. **Edite** os pares pergunta→resposta, a mensagem de boas-vindas e o fallback. Adicione ou remova o que quiser.
4. **Teste no simulador** estilo WhatsApp à direita. Digite "horário", "preço" ou "quero agendar" para ver o fluxo de agendamento e a captura de lead (nome + contato + dia + horário).
5. **Exporte**: botão *Exportar JSON* (gera o arquivo de configuração que você entrega/instala) ou *Copiar roteiro* (texto legível do fluxo, ótimo para revisar com o cliente).
6. Tudo é salvo automaticamente no `localStorage` — não se perde ao recarregar.

## Modelo de negócio (sem investimento)
Você não precisa pagar nada para começar a vender:

- **Setup por nicho (one-time):** R$ 297–797 para montar e entregar o bot configurado do cliente. O nicho-bot faz o trabalho pesado; você só ajusta.
- **Mensalidade de manutenção:** R$ 49–149/mês para ajustar respostas, atualizar promoções e dar suporte. Receita recorrente.
- **Venda do template pronto:** empacote configurações por nicho (JSON) e venda como produto digital, escalável e sem custo marginal.
- **Combo:** setup + mensalidade é o de maior margem e fideliza.

Custo operacional do MVP: **zero** (roda no navegador do cliente / hospedagem estática grátis tipo GitHub Pages, Netlify).

## Roadmap
1. **MVP atual** — construtor + simulador + export (sem conexão real). ✅
2. **Painel multi-cliente** — gerenciar vários bots/nichos em um só lugar.
3. **Biblioteca de nichos** — mais segmentos e variações de tom.
4. **Integração real (quando houver receita):** conectar à **WhatsApp Cloud API oficial** (Meta) para envio/recebimento de mensagens de verdade, com webhook e número verificado.
5. **IA generativa opcional** — respostas dinâmicas via API quando o faturamento justificar o custo por token.

## Arquitetura
Arquivo único `index.html` com HTML, CSS e JS inline. Sem dependências externas. Persistência via `localStorage`. Export via `Blob` + download. Casamento de intenção por palavras-chave (gatilhos) com fallback configurável e máquina de estados simples para o fluxo de agendamento.
