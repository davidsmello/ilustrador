---
name: ilustrador
description: Gera desenhos e ilustrações analisando o contexto do projeto para escolher entre Gemini (padrão) e ChatGPT, usa o outro se o limite acabar, depois o Canva e por último SVG; o Canva também faz o acabamento (texto, logo, formatos). Use sempre que o usuário pedir um desenho, ilustração, imagem, arte, mascote, banner, capa, fundo ou ícone, ou pedir para "ilustrar" um site, landing page, apresentação, post ou projeto, mesmo que não cite Gemini nem ChatGPT. Use também quando, no meio de outra tarefa (criar um site, um deck), for preciso criar uma imagem nova. Não use para gráficos de dados, diagramas técnicos, nem para apenas editar ou redimensionar uma imagem que já existe.
---

# Ilustrador

O usuário quer que as imagens venham de uma IA geradora: Gemini ou ChatGPT, com o Canva de reserva. Desenhar por conta própria antes de tentar essas opções contraria o motivo desta skill.

Ordem: **IA mais indicada para o contexto → a outra → Canva → Claude (SVG)**. Na dúvida, a primeira é o Gemini. Cada pedido novo é analisado de novo, porque o contexto muda e os limites se renovam.

## 1. Entender o pedido

Descubra pelo contexto: onde a imagem vai ser usada, proporção (ex.: 16:9 para topo de site, 1:1 ou 4:5 para post), estilo, cores e marca, e se há texto dentro da imagem. Pergunte só o que não der para deduzir e mudaria muito o resultado. Se o projeto já tiver identidade visual (cores, logo, imagens), siga-a. Para sites, vale a consulta de referências que o usuário já usa (SEESAW).

## 2. Analisar o contexto e escolher a IA

Antes de escolher, leia o que o projeto no Claude já oferece: a conversa, as instruções e arquivos do projeto (`CLAUDE.md`, README, guia de marca), as imagens existentes e a memória, se houver. Leia só o necessário para saber o que é o projeto, para quem é, que estilo usa e onde a imagem vai entrar.

Ponto de partida para a escolha. São tendências, não fatos testados neste projeto, e os modelos mudam:

| O que o pedido mais exige | Primeira tentativa |
|---|---|
| Foto realista, produto, ambiente, pessoas | Gemini |
| Manter o mesmo personagem ou estilo de uma imagem de referência | Gemini |
| Texto legível dentro da imagem (cartaz, capa, rótulo) | ChatGPT |
| Muitos elementos com posições e instruções precisas | ChatGPT |
| Fundo transparente | ChatGPT |
| Nada disso se destaca | Gemini |

A experiência vale mais que a tabela: se o usuário pedir uma IA específica, use-a; se neste projeto uma delas já rendeu imagens aprovadas no mesmo estilo, continue com ela para manter a unidade visual.

Antes de gerar, diga em uma linha qual escolheu e por quê, e siga sem esperar resposta. Exemplo: "Vou de ChatGPT, porque a capa tem título escrito. Se preferir o Gemini, é só falar."

Enviar uma imagem de referência do projeto para a IA exige o OK do usuário antes.

## 3. Escrever o prompt

Um parágrafo descritivo: assunto, cena, estilo, paleta (com códigos hex quando conhecidos), composição, proporção, espaço livre para título se houver, e o que evitar. Peça sem texto na imagem, a menos que ele seja necessário, porque geradores costumam errar letras.

O prompt vai para um serviço externo: não coloque dados pessoais, senhas, nomes de clientes nem informação confidencial do projeto. Descreva o visual sem eles.

## 4. Gerar pelo Chrome

Use o Claude in Chrome (`mcp__claude-in-chrome__*`), no Claude Code ou no Cowork. Abra uma aba nova.

**Login:** antes de enviar o prompt, veja se a página já está conectada.

- Já conectada: use essa mesma sessão. Não saia da conta, não troque de conta e não peça novo login.
- Não conectada (tela de login ou botão "Entrar" no lugar da conta): avise qual serviço precisa de login, peça para a pessoa entrar na aba aberta e espere. A senha e os códigos de verificação são digitados por ela, nunca por você.
- Depois que ela disser que entrou, confira a página e continue de onde parou, com o mesmo prompt, sem pedir tudo de novo.

Isso vale mesmo que a página aceite uso sem conta, e vale para as duas IAs, cada uma quando chegar a vez dela. Falta de login não é motivo para passar à próxima IA.

Endereços: Gemini em https://gemini.google.com/app e ChatGPT em https://chatgpt.com.

1. **Primeira:** a IA escolhida no passo 2. Envie o prompt pedindo a geração da imagem e espere o resultado.
2. **Segunda:** a outra IA, só se o limite da primeira tiver acabado. Use o mesmo prompt.
3. **Canva:** só se os dois limites tiverem acabado. Gere pelo conector do Canva (seção "Canva" abaixo).
4. **Claude:** só se o Canva também não puder gerar (limite, recurso pago ou conector indisponível). Desenhe em SVG (ou HTML/CSS) e avise claramente que não veio de nenhuma das três.

**O que conta como limite esgotado:** a própria página diz que a cota, o limite de imagens ou de uso foi atingido, que é preciso esperar até certo horário, ou só oferece upgrade para continuar. Anote o horário de renovação, se aparecer. Não compre nem assine nada.

**O que não é limite:** página pedindo login, CAPTCHA, tela de termos, erro de carregamento, demora, ou recusa do conteúdo. Nesses casos não pule para a próxima IA em silêncio:

- Erro ou demora: tente mais uma vez; se persistir, conte ao usuário e pergunte se passa para a próxima.
- Login: siga a regra de login acima.
- CAPTCHA, termos: peça para a pessoa resolver na aba. Não aceite termos por ela.
- Recusa do conteúdo: mostre a mensagem e proponha um ajuste no prompt.

Se o Chrome não estiver disponível, avise e pergunte antes de usar outro caminho.

## Canva

Use o conector do Canva (ferramentas como `generate-image`, `create-design`, `edit-design`, `resize-design` e `export-design`), não o Chrome. Se não estiver conectado, avise, peça para a pessoa conectar o Canva e continue depois. Se algo exigir plano pago, diga e não assine nem compre.

Ele tem dois papéis:

- **Reserva de geração:** quando os limites do Gemini e do ChatGPT acabarem.
- **Acabamento:** só quando a peça precisar de texto, logo ou vários formatos (post, story, capa, banner). Primeiro a imagem base é aprovada; depois monte no Canva. Texto colocado ali sai correto e editável, então prefira gerar a imagem base sem texto. Use o kit de marca do grupo, se houver. Mostre o resultado e espere novo OK antes de exportar.

**Confira o logo antes de mostrar.** O gerador de layout do Canva pode cortar ou alterar o logo enviado (já aconteceu de sobrar só o ícone, sem as letras). Olhe a miniatura e compare com o arquivo oficial: todas as partes presentes, mesmas cores, sem distorção. Se estiver errado, apague o elemento e insira o arquivo oficial inteiro, mantendo a proporção original, e confira de novo. Depois de exportar, abra o arquivo final e confira mais uma vez.

Assim, escolher o ChatGPT por causa de texto (passo 2) só faz sentido quando o texto precisa fazer parte do próprio desenho. Uma ilustração simples não passa pelo Canva. Publicar ou compartilhar um design exige pedido do usuário.

## 5. Mostrar e esperar o OK

Mostre o resultado (captura de tela da imagem) e diga qual IA gerou. Se não ficou bom, peça o ajuste na mesma conversa da IA, lembrando que cada geração gasta limite.

Nada é aplicado no site ou projeto antes do OK. Como baixar arquivo também precisa de autorização, pergunte as duas coisas juntas, informando nome do arquivo, origem e tamanho (ou que o tamanho não aparece). Exemplo: "Gerada no Gemini. Aprova? Se sim, baixo `hero.png` (gemini.google.com, tamanho não informado) e coloco no topo do site."

No caso do SVG feito pelo Claude, mostre antes e só aplique depois do OK; não há download.

## 6. Aplicar

Depois do OK, baixe pelo botão de download da própria página, mova para a pasta de imagens do projeto (ou `imagens/` se não houver) com um nome descritivo, e insira onde combinado, com texto alternativo no caso de site. Nunca sobrescreva uma imagem existente sem perguntar.

Termine informando: qual IA gerou, se passou pelo Canva (com o link do design), onde o arquivo ficou, e se algum limite acabou (e quando renova, se a página disse).
