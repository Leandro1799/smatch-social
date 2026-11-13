# Mapa de funcionalidades do Smatch

O que o app faz hoje, tela por tela, para uso do marketing. A fonte é o **código do app**
(repositório `Leandro1799/smatchbeach`, commit `fc7fb93e`, de 12/11/2026), não o que está
planejado nem o que já foi dito em divulgação. As telas citadas estão na biblioteca ao lado
([README.md](README.md), pasta [`2026-11-13/`](2026-11-13/)).

## Como ler

Cada funcionalidade traz: onde fica, para que serve, o passo a passo com os nomes reais
dos botões, para quem é, o que é grátis e o que é pago, o status e as telas que a mostram.

**Status**

- **No ar** — está no código publicado e qualquer usuário alcança.
- **Em teste** — está no código, mas depende de algo que ainda não está ligado ou só
  aparece para administradores.
- **Planejado** — não existe no código. Só aparece na seção [Planejado](#14-planejado).

Antes de divulgar qualquer coisa, leia também a seção
[Cuidados na divulgação](#15-cuidados-na-divulgação): ela lista o que parece pronto e não está.

**Barra de baixo do app:** Home · Torneios · Arenas · Match · Coringa · Desafios · Ranking.
No topo ficam o sino, as mensagens e o menu do avatar.

## Preços (o que o código cobra)

| O quê | Preço | Quem paga |
|---|---|---|
| Usar o app como jogador (perfil, desafios, coringa, match, ranking, ITF, arenas) | Grátis | — |
| **Premium** | R$ 9,90 por mês | Jogador |
| **Plano Arena** | R$ 99,90 por mês (era R$ 49,90 até 12/11/2026) | Dono de arena |
| **Plano Arena Gestão** | R$ 300,00 por mês | Dono de arena |
| Inscrição em torneio cobrada pelo app | R$ 1,00 do Smatch + R$ 0,99 do Pix = **R$ 1,99 por inscrição paga** | Organizador (sai do valor da inscrição; o atleta paga só o preço anunciado) |
| Criar e organizar torneio, com inscrição grátis ou paga fora do app | Grátis | — |
| Day Use, aula e aluguel de quadra | O valor é da arena e é pago direto a ela; o Smatch não recebe nem cobra nada | Jogador → arena |

**Atenção ao nome do plano de R$ 300.** No app existem dois planos de arena. O de
R$ 300,00 por mês chama-se **Plano Arena Gestão** (aulas, aluguel de quadra e painel
completo). O **Plano Arena**, sem "Gestão", custa R$ 99,90 por mês. Em material de
divulgação, "Plano Arena R$ 300" deve virar "Plano Arena Gestão R$ 300".

Os dois planos de arena já incluem o Premium do dono. Nos apps de iPhone e Android as
assinaturas são vendidas pelas lojas. O Plano Arena Gestão foi cadastrado nas duas lojas a
R$ 300,00 e o Plano Arena a R$ 99,90 (Android desde 12/11/2026; iPhone a partir de
14/11/2026). O preço de loja do Premium não está no código e deve ser conferido no App
Store Connect e no Google Play Console antes de ser divulgado.

---

## 1. Conta e acesso

### Criar conta e entrar
- **Onde fica:** tela de entrada do app (`/auth`).
- **Para que serve:** entrar no Smatch e guardar seu perfil, seus jogos e seus resultados.
- **Como usar:**
  1. Informe e-mail e senha, ou toque em **Continuar com Google**. No iPhone também há **Continuar com Apple**.
  2. Se tiver um convite, preencha **Código de convite (opcional)**.
  3. Toque em **Entrar na quadra**. Quem esqueceu a senha usa **Esqueci minha senha**.
- **Para quem:** todos.
- **Grátis ou pago:** grátis.
- **Status:** no ar. Idade mínima de 14 anos.
- **Telas:** —

### Primeiro acesso por papel
- **Onde fica:** logo depois de criar a conta.
- **Para que serve:** dizer como você vai usar o app, para ele mostrar só o que interessa.
- **Como usar:**
  1. Em **Como você vai usar o Smatch?**, marque **Atleta**, **Dono ou gestor de arena** e/ou **Árbitro** (pode marcar mais de um).
  2. Preencha os dados que cada papel pede.
  3. Quem marcou arena termina em **Cadastrar minha arena**.
- **Para quem:** jogador, arena e árbitro.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** —

### Ver o app sem conta
- **Onde fica:** qualquer link do app aberto sem login.
- **Para que serve:** conhecer o app antes de se cadastrar.
- **Como usar:** sem conta dá para ver a Home pública, Torneios e a página de cada torneio, Circuitos, Ranking, ITF, perfis de jogadores, Arenas, Day Use, páginas de turma e a grade de horários das quadras. As abas **Match**, **Coringa** e **Desafios** abrem **Crie sua conta grátis**.
- **Para quem:** visitante.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** —

### Verificação em duas etapas
- **Onde fica:** Perfil › **Editar** › **Verificação em duas etapas**.
- **Para que serve:** proteger a conta com um código do celular além da senha.
- **Como usar:**
  1. Toque em **Ligar verificação em duas etapas**.
  2. Leia o código com um aplicativo autenticador e confirme.
  3. Guarde os códigos de recuperação.
- **Para quem:** todos.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** —

### Idioma
- **Onde fica:** menu do avatar › **Idioma**; também na tela de entrada.
- **Para que serve:** usar o app em português, inglês ou espanhol.
- **Para quem:** todos.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** —

### Excluir a conta
- **Onde fica:** Perfil › **Editar** › **Zona de perigo**.
- **Para que serve:** apagar a conta e os dados.
- **Como usar:** **Excluir minha conta** › **Excluir definitivamente**. Quem tem assinatura comprada no Google Play precisa cancelar antes.
- **Para quem:** todos.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** —

---

## 2. Home

### Home
- **Onde fica:** aba **Home**.
- **Para que serve:** ver num lugar só o que está acontecendo: torneios ITF ao vivo, arenas da sua cidade, sua dupla, coringa e o que os amigos fizeram.
- **Como usar:** a tela traz, de cima para baixo:
  1. Faixa de destaques.
  2. **ITF ao vivo**, com **Ver todos**.
  3. **Arenas**, com **Perto de mim** e **Ver todas**; o dono de arena vê **Gerenciar minha arena**.
  4. **Sua dupla**: alterna **Mesmo gênero** / **Mista**. Sem dupla, **Buscar parceiro agora** e a chave **Aparecer para outros**. Com dupla, **Desafiar dupla** e **Ver detalhes**.
  5. Coringa e desafios pendentes.
  6. **Atividade da comunidade**, com **Ver feed completo**.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** [`home-inicio`](2026-11-13/home-inicio.png)

---

## 3. Match, amigos e mensagens

### Match social
- **Onde fica:** aba **Match** › **Social** (o título da tela é "Amigos").
- **Para que serve:** conhecer gente do beach tennis na sua cidade, para amizade, namoro ou networking.
- **Como usar:**
  1. Em **Ative o match social**, toque em **Configurar**.
  2. Escolha **Amizade**, **Namoro** ou **Networking**, gênero, faixa de idade e cidade.
  3. Nos cartões, **Passar** ou **Curtir**.
  4. Quando os dois curtem, a conversa abre.
  5. **Já vi** › **Trazer de volta** recupera quem você passou.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis. No Premium, **Te curtiram** mostra quem curtiu você (no grátis as fotos aparecem borradas) e o perfil sobe na fila.
- **Status:** no ar. Só entra quem liga a opção; **Namoro** é só para maiores de 18.
- **Telas:** —

### Busca de dupla
- **Onde fica:** aba **Match** › **Dupla**. Também em Home › **Buscar parceiro agora** (tela "Parceiros", com **Descobrir** / **Aceitos** / **Recusados**).
- **Para que serve:** achar parceiro da sua categoria para jogar e disputar torneio.
- **Como usar:**
  1. Abra **Match** › **Dupla**.
  2. Veja o cartão: categoria, lado, mão, estilo e dias em que joga.
  3. **Passar**, **Curtir** ou **Conversa**. Tocar no cartão abre o perfil.
  4. Com curtida dos dois, vira match e a conversa abre.
  5. Em Home › **Sua dupla**, toque em **Formar dupla**.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis. No Premium o perfil sobe na fila e **Onde tá rolando** mostra as arenas com gente ativa.
- **Status:** no ar. Mostra só jogadores da mesma categoria; cada pessoa tem uma dupla de mesmo gênero e uma mista.
- **Telas:** [`match-busca-de-dupla`](2026-11-13/match-busca-de-dupla.png), [`match-card-de-perfil`](2026-11-13/match-card-de-perfil.png)

### Amigos
- **Onde fica:** Perfil › **Visão pública** › abas **Amigos** / **Buscar Dupla** (menu do avatar › **Amigos**).
- **Para que serve:** adicionar quem você conhece e acompanhar os jogos deles.
- **Como usar:**
  1. Em **Buscar jogador pelo nome**, digite o nome. A busca ignora acento ("matias" acha "Matías").
  2. Toque em **Adicionar**.
  3. A outra pessoa responde com **Aceitar** ou **Recusar**.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** —

### Mensagens
- **Onde fica:** ícone de mensagens no topo (`/chat`, "Mensagens").
- **Para que serve:** combinar jogo com amigos e matches.
- **Como usar:** abra a conversa e escreva. Convite de coringa chega como cartão com **Aceitar** / **Recusar** e vale por 24 horas.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar. Só texto, e só entre amigos ou matches de dupla.
- **Telas:** —

### Sino de pendências
- **Onde fica:** sino no topo.
- **Para que serve:** ver o que está esperando uma resposta sua.
- **Como usar:** toque no sino e depois no item. Aparecem desafio recebido, placar para validar, pedido de vaga em turma, pagamento de reserva informado e avisos de aula (cancelada ou de volta).
- **Para quem:** jogador, professor e arena.
- **Grátis ou pago:** grátis.
- **Status:** no ar. É uma lista de pendências, não um histórico. **Não existe notificação push**: o aviso só aparece dentro do app.
- **Telas:** [`arenas-avisos`](2026-11-13/arenas-avisos.png)

---

## 4. Perfil e estatísticas

### Perfil do jogador
- **Onde fica:** menu do avatar › perfil (`/perfil`), com **Visão pública** e **Editar**. Os outros veem em `/jogador/…`.
- **Para que serve:** mostrar quem você é na quadra: categoria, lado, mão, estilo, arenas, ranking e desempenho.
- **Como usar:**
  1. Em **Editar**, preencha os dados, a foto e até 8 fotos extras.
  2. Escolha até 5 em **Arenas onde você joga**.
  3. Marque ou não **Mostrar minha faixa etária no perfil** (a idade exata nunca aparece).
  4. Em **Meu cartão**, o ícone de compartilhar gera uma imagem do perfil.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** [`perfil-jogador`](2026-11-13/perfil-jogador.png), [`match-card-de-perfil`](2026-11-13/match-card-de-perfil.png)

### Perfil verificado
- **Onde fica:** Perfil › **Editar** › **Solicitações** › **Perfil verificado**.
- **Para que serve:** ganhar o selo **Verificado** ao lado do nome.
- **Como usar:** **Ativar perfil verificado** › informe o número do documento › **Confirmar e ativar**.
- **Para quem:** jogador.
- **Grátis ou pago:** só para assinantes Premium (R$ 9,90 por mês) ou donos de arena com plano.
- **Status:** no ar. O selo é ativado na hora; o documento informado não é conferido por ninguém. Evite prometer "identidade checada".
- **Telas:** [`perfil-jogador`](2026-11-13/perfil-jogador.png)

### Estatísticas
- **Onde fica:** Perfil › **Ver estatísticas completas** (`/estatisticas`).
- **Para que serve:** acompanhar sua evolução.
- **Como usar:** a tela mostra **Evolução do Ranking**, **Win Rate Geral**, **Resultado por Fase**, **Pontos: Válidos vs Expirando**, **Frequência de Jogos**, **Categorias Jogadas** e **Confrontos**.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** [`desafios-estatisticas`](2026-11-13/desafios-estatisticas.png)

### Vincular perfil ITF
- **Onde fica:** cartão **Você joga o circuito ITF?** no Perfil.
- **Para que serve:** ligar sua conta ao seu registro de jogador da ITF.
- **Como usar:**
  1. **Vincular perfil ITF**.
  2. Busque em **Seu nome como aparece na ITF...**.
  3. Preencha **Como podemos confirmar? (opcional)** e toque em **Pedir vínculo**.
  4. Fica como **Pedido em análise** até o Smatch aprovar.
- **Para quem:** só jogador da categoria PRO ou professor aceito por uma arena.
- **Grátis ou pago:** grátis.
- **Status:** no ar. A aprovação é manual. Com o vínculo, o perfil mostra o ranking ITF, os jogos do circuito entram em **Confrontos**, aparece **Meus jogos** (vídeos) e o professor ganha o selo **Rankeado ITF**.
- **Telas:** —

### Importar torneios da LetzPlay
- **Onde fica:** Torneios › **Meus** › **Importar torneios da Letzplay**; Perfil › **Importar torneios**.
- **Para que serve:** trazer para o Smatch o histórico de torneios que você jogou na LetzPlay.
- **Como usar:**
  1. Informe **Nome Usuário Plataforma** e aceite o **Termo de Importação**.
  2. **Abrir meu perfil na LetzPlay**, copie a página de torneios, cole e toque em **Importar o que colei** (ou **Tentar importação automática**).
  3. Use **Remover em aberto** para tirar os que você não jogou.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar. O histórico alimenta o perfil, as estatísticas e os pontos do ranking local.
- **Telas:** —

---

## 5. Desafios

### Desafios
- **Onde fica:** aba **Desafios**, com **Para você** / **Enviados** / **Confirmados** / **Validar** / **Histórico**.
- **Para que serve:** chamar alguém para um jogo, registrar o placar e guardar o histórico.
- **Como usar:**
  1. Toque em **Desafiar alguém** para abrir **Novo desafio**.
  2. Em **Tipo de jogo**, escolha **1 vs 1** ou **Dupla**.
  3. Em **Formato do jogo**, escolha **1 Set + Tie break**, **2 Sets + Super TB** ou **Só tie-break**. No tie-break, **Até quantos pontos**: **7**, **10** ou **Outro** (de 1 a 30).
  4. Escolha o adversário, a data, a arena e um **Recado (opcional)**; toque em **Enviar desafio**.
  5. O adversário responde com **Aceitar** ou **Recusar**.
  6. Depois do jogo, **Informar placar**. O outro lado confere em **Validar**, com **Confirmar** ou **Contestar**.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar. O formato **Só tie-break** entrou em 12/11/2026. Desafio não dá pontos de ranking; conta vitórias e derrotas no perfil. Em **Quem pode me desafiar** o jogador escolhe **Qualquer um**, **Minha categoria ou acima (e amigos)**, **Só amigos** ou **Ninguém**.
- **Telas:** [`desafios-criar`](2026-11-13/desafios-criar.png), [`desafios-resultado`](2026-11-13/desafios-resultado.png), [`desafios-historico`](2026-11-13/desafios-historico.png), [`desafios-estatisticas`](2026-11-13/desafios-estatisticas.png)

---

## 6. Coringa

### Coringa
- **Onde fica:** aba **Coringa**, com **Disponíveis** / **Chamadas** / **Árbitros** / **Minha disp.**
- **Para que serve:** completar o jogo quando falta alguém, ou se oferecer para completar o jogo dos outros.
- **Como usar:**
  1. **Para chamar:** **Chamadas** › **Publicar chamada** › preencha data, horário de início, período, categoria, arena, cidade e mensagem › **Publicar**.
  2. **Para se candidatar:** numa chamada aberta, toque em **Candidatar-me**.
  3. **Para convidar alguém:** **Disponíveis** › **Convidar** › **Enviar convite**. Também há **Desafiar** e **WhatsApp**.
  4. **Para se oferecer:** **Minha disp.** › ligue **Habilitar como coringa**, marque dias, períodos, categorias e arenas › **Salvar disponibilidade**.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** [`coringa-disponiveis`](2026-11-13/coringa-disponiveis.png), [`coringa-chamadas`](2026-11-13/coringa-chamadas.png)

### Árbitros
- **Onde fica:** para se cadastrar, primeiro acesso (papel **Árbitro**) ou Perfil › **Sou árbitro**. Para achar um, Coringa › **Árbitros**.
- **Para que serve:** o árbitro se apresenta; o organizador encontra árbitro para o torneio.
- **Como usar:**
  1. O árbitro marca **Sou árbitro**, escolhe o **Nível de experiência** (E a PRO), marca **Tenho certificado ITF** se tiver e toca em **Salvar árbitro**.
  2. O organizador abre Coringa › **Árbitros** e toca em **Convidar para meu torneio**.
- **Para quem:** árbitro e organizador.
- **Grátis ou pago:** grátis.
- **Status:** no ar. O cadastro é uma declaração do próprio árbitro; ninguém confere o certificado. Pagamento do árbitro pelo app não existe.
- **Telas:** —

---

## 7. Torneios (para o jogador)

### Lista de torneios
- **Onde fica:** aba **Torneios**, com **Locais** / **ITF** / **Meus** (a tela abre em **ITF**).
- **Para que serve:** achar torneio para jogar.
- **Como usar:**
  1. Toque em **Locais**.
  2. Alterne **Abertos** / **Encerrados**.
  3. Filtre por **Torneio** / **Rankings** / **Super 8**, categoria, cidade, formato, período e modalidade. **Limpar filtros** desfaz.
  4. Toque no torneio para abrir a página dele.
- **Para quem:** jogador; funciona sem conta.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** [`torneios-lista`](2026-11-13/torneios-lista.png)

### Inscrição em torneio
- **Onde fica:** página do torneio › **Inscrever-se**.
- **Para que serve:** garantir a vaga, sozinho ou com parceiro.
- **Como usar:**
  1. **Inscrever-se** › em **Confirmar inscrição**, informe **WhatsApp para contato**, o tamanho da camiseta se o torneio pedir e **Meu parceiro** nas duplas.
  2. Torneio grátis, ou com pagamento combinado com o organizador: a inscrição já fica confirmada.
  3. Torneio cobrado pelo app: **Confirme seu CPF** (aceita **Cupom de desconto**) › **Continuar pro pagamento**.
  4. Em **Pague via PIX**, use o QR code ou **Copiar código**.
  5. Se não pagar na hora, o cartão **Você tem 1 pagamento pendente** fica na página do torneio e na Home, com **Ver PIX**. A vaga só é garantida quando o pagamento entra.
- **Para quem:** jogador.
- **Grátis ou pago:** o atleta paga exatamente o valor anunciado pelo organizador, sem taxa por cima. Pelo app, **só Pix** (não há cartão). Nas duplas, cada um paga a sua parte; o parceiro recebe o convite **Aceitar e me inscrever**.
- **Status:** no ar. Torneio lotado oferece **Entrar na fila de espera**. Se o organizador cancela o torneio ou a categoria, o atleta recebe o valor inteiro de volta. Se o próprio atleta cancela uma inscrição já paga, **não há devolução automática**.
- **Telas:** [`torneios-inscricao`](2026-11-13/torneios-inscricao.png), [`torneios-inscricao-pix`](2026-11-13/torneios-inscricao-pix.png)

### Chave e resultados
- **Onde fica:** página do torneio › **Chaveamento**.
- **Para que serve:** acompanhar os jogos, os placares e quem avançou.
- **Como usar:**
  1. Abra o torneio e toque em **Chaveamento**.
  2. Navegue pelas fases (**Quartas**, **Semifinal**, **Final**).
  3. Em cada jogo, **Compartilhar** gera a arte do confronto para postar.
  4. **Premiação** mostra o campeão e o vice.
- **Para quem:** jogador e público.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** [`torneios-chave`](2026-11-13/torneios-chave.png)

### Super 8
- **Onde fica:** página do torneio › **Jogos**.
- **Para que serve:** jogar no formato em que o parceiro muda a cada rodada.
- **Como usar:**
  1. Em **Jogos**, toque no número da rodada.
  2. Veja em que quadra você joga, com quem e contra quem, e o placar de cada quadra.
  3. Toque em **Classificação** para ver a posição de cada jogador (vitórias, games a favor e saldo).
- **Para quem:** jogador.
- **Grátis ou pago:** conforme o torneio.
- **Status:** no ar.
- **Telas:** [`torneios-placar`](2026-11-13/torneios-placar.png), [`torneios-classificacao`](2026-11-13/torneios-classificacao.png)

### Ranking local
- **Onde fica:** aba **Ranking** › **Local**.
- **Para que serve:** ver quem são os melhores da sua categoria e onde você está.
- **Como usar:**
  1. Ranking › **Local**.
  2. Escolha **Masculino**, **Feminino** ou **Misto** e a categoria (PRO a E).
  3. Filtre pela cidade, ou toque em **Todos**; use **Buscar outra cidade...** e a busca por nome.
  4. Toque num jogador para ver o **Detalhamento dos pontos**.
- **Para quem:** jogador; funciona sem conta.
- **Grátis ou pago:** grátis.
- **Status:** no ar. Só pontuam os torneios do tipo **Torneio** (mata-mata) e os torneios importados da LetzPlay (os 6 melhores). Super 8, Ranking de duplas fixas, Copa por Equipes e desafios **não** dão pontos. O campeão leva de 50 a 800 pontos, conforme o número de inscritos na categoria; os pontos valem 12 meses.
- **Telas:** [`ranking-local-categoria`](2026-11-13/ranking-local-categoria.png), [`perfil-jogador`](2026-11-13/perfil-jogador.png)

### Circuitos
- **Onde fica:** carrossel **Circuitos** na aba Torneios.
- **Para que serve:** acompanhar uma série de torneios com classificação acumulada.
- **Como usar:** abra o circuito para ver **Etapas** e **Classificação do circuito**; **Seguir circuito** guarda nos seus.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar. Pontos fixos por etapa: campeão 100, vice 60, semifinal 30, quartas 15, oitavas 8, fase de grupos 4.
- **Telas:** —

---

## 8. Para o organizador de torneios

### Criar torneio
- **Onde fica:** aba **Torneios** › **Criar torneio**.
- **Para que serve:** montar um evento e abrir inscrições em poucos minutos.
- **Como usar:**
  1. **Criar torneio** › escolha o **Tipo de evento**: **Torneio**, **Ranking**, **Super 8** ou **Copa por Equipes**.
  2. Preencha **Nome do torneio**, **Data de início**, **Horário de início**, **Cidade** e **Arena / Local**.
  3. **Avançar** abre as etapas **Tipo de competição** › **Informações** › **Configuração** › **Inscrição**.
  4. Crie pelo menos uma categoria (PRO, A, B, C, D, Iniciante ou Open; masculino, feminino ou misto) e defina as vagas.
  5. Na linha do tempo do torneio, toque em **Publicado** › **Confirmar**.
- **Para quem:** organizador. Qualquer pessoa com conta pode criar.
- **Grátis ou pago:** grátis.
- **Status:** no ar. **Já organizou um evento parecido? Copiar de um anterior** reaproveita descrição, regulamento, capa, categorias e regras. Dá para ter um rascunho por vez.
- **Telas:** [`torneios-criacao-formato`](2026-11-13/torneios-criacao-formato.png), [`torneios-lista`](2026-11-13/torneios-lista.png)

### Formatos de competição
- **Onde fica:** na criação do torneio, em **Tipo de evento**.
- **Para que serve:** escolher como o evento é disputado.

| Formato no app | Como joga | Conta para o ranking local? | Status |
|---|---|---|---|
| **Torneio** — "Simples ou duplas, mata-mata" | Chave eliminatória em **Set único** ou **Melhor de 3**; opcional **Fase de grupos antes do mata-mata** | Sim | No ar |
| **Ranking** — "Duplas com parceiro fixo" | **Dupla fixa** e **Super 4/6/8 Duplas Fixas**: todas as duplas jogam entre si | Não | No ar |
| **Super 8** — "Duplas com parceiro rotativo" | **Super 8 Individual**, **Super 8 soma de X** e **Super 12 Individual** | Não | No ar |
| **Copa por Equipes** — "Equipes (fem + masc + mista)" | Cada confronto tem uma partida feminina, uma masculina e uma mista; equipes pré-definidas ou por sorteio | Não | No ar, ainda sem torneio real disputado |

- **Para quem:** organizador.
- **Grátis ou pago:** grátis.
- **Outros formatos:** **Rei da Praia** e temporadas de **Dupla Fixa** ficam em Torneios › **Meus** › **Outros formatos**. A temporada de Rei da Praia só é criada pela equipe do Smatch (**em teste**).
- **Telas:** [`torneios-criacao-formato`](2026-11-13/torneios-criacao-formato.png), [`torneios-chave`](2026-11-13/torneios-chave.png), [`torneios-placar`](2026-11-13/torneios-placar.png)

### Cobrar a inscrição pelo app
- **Onde fica:** criação do torneio › etapa **Inscrição** › **Valor da inscrição por atleta (R$)**.
- **Para que serve:** receber as inscrições por Pix sem controlar pagamento na mão.
- **Como usar:**
  1. Cadastre e confirme sua chave Pix.
  2. Informe o valor por atleta (grátis ou a partir de R$ 5,00) e escolha a cobrança **Via Smatch**.
  3. Ao publicar, confirme em **Publicar com cobrança pelo Smatch** › **Entendi, publicar**.
  4. Acompanhe em **Gestão financeira**; crie **Cupons e descontos** se quiser.
  5. Depois do torneio encerrado, o valor é repassado por Pix para a sua chave.
- **Para quem:** organizador (no Brasil, com chave Pix confirmada).
- **Grátis ou pago:** o Smatch fica com **R$ 1,00 por inscrição paga**, mais **R$ 0,99 do Pix**: **R$ 1,99 por inscrição**, descontados do valor que o organizador recebe. O atleta paga só o preço anunciado. Exemplo: inscrição de R$ 80,00 rende R$ 78,01 ao organizador. Torneio grátis e torneio com pagamento **Fora do Smatch** não têm taxa.
- **Status:** no ar. O repasse sai automaticamente depois do fim do torneio. Em cancelamento pelo organizador, o atleta recebe tudo de volta.
- **Telas:** [`torneios-inscricao`](2026-11-13/torneios-inscricao.png), [`torneios-inscricao-pix`](2026-11-13/torneios-inscricao-pix.png)

### Rodar o torneio
- **Onde fica:** página do torneio (o organizador vê os controles a mais).
- **Para que serve:** sortear, lançar resultados e divulgar.
- **Como usar:**
  1. **Gerar chaveamento** (com fase de grupos: **Sortear grupos** e depois **Gerar mata-mata**).
  2. Em cada jogo, **Definir horário** e **Lançar resultado**. Para ausência, **Alguém não compareceu ou desistiu?** › **Salvar W.O.**
  3. **Imprimir súmula** para levar à quadra.
  4. Em **Equipe**, chame **Co-org** e **Árbitro**.
  5. Em **Inscritos**: **Adicionar jogador**, **Trocar atleta**, **Exportar CSV**.
  6. **Compartilhar** em cada jogo gera a arte do confronto; em **Premiação**, **Ver artes** gera a **Arte dos campeões**.
- **Para quem:** organizador, co-organizador e árbitro convidado.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** [`torneios-chave`](2026-11-13/torneios-chave.png), [`torneios-placar`](2026-11-13/torneios-placar.png)

### Painel do organizador
- **Onde fica:** Torneios › **Painel do organizador**.
- **Para que serve:** ver todos os seus eventos e inscritos num lugar só.
- **Como usar:** abas **Visão**, **Torneios** e **Inscritos**. Em **Torneios**: **Editar**, **Publicar**, **Fechar inscrições**, **Reabrir inscrições**, **Replicar**, **Cancelar**.
- **Para quem:** organizador.
- **Grátis ou pago:** grátis.
- **Status:** no ar para **Visão**, **Torneios** e **Inscritos**. As abas **Analytics** e **Financeiro** do painel mostram "Em breve": o financeiro de cada torneio já existe, mas dentro da página do torneio (**Gestão financeira**).
- **Telas:** [`torneios-lista`](2026-11-13/torneios-lista.png) (botão de entrada)

---

## 9. ITF

### Torneios ITF
- **Onde fica:** Torneios › aba **ITF**; bloco **ITF ao vivo** na Home; página de cada torneio.
- **Para que serve:** acompanhar chaves, resultados e inscritos do circuito mundial.
- **Como usar:**
  1. Torneios › **ITF**; alterne **Abertos** / **Encerrados**. O torneio em andamento fica no topo, com o selo **Ao vivo**.
  2. Toque no cartão do torneio.
  3. Escolha **Matches** ou **Players**.
  4. Em **Matches**, filtre por **Duplas** / **Simples**, **Masculino** / **Feminino** / **Misto** e pela fase.
  5. **Abrir no ITF** leva ao site oficial.
- **Para quem:** todos, inclusive visitante sem conta.
- **Grátis ou pago:** grátis.
- **Status:** no ar. Os dados são atualizados de hora em hora durante os torneios.
- **Telas:** [`itf-lista-ao-vivo`](2026-11-13/itf-lista-ao-vivo.png), [`itf-chave`](2026-11-13/itf-chave.png), [`home-inicio`](2026-11-13/home-inicio.png)

### Favoritos
- **Onde fica:** estrela ao lado do nome do jogador na chave ITF, na aba **Players**, no Ranking ITF e na chave de torneio local de simples.
- **Para que serve:** marcar os atletas que você acompanha e ver em que torneios eles estão.
- **Como usar:**
  1. Toque na estrela (**Favoritar jogador**).
  2. Na lista de torneios ITF, o cartão passa a mostrar **N favoritos**.
  3. Na página do torneio, toque em **N favoritos** para abrir **Seus favoritos neste torneio**.
- **Para quem:** jogador com conta.
- **Grátis ou pago:** grátis.
- **Status:** no ar. **Favoritar não gera aviso**: o app não notifica jogo marcado nem resultado do favorito.
- **Telas:** [`itf-favoritos`](2026-11-13/itf-favoritos.png), [`ranking-itf`](2026-11-13/ranking-itf.png)

### Ranking ITF
- **Onde fica:** aba **Ranking** › **ITF**.
- **Para que serve:** consultar o ranking mundial de beach tennis.
- **Como usar:**
  1. Ranking › **ITF**.
  2. Escolha **Masculino MD** ou **Feminino WD**.
  3. Use **Buscar por nome ou país...**.
  4. Toque na linha para ver o resumo do atleta; a estrela favorita.
- **Para quem:** todos, inclusive visitante.
- **Grátis ou pago:** grátis.
- **Status:** no ar. Atualização semanal; a tela mostra a data. Não há ranking misto, porque a ITF não publica.
- **Telas:** [`ranking-itf`](2026-11-13/ranking-itf.png)

### Vídeos dos jogos
- **Onde fica:** botão na linha do jogo, na chave ITF (**Assistir ao vivo**, **Ver transmissão** ou o horário programado); busca **Buscar vídeos e perfis de atletas e arenas**, no topo de Torneios; **Meus jogos**, no perfil de quem tem vínculo ITF.
- **Para que serve:** achar e assistir aos jogos transmitidos do circuito.
- **Como usar:**
  1. Na chave, toque no botão de vídeo do jogo.
  2. Ou busque o nome do atleta em Torneios e abra **Atletas ITF · vídeos dos jogos**.
  3. Na página do atleta, filtre em **Todos os torneios** / **Qualquer data**.
- **Para quem:** todos.
- **Grátis ou pago:** grátis.
- **Status:** no ar. Os vídeos vêm dos canais PlayBT e Arena Ace e abrem no YouTube; não há player dentro do app.
- **Telas:** —

### Resultado Smatch na chave ITF
- **Onde fica:** na chave do torneio ITF.
- **Para que serve:** mostrar o resultado de um jogo antes de a ITF publicar.
- **Como usar:** o público só vê. O jogo aparece com a etiqueta **Resultado Smatch · aguardando ITF** ou **Jogo provisório · aguardando ITF**. Quando a ITF publica, vale o resultado dela.
- **Para quem:** todos veem; só administradores do Smatch lançam.
- **Grátis ou pago:** grátis.
- **Status:** em teste (operado pela equipe do Smatch; não conta pontos).
- **Telas:** —

---

## 10. Arenas

### Diretório e mapa de arenas
- **Onde fica:** aba **Arenas** (diretório). O mapa abre por Home › **Ver todas**.
- **Para que serve:** achar onde jogar, fazer aula ou alugar quadra perto de você.
- **Como usar:**
  1. Toque em **Arenas**.
  2. Filtre por **Tudo**, **Day use**, **Aulas** ou **Aluguel**.
  3. Escolha a cidade ou toque em **Perto de mim**.
  4. Em **Convênios**, marque **Wellhub** ou **TotalPass**.
  5. Use os atalhos **Professores** e **Buscar vaga**, ou toque no cartão da arena.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar. Só aparecem no diretório as arenas aprovadas e com plano ativo. No mapa aparecem também lugares cadastrados por jogadores ou achados no Google, sem perfil.
- **Telas:** [`arenas-lista`](2026-11-13/arenas-lista.png), [`home-inicio`](2026-11-13/home-inicio.png)

### Perfil da arena e favoritar
- **Onde fica:** cartão da arena no diretório.
- **Para que serve:** ver tudo sobre a arena antes de ir.
- **Como usar:**
  1. Veja endereço, descrição, fotos, professores, **Horário de funcionamento** e **Valores e serviços**.
  2. **Como chegar** abre o mapa.
  3. Use as abas **Day use**, **Aulas** e **Aluguel**.
  4. Toque no coração (**Favoritar arena**) para seguir.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar. Arena favorita aparece primeiro no diretório, e o dono vê quantas pessoas favoritaram. O seguidor **não recebe aviso** quando a arena cria Day Use ou turma.
- **Telas:** [`arenas-perfil`](2026-11-13/arenas-perfil.png)

### Day Use
- **Onde fica:** Arenas › **Day use**, ou a aba **Day use** no perfil da arena.
- **Para que serve:** saber quando a arena abre para jogo livre e avisar que você vai.
- **Como usar:**
  1. Abra o Day Use: data, horário, valor, atrações e descrição.
  2. Em **Vou nessa! Em qual período?**, toque em **Manhã**, **Tarde** ou **Noite**.
  3. Veja **N confirmados** e quem vai, por categoria.
  4. **Cancelar presença** desfaz.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis no app. O valor do Day Use é **cobrado na arena**.
- **Status:** no ar.
- **Telas:** [`arenas-day-use`](2026-11-13/arenas-day-use.png), [`arenas-perfil`](2026-11-13/arenas-perfil.png)

### Aulas
- **Onde fica:** perfil da arena › **Aulas**; Arenas › **Buscar vaga**; depois, menu do avatar › **Minhas aulas**.
- **Para que serve:** achar turma do seu nível, pedir vaga e acompanhar suas aulas.
- **Como usar:**
  1. Abra a turma: nível, professor, dias, horário, vagas e mensalidade.
  2. Toque em **Quero participar**, escreva em **Conte para a arena** e **Enviar pedido**. A arena aceita ou recusa.
  3. Para testar antes, **Fazer uma aula** › **Aula experimental** ou **Aula avulsa** › escolha a data › **Pedir a aula**.
  4. Em **Minhas aulas**, veja **Sua semana** e **Sua frequência**.
  5. Se não puder ir, **Avisar que não vou**. Avisando dentro do prazo da arena, você ganha uma reposição: **Usar** › **Pedir reposição**.
- **Para quem:** jogador (aluno).
- **Grátis ou pago:** grátis no app. Mensalidade e aula avulsa são combinadas e pagas direto à arena.
- **Status:** no ar (a arena precisa ter o Plano Arena Gestão).
- **Telas:** [`arenas-aulas`](2026-11-13/arenas-aulas.png)

### Aluguel de quadra
- **Onde fica:** perfil da arena › **Aluguel** › **Reservar quadra**.
- **Para que serve:** reservar um horário de quadra pelo celular.
- **Como usar:**
  1. Escolha a quadra, o dia (até 14 dias à frente) e um horário **Livre**.
  2. Em **Reservar este horário?**, toque em **Reservar**.
  3. Em **Pague com Pix**, pague para a chave da arena dentro do tempo mostrado.
  4. Toque em **Já paguei**.
  5. A reserva fica em **Aguardando a arena confirmar** até virar **Reserva confirmada**.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis no app. O Pix vai direto para a arena; o Smatch não recebe esse dinheiro.
- **Status:** no ar (a arena precisa ter o Plano Arena Gestão). Uma reserva em aberto por vez. Depois de **Já paguei**, só a arena cancela; devolução é tratada fora do app.
- **Telas:** [`arenas-aluguel`](2026-11-13/arenas-aluguel.png)

### Buscar professor
- **Onde fica:** Arenas › **Professores**.
- **Para que serve:** achar professor por região ou nome e ver onde ele dá aula.
- **Como usar:** busque pela região ou pelo nome; filtre por **Rankeado ITF**; abra o professor para ver as arenas e as turmas abertas.
- **Para quem:** jogador.
- **Grátis ou pago:** grátis.
- **Status:** no ar.
- **Telas:** [`arenas-lista`](2026-11-13/arenas-lista.png), [`arenas-aulas`](2026-11-13/arenas-aulas.png)

---

## 11. Para o dono de arena e o professor

### Cadastrar a arena
- **Onde fica:** primeiro acesso (papel **Dono ou gestor de arena**) ou menu do avatar › `/arena/plano`.
- **Para que serve:** colocar a arena no Smatch.
- **Como usar:**
  1. **Passo 1 de 2 · cadastro grátis**: preencha os dados e toque em **Salvar e continuar**.
  2. **Passo 2 de 2 · ativar**: escolha o plano.
  3. Aguarde a aprovação do Smatch.
- **Para quem:** arena.
- **Grátis ou pago:** o cadastro é grátis, mas a arena só aparece no diretório e só gera Day Use com um plano ativo.
- **Status:** no ar. A aprovação é feita pela equipe do Smatch.
- **Telas:** —

### Plano Arena
- **Onde fica:** menu do avatar › carteira (`/carteira`) ou `/arena/plano`.
- **Para que serve:** ter a arena visível no app.
- **O que libera:** perfil público com logo, horários e preços; Day Use ilimitado; professores vinculados; selos Total Pass e Wellhub; painel da arena; Premium para o dono.
- **Para quem:** arena.
- **Grátis ou pago:** **R$ 99,90 por mês** desde 12/11/2026 (antes, R$ 49,90). Na web, só cartão de crédito, cobrança mensal. No app de iPhone e Android, compra pela loja: no Android já está em R$ 99,90; no iPhone o preço novo entra em 14/11/2026.
- **Status:** no ar. Não há período de teste. Ao cancelar, o acesso vale até o fim do período pago; depois o perfil e os Day Use somem do app.
- **Telas:** [`arenas-plano-arena`](2026-11-13/arenas-plano-arena.png), [`arenas-perfil`](2026-11-13/arenas-perfil.png)

### Plano Arena Gestão
- **Onde fica:** menu do avatar › carteira (`/carteira`).
- **Para que serve:** administrar aulas e aluguel de quadra pelo app.
- **O que libera:** tudo do Plano Arena, mais **Aulas** (turmas, pedidos de vaga, chamada, frequência, reposições), **Quadras** (reservas com Pix direto para a arena) e o painel com números completos.
- **Para quem:** arena.
- **Grátis ou pago:** **R$ 300,00 por mês**. Na web, só cartão de crédito, cobrança mensal. Subir do Plano Arena para o Gestão cobra na hora, sem abater os dias já pagos.
- **Status:** no ar desde 08/11/2026 (venda ligada na configuração de produção). Também é vendido pelas lojas, a R$ 300,00: a compra foi testada no Android em 09/11/2026 e a assinatura foi aprovada pela Apple no mesmo dia. Falta só um teste de compra feito num iPhone.
- **Telas:** [`arenas-plano-arena`](2026-11-13/arenas-plano-arena.png), [`arenas-painel`](2026-11-13/arenas-painel.png)

### Painel da arena
- **Onde fica:** menu do avatar › **Minha Arena** (`/arena/painel`).
- **Para que serve:** ver o dia da arena e resolver o que está esperando.
- **Como usar:**
  1. No topo, os números de **hoje**, **semana**, **alunos** e **mês**.
  2. Em **Precisa de você**, resolva cada item: **Confirmar pagamento** de reserva, **Aceitar** ou **Recusar** pedido de vaga, reposições e chamadas pendentes.
  3. Em **Sua semana**, veja a ocupação dia a dia.
  4. Em **Equipe**, **+ professor**; em **Turmas e alunos**, **+ turma**.
  5. Atalhos: **Agenda**, **Números**, **Fechar**, **Day use**.
- **Para quem:** arena.
- **Grátis ou pago:** incluído nos planos de arena. Sem o Gestão, o painel avisa **Plano Gestão libera quadras, turmas e números**.
- **Status:** no ar.
- **Telas:** [`arenas-painel`](2026-11-13/arenas-painel.png)

### Turmas, alunos e chamada
- **Onde fica:** painel › **Turmas e alunos** (`/arena/turmas`).
- **Para que serve:** organizar as turmas e acompanhar a presença.
- **Como usar:**
  1. **Nova turma**: nome, níveis, professor, dias da semana, início, fim, vagas (até 30) e valor mensal › **Salvar**.
  2. Na turma, aba **Alunos**: em **Pedidos aguardando**, **Aceitar** ou **Recusar**.
  3. **Adicionar aluno de fora** inclui quem não tem conta no app.
  4. **Chamada de hoje**: marque **Presente**, **Falta** ou **Avisou**.
  5. Veja a frequência de cada aluno e da turma.
- **Para quem:** arena e professor. Só o dono cria turma, aceita pedido de vaga e remove aluno. O professor vinculado faz a chamada, vê os alunos e responde aula experimental e avulsa (menu **Minhas turmas (professor)**).
- **Grátis ou pago:** Plano Arena Gestão (R$ 300,00 por mês). A mensalidade aparece só como informação; o app não cobra aula.
- **Status:** no ar.
- **Telas:** [`arenas-turma`](2026-11-13/arenas-turma.png), [`arenas-aulas`](2026-11-13/arenas-aulas.png), [`arenas-painel`](2026-11-13/arenas-painel.png)

### Quadras e reservas
- **Onde fica:** painel › `/arena/quadras`, com **Quadras** / **Agenda**.
- **Para que serve:** receber reservas de quadra pelo app.
- **Como usar:**
  1. **Nova quadra**: nome, **Preço padrão por horário (R$)** e até 10 **Faixas de preço**.
  2. Em **Reservas e Pix**, informe a chave Pix da arena, a duração do horário (60, 90 ou 120 minutos) e o tempo para pagar.
  3. Quando o jogador avisar que pagou, **Confirmar pagamento** ou **Cancelar reserva** (com motivo).
- **Para quem:** arena.
- **Grátis ou pago:** Plano Arena Gestão (R$ 300,00 por mês). O Smatch não fica com nada do aluguel.
- **Status:** no ar. Sem chave Pix cadastrada, a arena não recebe reservas. O jogador não envia comprovante: a arena confere o Pix na própria conta.
- **Telas:** [`arenas-aluguel`](2026-11-13/arenas-aluguel.png), [`arenas-painel`](2026-11-13/arenas-painel.png)

### Day Use (criar)
- **Onde fica:** painel › **Day use**, ou Arenas › **Day use** › **Novo Day Use**.
- **Para que serve:** divulgar os dias de jogo livre.
- **Como usar:**
  1. **Novo Day Use**: título, cidade, data, início, fim, valor, extras e descrição.
  2. Ou preencha **Horário de Day Use** e **Valor padrão do Day Use** no perfil da arena: o app cria sozinho um Day Use por dia aberto, para os próximos 21 dias.
  3. Acompanhe quantas pessoas confirmaram em cada período.
- **Para quem:** arena.
- **Grátis ou pago:** incluído no Plano Arena (R$ 99,90 por mês) e no Gestão.
- **Status:** no ar. O Day Use criado já sai publicado; não há rascunho.
- **Telas:** [`arenas-day-use`](2026-11-13/arenas-day-use.png)

### Fechar a arena numa data
- **Onde fica:** painel › **Fechar** ("Fechamentos e torneios").
- **Para que serve:** bloquear a agenda num feriado, numa manutenção ou num evento.
- **Como usar:**
  1. **Novo fechamento**: **Fechada** ou **Evento**, início, fim e motivo.
  2. Confira o que será afetado.
  3. Confirme em **Cancelar reservas e fechar** ou **Cancelar aulas e fechar**.
- **Para quem:** arena.
- **Grátis ou pago:** Plano Arena Gestão.
- **Status:** no ar. As reservas e as aulas do período são canceladas e os alunos e jogadores são avisados no sino. Torneio marcado como **Na minha arena** fecha a agenda nos dias do torneio automaticamente.
- **Telas:** [`arenas-avisos`](2026-11-13/arenas-avisos.png)

### Números da arena
- **Onde fica:** painel › **Números** (`/arena/numeros`).
- **Para que serve:** ver como a arena foi no mês.
- **Como usar:** em **Números do mês**, troque o mês e veja **Aluguel de quadra**, **Ocupação das quadras**, **Alunos e turmas**, **Frequência** e **Alcance da arena** (quantas pessoas favoritaram, visitas à página, presenças no Day Use).
- **Para quem:** arena.
- **Grátis ou pago:** **Alcance da arena** em qualquer plano; os demais blocos, só no Gestão.
- **Status:** no ar.
- **Telas:** [`arenas-seguidores`](2026-11-13/arenas-seguidores.png)

### Professores da arena
- **Onde fica:** perfil da arena › editar › **Professores vinculados**; o professor responde em menu do avatar › **Convites de arena**.
- **Para que serve:** mostrar a equipe de professores no perfil da arena.
- **Como usar:**
  1. A arena usa **Buscar professor por nome** e convida.
  2. O professor aceita em **Convites de arena**.
  3. O professor passa a aparecer no perfil da arena e pode ser colocado nas turmas.
- **Para quem:** arena e professor.
- **Grátis ou pago:** grátis para o professor; a arena precisa de plano (o Plano Arena basta).
- **Status:** no ar.
- **Telas:** [`arenas-aulas`](2026-11-13/arenas-aulas.png), [`arenas-painel`](2026-11-13/arenas-painel.png)

### Avisos da arena
- **Onde fica:** sino de quem é aluno ou tem reserva.
- **Para que serve:** avisar quem foi afetado por um fechamento.
- **Como usar:** é automático. Ao fechar a arena, o app avisa os alunos (**aula cancelada**) e quem tinha reserva; ao reabrir, avisa **Aula de volta**.
- **Para quem:** jogador (recebe) e arena (gera ao fechar).
- **Grátis ou pago:** incluído no Gestão.
- **Status:** no ar, **só para esses avisos automáticos**. A arena **não consegue escrever um comunicado** para alunos ou seguidores; isso não existe no app.
- **Telas:** [`arenas-avisos`](2026-11-13/arenas-avisos.png)

---

## 12. Premium e carteira

### Premium
- **Onde fica:** menu do avatar › **Virar Premium** (para quem assina, **Minha Carteira**).
- **Para que serve:** ter vantagens no match e o selo de verificado.
- **O que libera (são só estas quatro coisas):**
  1. **Te curtiram**: ver quem curtiu você, sem as fotos borradas.
  2. **Onde tá rolando**: arenas com gente ativa por perto.
  3. Perfil no topo das filas de **Social** e **Dupla**.
  4. Selo **Perfil verificado**.
- **Como usar:** **Virar Premium** › **Testar 7 dias grátis** ou assinar › para sair, **Gerenciar** › **Cancelar assinatura**.
- **Para quem:** jogador.
- **Grátis ou pago:** **R$ 9,90 por mês**. Na web, só cartão de crédito (pede CPF ou CNPJ e CEP); não há Pix. No app de iPhone e Android, compra pela loja. O teste de 7 dias existe só na web, sem cartão, uma vez por CPF.
- **Status:** no ar. Cancelando, o acesso vale até o fim do período pago.
- **Telas:** [`arenas-plano-arena`](2026-11-13/arenas-plano-arena.png) (a carteira mostra os três planos)

---

## 13. Apps e site

### Apps de iPhone e Android
- **O que são:** o mesmo app da web, dentro de um aplicativo das lojas. Tudo o que funciona na web funciona no app.
- **Só no app:** compra de Premium, Plano Arena e Plano Arena Gestão pela loja; **Continuar com Apple** no iPhone.
- **Status:** no ar. **Não há notificação push.**

### Site público
- **Onde fica:** smatchbeach.com.
- **O que tem:** página inicial, página para organizadores, guia de ranking de beach tennis, blog com 3 textos, lista de torneios e uma página por torneio, além das páginas legais e de suporte.
- **Status:** no ar. Não há página de arena nem de torneio ITF no site. A página inicial tem seletor de português, inglês e espanhol; blog e textos legais só em português.

---

## 14. Planejado

Nada desta lista existe no app hoje. São itens descritos nos documentos de planejamento
do projeto ou marcados como "Em breve" dentro do próprio app.

**Torneios**
- Aba **Analytics** do painel do organizador (visualizações, interessados, conversão, origem).
- Aba **Financeiro** do painel do organizador com receita, saldo e histórico de todos os torneios.
- Check-in dos atletas no dia do torneio.
- Editor de cruzamento do mata-mata na Copa por Equipes.

**Arenas e aulas**
- Comunicado escrito pela arena para alunos e seguidores.
- Aviso ao seguidor quando a arena cria Day Use ou turma.
- Mensalidade, pacote de aulas, Day Use ou aluguel pagos dentro do app.
- Envio da foto do comprovante da reserva; cancelamento pelo jogador depois de pagar; estorno; lembrete da reserva.
- Horário fixo semanal de quadra (mensalista) e bloqueio manual de um horário.
- Fechar só uma quadra; remarcar sozinho a aula cancelada.
- Lista de espera de turma.
- Calendário mensal das aulas.
- Avaliação de arenas e professores.
- Acesso de funcionário ou recepção ao painel da arena; exportar planilha.

**Coringa e árbitros**
- Chamada "preciso de árbitro" e disponibilidade do árbitro no Coringa (hoje só existe a lista de árbitros).
- Pagamento do árbitro e conferência do certificado.

**Geral**
- Notificações push.
- Aviso de jogo e de resultado dos jogadores favoritos.
- Publicação automática no Instagram quando uma arena é aprovada (o código existe, mas está desligado, à espera das credenciais da Meta).

---

## 15. Cuidados na divulgação

O que parece pronto e não está, ou funciona de um jeito diferente do que o nome sugere.

1. **"Plano Arena R$ 300"** não existe com esse nome. R$ 300,00 é o **Plano Arena Gestão**; o **Plano Arena** custa R$ 99,90.
2. **Não há notificação push.** Todo aviso aparece só no sino, dentro do app.
3. **Favoritar não avisa.** Marcar um jogador ou uma arena como favorito não gera notificação de jogo, resultado, Day Use ou turma nova.
4. **A arena não envia comunicados.** Os "avisos" são só os automáticos de fechamento (aula cancelada, aula de volta, reserva cancelada).
5. **O app não recebe pagamento de Day Use, aula nem aluguel.** Tudo isso é pago direto à arena. No aluguel, o Pix vai para a chave da arena e ela confirma à mão.
6. **Planos e Premium na web só aceitam cartão de crédito.** Pix existe apenas na inscrição de torneio.
7. **Inscrição em torneio pelo app é só por Pix**, e o valor é único por torneio (não há preço por categoria).
8. **Atleta que cancela a própria inscrição paga não recebe devolução automática.** A devolução automática vale quando o organizador cancela.
9. **O selo "Verificado" não confere documento.** Ele é um benefício do Premium, ativado na hora.
10. **O cadastro grátis da arena não a coloca no diretório.** A arena só aparece para os jogadores depois de aprovada e com plano ativo.
11. **Desafio, Super 8, Ranking de duplas fixas e Copa por Equipes não pontuam** no ranking local. Só o formato Torneio e o histórico importado da LetzPlay.
12. **O teste grátis de 7 dias do Premium vale só na web**, uma vez por CPF. No app das lojas ele não existe.
13. **Vídeos abrem no YouTube.** Não há player dentro do app, e só entram jogos transmitidos pelos canais PlayBT e Arena Ace.
14. **Vínculo com o perfil ITF** é só para a categoria PRO e para professores, com aprovação manual.
15. **A chave do mata-mata não tem disputa de terceiro lugar, cabeças de chave nem quadra por jogo.** Super 8 e Copa têm quadra e terceiro lugar.
16. **Copa por Equipes e Rei da Praia** ainda não foram usados em evento real; trate como novidade em validação, não como produto consolidado.
17. **Pessoas reais nas telas.** Desde 13/11/2026 as telas mostram dois perfis reais, com autorização: o **Leandro Silva** é a conta que tira as fotos (canto de todas as telas e "Meu cartão") e o **Vicente Brusadelli** é o cartão do Match, o card de perfil e o primeiro coringa. A ficha de jogador dos dois (foto, categoria, lado, dias) é a real; os torneios, pontos, ranking e a chamada de coringa em que aparecem são de demonstração. Não use as telas para afirmar resultados deles. No Match, o Vicente (PRO) aparece para a conta C só na captura: no app o baralho mostra apenas a mesma categoria.

## Como este mapa foi feito

Leitura do código do app, das funções do servidor e das migrações do banco, no commit
`fc7fb93e` de 12/11/2026. Três pontos foram conferidos também em produção: a venda do
Plano Arena Gestão está ligada, a taxa do torneio é de R$ 1,00 mais R$ 0,99 do Pix com
cobrança mínima de R$ 5,00, e o teste do Premium é de 7 dias. Os nomes de botões citados
(353) foram conferidos um a um contra o texto em português do app. A situação do Plano
Arena Gestão nas lojas vem do registro do cadastro feito em 08 e 09/11/2026, não do código. Para atualizar o mapa a cada release, releia o
código das áreas que mudaram e refaça a biblioteca de telas.
