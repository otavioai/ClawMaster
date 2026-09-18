# Plano de 30 dias — Ouvert Estratégias

## Diagnóstico do desafio

O alvo declarado é USD 6.000/mês de receita recorrente em até 30 dias, partindo de capital zero. Três restrições estruturais moldam qualquer plano honesto para esse alvo:

1. **Identidade e recebimento.** Nenhuma conta de pagamento, domínio ou contrato pode ser aberto por um agente sem personalidade jurídica. Todo recebimento recai sobre a identidade de Otávio Berti e sobre os ativos já existentes (Stripe/PayPal/Mercado Pago verificados, domínio `ouvertestrategias.com.br` e hospedagem pagos, conforme informado).
2. **Distribuição.** O grupo de LinkedIn (9.573 membros) foi classificado pelo próprio Otávio como "adormecido, considere quase zero". Isso descarta qualquer plano que dependa de alcance orgânico rápido; o motor de aquisição precisa ser prospecção direta e pessoal, não conteúdo esperando alcance.
3. **Capacidade computacional.** O hardware disponível (Ryzen AI 7 350, 16 GB RAM, GPU integrada Radeon 860M) não sustenta um negócio de hospedagem de modelos ou revenda de capacidade de inferência em escala comercial. Isso descarta a rota "monetizar compute ocioso" como caminho principal.

Dado isso, o modelo de negócio de maior probabilidade de sucesso não é um produto de software com autoatendimento, que dependeria de audiência e tempo de maturação que o prazo não permite, mas um **serviço de consultoria de alto ticket, ancorado na credibilidade profissional já existente de Otávio como consultor financeiro/estratégico**, vendido por prospecção direta. Este é o ativo mais valioso disponível e o único que pode gerar receita em dias, não em meses.

## Calibração da meta

Fechar o equivalente a USD 6.000/mês recorrentes em 30 dias, do zero, sem audiência ativa, exigiria aproximadamente 2 a 3 contratos de assessoria contínua fechados via prospecção fria/morna dentro do mês. [Inference] Isso está no extremo otimista do que consultores individuais relatam como ciclo de venda para ticket alto em B2B, mesmo com produto validado e rede ativa. Não há dado verificável que sustente uma probabilidade específica de atingir esse número neste prazo exato — é uma meta agressiva, não uma projeção. [Speculation encerrada]

Marcos intermediários mais úteis para acompanhar nas próximas semanas, em vez do número final isolado:

| Semana | Marco | Sinal de que o motor funciona |
|---|---|---|
| 1 | Página no ar, lista de 30–50 contatos qualificados, primeiras 15 mensagens de prospecção enviadas | Taxa de resposta > 0 |
| 2 | 5–10 conversas realizadas, 2–4 diagnósticos vendidos (R$ 3.500 cada) | Primeira receita em caixa |
| 3 | Diagnósticos entregues, 1–2 propostas de assessoria contínua apresentadas | Conversão diagnóstico → assessoria > 0 |
| 4 | 1–3 contratos de assessoria contínua assinados | MRR real, ainda que abaixo da meta |

Se ao fim da semana 2 a taxa de resposta às mensagens de prospecção estiver perto de zero, o problema não é o produto, é o canal ou a lista de contatos — ajustar ali antes de insistir na mesma abordagem.

## Estrutura da oferta

- **Diagnóstico Estratégico-Financeiro** — R$ 3.500, pagamento único, entrega em 2 semanas. Produto de entrada, autoatendimento via link de pagamento, baixo atrito.
- **Assessoria Contínua Ouvert** — a partir de R$ 9.000/mês, escopo fechado após conversa. Produto principal de receita recorrente; vendido depois do diagnóstico, nunca antes.

Com 1 diagnóstico convertendo em 1 assessoria de R$ 9.000/mês, faltam ainda cerca de 2 assessorias adicionais (ou tickets maiores) para alcançar o equivalente a USD 6.000. Isso é factível apenas se o funil de prospecção gerar volume suficiente de conversas qualificadas nas duas primeiras semanas — daí a prioridade em enviar mensagens de prospecção já nos primeiros dias, e não esperar a página "estar perfeita".

## O que já foi construído nesta sessão

- `site/index.html` — página comercial no sistema visual da Ouvert (cores, tipografia e tom de voz extraídos do design system já existente), com as duas ofertas e formulário de contato por e-mail.
- `docs/scripts-prospeccao.md` — roteiros de mensagem para LinkedIn, Instagram e e-mail frio, prontos para personalização.

## O que só Otávio pode fazer

1. **Publicar a página.** Fazer o deploy de `site/index.html` no domínio `ouvertestrategias.com.br` (ou em um subdomínio como `oferta.ouvertestrategias.com.br`), conforme a hospedagem já paga permitir.
2. **Criar o link de pagamento.** Gerar um Payment Link recorrente (para a assessoria, se decidir automatizar a cobrança) e um link de pagamento único de R$ 3.500 (para o diagnóstico) no Stripe, Mercado Pago ou PayPal, e substituir o placeholder `data-payment-link-pendente` em `site/index.html` pela URL real.
3. **Preencher a seção "Sobre a Ouvert".** O parágrafo de credenciais foi deixado como placeholder marcado — não preenchi com dado inventado. Precisa da trajetória real (formação, anos de atuação, setores atendidos).
4. **Montar a lista de prospecção.** 30 a 50 contatos reais e qualificados: membros específicos do grupo de LinkedIn com perfil de decisor em empresa de médio porte, contatos de rede pessoal, ex-clientes ou ex-colegas em posições relevantes. Isso não pode ser feito por mim sem acesso às contas.
5. **Enviar as mensagens.** Os roteiros estão prontos; o envio precisa partir da conta pessoal/profissional de Otávio, uma a uma, personalizada pelo nome e contexto de cada contato — mensagem em massa idêntica tende a converter pior e pode violar termos de uso do LinkedIn.
6. **Conduzir as conversas de venda.** Nenhuma ferramenta automatiza a conversa que fecha um contrato de assessoria de R$ 9.000/mês; isso depende da conversa direta de Otávio com o decisor.

## O que eu posso continuar fazendo

- Ajustar copy, preços e estrutura da página conforme feedback do mercado.
- Escrever ou revisar propostas comerciais e materiais de apoio para as conversas de venda.
- Construir o painel de indicadores (`KpiTile`, `DataTable` do design system) como ferramenta de entrega da assessoria contínua, se e quando houver o primeiro cliente.
- Analisar dados que Otávio compartilhar (planilhas, contratos de dívida, DRE) para montar os diagnósticos com mais eficiência.
