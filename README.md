# Ministério ADEALGO

Sistema da **Assembleia de Deus Missão de Águas Lindas de Goiás (ADEALGO)**, com três partes:

- **Site público**: apresenta o ministério, os pastores, os cultos, os eventos e as congregações.
- **Painel administrativo**: secretaria da igreja, com cadastro de membros, documentos, carteirinhas, relatórios e o conteúdo do site.
- **Portal do membro**: cada membro consulta os próprios dados, carteirinhas e documentos.

> As telas abaixo foram capturadas com dados de teste. Os CPFs e nomes são fictícios.

## Sumário

- [Site público](#site-público)
- [Painel administrativo](#painel-administrativo)
  - [Membros](#membros)
  - [Pastores, congregações e agenda](#pastores-congregações-e-agenda)
  - [Conteúdo do site](#conteúdo-do-site)
  - [Documentos, carteirinhas e relatórios](#documentos-carteirinhas-e-relatórios)
  - [Administração e auditoria](#administração-e-auditoria)
- [Portal do membro](#portal-do-membro)
- [Perfis e permissões](#perfis-e-permissões)
- [Identidade visual](#identidade-visual)
- [Tecnologias](#tecnologias)

---

## Site público

### Página inicial

O banner mostra fotos da igreja sob um degradê e dois botões: "Faça parte da família" e "Encontre uma congregação". O título, a linha de cima e as fotos do fundo são editáveis pelo painel, em **Conteúdo do Site**.

![Página inicial](docs/telas/01-site-inicio.jpg)

### Avisos e destaques

Logo abaixo do topo aparecem os avisos cadastrados no painel, com imagem, texto e botão opcionais. Cada aviso pode ter um período para aparecer (por exemplo, só na semana do evento). Sem nenhum aviso vigente, a seção não aparece.

![Avisos e destaques](docs/telas/01b-site-avisos.jpg)

### História do Ministério

O texto e as fotos que passam ao lado dele são editáveis pelo painel, em **Conteúdo do Site**.

![História do Ministério](docs/telas/02-site-historia.jpg)

### Pastores do Ministério

Clique ou passe o mouse sobre a foto para ler a biografia de cada pastor. Os pastores exibidos são os marcados como **Pastor do Ministério** no cadastro.

![Pastores do Ministério](docs/telas/03-site-pastores-ministerio.jpg)

### Pastores nas Congregações

Carrossel com os pastores ativos. O botão "Ver Biografia" abre a biografia com as redes sociais.

![Pastores nas congregações](docs/telas/04-site-pastores-congregacoes.jpg)

### Cultos

Horários de cada congregação, com link para o mapa e para a transmissão.

![Cultos](docs/telas/05-site-cultos.jpg)

### Eventos

Os próximos eventos em destaque. Eventos que já passaram saem da lista automaticamente. O banner aparece inteiro, sem cortes, em qualquer formato: feed 4:5, quadrado ou stories. Há botão de inscrição quando o evento tem link.

![Eventos](docs/telas/06-site-eventos.jpg)

**Compartilhar:** cada evento tem um botão **Compartilhar**.

- **No celular**, abre o menu do próprio aparelho (WhatsApp, Instagram, Facebook etc.) e envia a **imagem do banner** junto com o título, a data e o link do evento.
- **No computador**, oferece WhatsApp, Facebook, copiar link e baixar o banner.

Tocar no banner abre a **página do evento** (`evento.xhtml?id=N`), com o banner grande e os botões **Compartilhar** e **Baixar banner**. Quando o link é enviado, o WhatsApp e o Facebook mostram uma prévia com o banner e o título.

![Página do evento no celular](docs/telas/06b-site-evento-celular.jpg)

### Congregações

Endereço de cada congregação, com link para o Google Maps. O mapa interativo aparece abaixo dos cards (não aparece na captura).

![Congregações](docs/telas/07-site-congregacoes.jpg)

### Conferir documento

Ofícios e carteirinhas trazem um QR Code que abre a conferência pública do documento: situação, número, data e, no ofício, o assunto e quem assinou. O QR usa um endereço curto (`/v/código`), mais fácil de ler no papel. Se o QR não puder ser lido, a página **Conferir documento** (link no rodapé do site) aceita o código impresso no rodapé do ofício, em maiúsculas ou minúsculas, ou o link colado. Os endereços dos documentos já impressos continuam funcionando.

![Conferir documento](docs/telas/07b-site-conferir.jpg)

### No celular e acesso restrito

O site se adapta a telas pequenas. O botão **Área Restrita** leva ao login.

| Celular | Login |
|---|---|
| ![Site no celular](docs/telas/09-site-celular.jpg) | ![Login](docs/telas/08-login.jpg) |

---

## Painel administrativo

O menu lateral é organizado em grupos: Pessoas, Igreja e Agenda, Documentos e Relatórios, e Administração. Cada perfil vê somente os itens a que tem permissão.

![Início do painel](docs/telas/10-admin-painel.jpg)

### Membros

#### Lista de membros

Busca por nome, CPF e congregação. Pela lista se acessa a ficha, as consagrações, as movimentações, as disciplinas e a carteirinha de cada membro.

![Lista de membros](docs/telas/11-admin-membros.jpg)

#### Ficha do membro

Dados pessoais, foto, congregação, estado civil, filiação, contato e endereço.

![Ficha do membro](docs/telas/12-admin-membro-ficha.jpg)

#### Batismo e consagrações

Registro do batismo nas águas e das consagrações do membro (diácono/diaconisa, presbítero, evangelista, missionário(a), pastor). **É daqui que saem os certificados de batismo, separação, consagração e ordenação.** Cada certificado é numerado (`BT-2026-000012` para batismo, `CS-...` para consagração), usa a arte do seu tipo e traz a data, a congregação e quem apresentou/oficiou. As vias e o cancelamento funcionam como nas apresentações. A função do membro (usada nas cartas e nas carteirinhas) é a consagração mais recente, ignorando o batismo.

![Batismo e consagrações](docs/telas/13-admin-consagracoes.jpg)

![Certificado de batismo](docs/telas/23c-certificado-batismo.jpg)

#### Movimentações

Histórico de admissão, saída e retorno do membro.

![Movimentações](docs/telas/14-admin-movimentacoes.jpg)

#### Visitantes

Registro simples de quem visita a igreja, para apresentar no culto e, mais adiante, ligar e marcar visita.

- **Porteiro (perfil Recepção):** usuário próprio, ligado à congregação. Ao entrar, cai direto na página **Registrar visitante**, feita para o celular.
  - Campos obrigatórios: nome completo e celular com DDD.
  - Campos opcionais: primeira vez na igreja, quem convidou e bairro.
  - **Aceita receber contato:** sem esse "sim", a igreja não liga nem marca visita (LGPD).
  - O culto vem da agenda da congregação (**Igreja e Agenda › Cultos**). O sistema sugere o culto do horário e o porteiro pode trocar.
  - Abaixo, os nomes registrados hoje na congregação, sem telefone, com os botões para corrigir a digitação ou remover um lançamento errado. O porteiro não entra no painel.
- **Mesma pessoa:** o mesmo celular na mesma congregação é a mesma pessoa; quem volta aparece como "2ª visita", "3ª visita" e assim por diante. O mesmo celular não é registrado duas vezes no mesmo dia.
- **Visitantes de hoje (pastor):** menu **Pessoas › Visitantes de hoje**. Só os nomes, em letra grande, separados por culto, com "primeira vez", o número da visita e quem convidou. A página se atualiza sozinha a cada 30 segundos, e um toque no nome marca como apresentado.
- **Acompanhamento (pastor e secretaria):** menu **Pessoas › Acompanhamento de visitantes**.
  - A lista abre nos **pendentes**: quem autorizou contato e ainda não foi visitado. Mostra o celular, os botões **Ligar** e **WhatsApp**, o número de visitas e a última visita.
  - Filtros por nome, congregação, situação e período da última visita.
  - Quem não autorizou contato aparece sem o celular, e não dá para marcar contato nem visita.
  - **Acompanhar** abre a situação (A contatar, Contatado, Visita marcada, Visitado, Não quer contato, Tornou-se membro), o responsável, o dia e a hora da visita marcada e uma anotação. Cada mudança fica no histórico do visitante, com quem fez e quando, junto com as visitas dele.
  - "Não quer contato" retira a autorização; ela volta se o visitante disser "sim" de novo na recepção.
  - **Cadastrar como membro** abre a ficha nova com o nome, o celular e a congregação do visitante.
- **Relatório de visitantes:** menu **Pessoas › Relatório de visitantes** (também pelo atalho em **Relatórios**).
  - Período (com os atalhos "Últimos 7 dias", "Este mês" e "Mês passado"), congregação e culto.
  - Números: visitas, pessoas, primeira vez, retornos, quantos aceitaram contato e quantos foram visitados ou viraram membros.
  - Totais por culto (dia, culto, visitantes, primeira vez) e cada registro, com hora, quem convidou e quem registrou: serve de registro de quem entrou na igreja.
  - Sai em **PDF** e em **planilha (CSV)**. O celular só aparece de quem autorizou contato.
- **Início do painel:** quem vê visitantes encontra no topo os visitantes dos últimos 7 dias e quantos estão para contatar, com link para cada lista.
- **Observação de segurança:** campo opcional do registro para anotar alguém que chamou a atenção. Só o pastor e o administrador veem, inclusive no relatório e no PDF. Não se pede foto nem documento: nome, celular e horário já ficam registrados, com quem registrou.
- **Permissão:** módulo **Visitantes** no Controle de Acesso (Visualizar = visitantes de hoje e a lista do acompanhamento, com os celulares; Editar = registrar e corrigir, pelo menu **Registrar visitante**, e registrar o acompanhamento; Emitir = relatório de visitantes). Pastor e secretário começam com as três. Todos ficam na própria congregação, salvo com "Ver todas as congregações".
- **LGPD:** quem passa 2 anos sem voltar tem o nome, o celular, o bairro e as anotações apagados automaticamente. As visitas continuam contando nos totais.

| Registrar visitante (celular do porteiro) | Visitantes de hoje (pastor) |
|---|---|
| ![Registrar visitante](docs/telas/54-recepcao-visitantes.jpg) | ![Visitantes de hoje](docs/telas/55-admin-visitantes-hoje.jpg) |

| Acompanhamento | Relatório |
|---|---|
| ![Acompanhamento de visitantes](docs/telas/56-admin-visitantes-acompanhamento.jpg) | ![Relatório de visitantes](docs/telas/57-admin-visitantes-relatorio.jpg) |

### Pastores, congregações e agenda

#### Pastores

Cadastro vinculado a um membro. Cada pastor tem foto, cargo, congregação, biografia curta e completa, redes sociais e ordem de exibição no site. A opção **Pastor do Ministério** coloca o pastor no bloco da página inicial.

| Lista | Edição |
|---|---|
| ![Pastores](docs/telas/15-admin-pastores.jpg) | ![Edição de pastor](docs/telas/16-admin-pastor-edicao.jpg) |

#### Congregações e eventos

Congregações com endereço e coordenadas para o mapa. Eventos com banner, tipo e congregação, e opção de destaque no site. O banner aceita JPG, PNG ou WebP de até 15 MB; um arquivo maior é recusado com aviso já na escolha.

| Congregações | Eventos |
|---|---|
| ![Congregações](docs/telas/17-admin-congregacoes.jpg) | ![Eventos](docs/telas/18-admin-eventos.jpg) |

#### Cultos

Agenda semanal de cultos de cada congregação.

![Cultos](docs/telas/19-admin-cultos.jpg)

### Conteúdo do site

Tudo o que aparece na página inicial fica em um só lugar, em abas na ordem da página:

- **Topo da página**: título, linha de cima e fotos do fundo. As fotos podem ser enviadas, reordenadas, ocultadas ou removidas; no celular aparece só a primeira.
- **História do Ministério**: texto (parágrafos separados por uma linha em branco) e as fotos de rolagem ao lado dele.
- **Avisos e destaques**: avisos com imagem, link, ordem e período. A lista mostra se cada um está no site, agendado, encerrado ou oculto.
- **Outras seções**: atalhos para os cadastros que alimentam o resto da página (Pastores, Cultos, Eventos e Congregações).

As fotos enviadas são convertidas para JPEG e reduzidas automaticamente, para o site carregar rápido. Cada seção mantém pelo menos uma foto visível. A tela mostra quem fez a última alteração e quando.

| Topo da página | Avisos e destaques |
|---|---|
| ![Conteúdo do site](docs/telas/21-admin-conteudo-site.jpg) | ![Avisos e destaques](docs/telas/20-admin-avisos.jpg) |

### Documentos, carteirinhas e relatórios

#### Carteirinhas

Carteirinhas do Ministério e da Convenção, impressas em PDF e exibidas como carteirinha digital no portal do membro.

- **Validade de 1 ano a partir da emissão.** Cada carteirinha recebe um número (`MN-2026-000012` no Ministério, `CV-...` na Convenção) e um código aleatório para o QR Code. Reimprimir o PDF mantém o número e o QR da carteirinha válida. Se ela estiver vencida, uma nova é emitida.
- **QR Code de conferência** no verso: o endereço curto `/v/código` abre a página pública `validar.xhtml`, que mostra só a situação, o nome, a função, a congregação, o número e a validade. O CPF não aparece nem no QR nem nessa página, e a página não é indexada por buscadores.
- **Quem pode ter:** membros com congregação ativa. Crianças apresentadas ficam de fora. A carteirinha da **Convenção** é só para quem tem os números de registro da **CGADB** e da **CONFRAMADEGO** no cadastro do membro (campos na ficha).
- **Situação** na lista: *Válida*, *Vencida*, *Suspensa*, *Cancelada*, *Substituída por nova via* ou *Sem vínculo ativo*. Membro em disciplina aparece como suspenso; membro desligado (última movimentação é uma saída) aparece sem vínculo ativo. Isso vale também na conferência pelo QR, que não mostra o motivo.
- **Ações da secretaria:** PDF, *Nova via* (a anterior deixa de valer), *Suspender* e *Cancelar* (com motivo) e *Reativar*. Tudo fica registrado na Auditoria. Os filtros mostram quem ainda não tem carteirinha e quais vencem em 30 dias.
- A foto só sai na carteirinha se o membro permitir no termo de privacidade (permitido por padrão).
- **Google Wallet:** com a conta configurada (ver [Google Wallet](#google-wallet)), o membro vê o botão **Adicionar à Google Wallet** na carteirinha válida. O cartão leva nome, função, congregação, número, validade e o mesmo QR Code de conferência, sem CPF e sem foto. Suspender, reativar, cancelar ou emitir nova via atualiza o cartão já salvo no celular. Se o Google estiver fora do ar, a ação da secretaria vale assim mesmo e a falha fica no log. A tela de carteirinhas mostra se a Google Wallet está ativa.
- **Apple Wallet:** com o certificado configurado (ver [Apple Wallet](#apple-wallet)), o membro baixa o cartão (`.pkpass`) pelo botão **Adicionar à Apple Wallet**. O cartão traz os mesmos dados e o QR Code de conferência, mais a foto se o membro permitir. Suspender, reativar, cancelar ou emitir nova via avisa o iPhone por push, e ele baixa a versão nova sozinho. Suspensa aparece em cinza; cancelada ou substituída fica anulada na Wallet.
- O QR Code aponta para o **endereço do sistema**, definido na instalação (ver [Endereço do sistema](#endereço-do-sistema)).

![Carteirinhas](docs/telas/22-admin-carteirinhas.jpg)

#### Documentos

**Todo documento é emitido no seu registro de origem**, e não mais a partir de um modelo solto. A origem fica no histórico:

| Documento | Onde é emitido | Número |
|---|---|---|
| Certificado de apresentação | Apresentações | `AP-ano-sequencial` |
| Certificados de batismo, separação, consagração e ordenação | Membros › Batismo e consagrações | `BT-...` / `CS-...` |
| Cartas de mudança e de recomendação | Cartas | `CM-...` / `CR-...` |

Toda emissão segue o mesmo fluxo:

- **Vias:** cada emissão é uma via numerada, com o PDF guardado, hash, quem emitiu, IP e data.
- **Nova emissão:** emitir de novo gera a 2ª via, com histórico.
- **Cancelamento:** registro com documento emitido não é excluído, é cancelado com motivo.
- **Auditoria:** alterações depois da emissão ficam registradas.

O menu **Documentos** é a **pesquisa** de tudo que foi emitido: por membro, CPF, nº do documento, tipo e período. Por ele também se visualiza e reimprime cada documento (a reimpressão é o mesmo PDF e fica registrada).

![Documentos](docs/telas/23-admin-documentos.jpg)

#### Cartas de mudança e recomendação

Cada carta é registrada com destino, cidade, data e, na recomendação, validade (30 dias por padrão). O texto sai desse registro, com a função do membro, e a carta é numerada.

- **Disciplina:** como atesta plena comunhão, a carta **não é emitida para membro em disciplina**.
- **Validade:** a recomendação vencida também não é emitida.
- **Acesso:** pela lista de membros, o botão de carta já abre o cadastro com o membro.
- **Layout:** igual ao da carta feita à mão. Na coluna "Pertencente à congregação" saem as congregações com o quadradinho (☒ na da carta), o nome em letras condensadas e o endereço abaixo; o texto sai com serifa, o nome do membro em negrito e, abaixo das linhas, o nome e o cargo de quem assina (também na via para assinar à mão).
- **Congregações na carta:** em **Congregações**, cada uma tem "Nome nas cartas" (ex.: JARDIM DA B. II), "Endereço nas cartas" e "Posição" (vazio = não aparece; a congregação da carta aparece sempre). Os valores iniciais vieram da carta em uso.

![Cartas](docs/telas/23b-admin-cartas.jpg)

![Carta de recomendação](docs/telas/23d-carta-recomendacao.jpg)

#### Ofícios à convenção

Ofícios para a CONFRAMADEGO (separação ao diaconato e ao presbitério, consagração a evangelista, ordenação a pastor, retirada de processo de ordenação, filiação e desligamento), feitos no sistema em vez do Word, com numeração controlada e o histórico de cada um. Fica em **Documentos e Relatórios > Ofícios**.

**Como funciona:**

1. **Rascunho:** quem tem a permissão escolhe o modelo e o membro. O sistema preenche nome, cargo atual (a última consagração), cargo pretendido (Diácono ou Diaconisa, conforme o sexo) e congregação. Falta só a data da assembleia e, se quiser, ajustar o texto. O que ainda precisa ser completado aparece como `[preencher: ...]` e impede o envio. Também há o **ofício livre**, para outros assuntos, e dá para escrever o nome de um obreiro que não é membro.
2. **Aprovação:** o rascunho vai para os **aprovadores** escolhidos pelo administrador (ex.: o pastor presidente). Eles recebem aviso por e-mail (com o envio de e-mails ligado) e veem a quantidade pendente no menu. O aprovador confere o PDF do rascunho (com a marca "RASCUNHO") e **aprova** ou **devolve** dizendo o que corrigir.
3. **Número:** só a aprovação dá o número, no formato dos ofícios em Word (**07/2026**), em sequência por ano, sem pular nem repetir. Ofício aprovado não é excluído: se não valer mais, é **cancelado** com o motivo e o número continua no livro.
4. **PDF:** com o timbre (CGADB, ADEALGO e CONFRAMADEGO, nome e dados da igreja), o nome e o cargo de quem aprovou (e a assinatura digitalizada, se cadastrada) e um **QR Code** que leva à conferência pública do ofício. O rodapé traz também o código do ofício (ex.: `OFPATXY79C2S`) para digitar em **Conferir documento**, caso o QR não possa ser lido.
5. **Envio e resposta:** registra-se quando e como foi enviado à convenção e a resposta (deferido ou indeferido). No deferido, a tela lembra de registrar a consagração na ficha do membro.

**Quem faz o quê:** permissão **Ofícios** no Controle de Acesso (Visualizar = lista e PDF; Editar = criar e enviar para aprovação; Emitir = registrar envio, resposta e cancelar). Quem aprova é escolhido em **Ofícios > Configuração**, e o aprovador acessa os ofícios mesmo sem a permissão do perfil. Pastor e secretário veem os ofícios da própria congregação; aprovadores e o administrador veem todos.

**Configuração (administrador):** os textos dos modelos (com as variáveis `{{nome}}`, `{{cargo_atual}}`, `{{cargo_pretendido}}`, `{{data_assembleia}}`, `{{congregacao}}` e `{{igreja}}`), os aprovadores, o timbre, o destinatário padrão e a **numeração**. Para continuar a sequência feita no Word, informe o número do próximo ofício do ano (ex.: 7, se o último foi o 06/2026).

| Livro de ofícios | Novo ofício |
|---|---|
| ![Livro de ofícios](docs/telas/43-oficios-livro.jpg) | ![Novo ofício](docs/telas/44-oficio-novo.jpg) |

| Aprovação | Configuração |
|---|---|
| ![Aprovação do ofício](docs/telas/45-oficio-aprovacao.jpg) | ![Configuração dos ofícios](docs/telas/47-oficios-configuracao.jpg) |

![Ofício aprovado em PDF](docs/telas/46-oficio-pdf.jpg)

#### Apresentação de crianças

A apresentação é o registro oficial, e **é o único lugar onde o certificado de apresentação é emitido**.

- **Cadastro do bebê** na própria tela: nome, CPF (da certidão), data de nascimento e sexo. A criança fica na categoria *Criança*: não conta como membro, não entra nos relatórios de membros nem recebe carteirinha. A filiação é preenchida a partir dos pais.
- **Mãe obrigatória:** vinculada ao cadastro, se for membro, ou pelo nome completo. O pai é opcional.
- **Certificado numerado** (ex.: `AP-2026-000007`), na arte oficial (azul para menino, rosa para menina). Traz filiação, data, congregação, pastor, número da via e data de emissão.
- **Rastreável (mesmo fluxo dos demais documentos):**
  - Cada emissão é uma via registrada; uma nova emissão vira **2ª via**, com histórico.
  - O certificado aparece em **Documentos** e no portal da **criança, do pai e da mãe**.
  - Alterar os dados depois da emissão fica na auditoria.
  - Uma apresentação com certificado emitido não é excluída, só **cancelada**, com motivo.

![Apresentações](docs/telas/24-admin-apresentacoes.jpg)

![Certificado de apresentação](docs/telas/24b-certificado-apresentacao.jpg)

#### Relatórios

Relatórios de membros em PDF, geral ou por congregação.

![Relatórios](docs/telas/25-admin-relatorios.jpg)

#### Modelos de documento

Modelos JasperReports com versão, situação e o perfil que pode emitir cada um.

![Modelos de documento](docs/telas/26-admin-modelos-documento.jpg)

#### Tipos de consagração

![Tipos de consagração](docs/telas/27-admin-tipos-consagracao.jpg)

### Administração e auditoria

#### Usuários

Usuários do sistema com perfil (Administrador, Pastor, Secretário ou Membro), e-mail, congregação e situação.

- **E-mail:** usado em "Esqueci minha senha" e nos avisos da conta. Não pode se repetir entre usuários.
- **Conta nova sem senha:** com o envio de e-mails ligado, a secretaria pode deixar a senha em branco e marcar "Enviar e-mail para o usuário definir a própria senha". O usuário recebe o login e um link (válido por 48 horas). Na edição, "Enviar link de nova senha" reenvia o link.
- **Senha:** mínimo de 8 caracteres, com letras e números (vale também para Minha conta e para os links do e-mail).
- **Vínculo com membro:** o CPF do membro é obrigatório para Membro, Pastor e Secretário e opcional para o Administrador. Com o vínculo, o usuário ganha a "Minha área" do portal.

![Usuários](docs/telas/28-admin-usuarios.jpg)

#### Servidor de e-mail

Somente o administrador acessa (**Administração > Servidor de e-mail**). A tela define a conta que envia os e-mails do sistema: conta criada, esqueci minha senha e senha alterada.

- **Gmail:** servidor `smtp.gmail.com`, porta 587, STARTTLS. Use uma **senha de app** (Conta Google > Segurança > Senhas de app, com a verificação em duas etapas ligada), não a senha normal. O limite é de cerca de 500 envios por dia.
- **Hostinger:** servidor `smtp.hostinger.com`, porta 465, SSL. Crie uma caixa no painel da Hostinger (ex.: `nao-responda@adealgo.com.br`) e use o endereço completo e a senha dessa caixa. Os e-mails saem com o domínio da igreja.
- **Senha da conta:** fica **cifrada** no banco com a chave do servidor (`MINISTERIO_CHAVE_SEGREDOS`) e nunca volta para a tela. Para mantê-la ao salvar de novo, deixe o campo em branco.
- **Ordem recomendada:** salvar, enviar o **e-mail de teste**, conferir que chegou e só então marcar **Enviar e-mails**. Se o servidor recusar o usuário ou a senha, a tela explica o motivo.

![Servidor de e-mail](docs/telas/39-admin-servidor-email.jpg)

#### Controle de acesso

Matriz de permissões por perfil: visualizar, editar e emitir em cada módulo. Inclui a permissão **"Ver todas as congregações"**.

![Controle de acesso](docs/telas/29-admin-controle-acesso.jpg)

#### Log de emissões e auditorias

Registro de cada documento emitido, das tentativas de login e das alterações críticas, com filtros.

| Log de emissões | Autenticação | Auditoria geral |
|---|---|---|
| ![Log de emissões](docs/telas/30-admin-log-emissoes.jpg) | ![Log de autenticação](docs/telas/31-admin-log-autenticacao.jpg) | ![Auditoria](docs/telas/32-admin-auditoria.jpg) |

#### Privacidade (LGPD)

Menu **Administração › Privacidade (LGPD)**, com permissão própria (**termo_privacidade**) no Controle de Acesso. No começo só o administrador acessa. Ao liberar para pastor ou secretário:

- **Visualizar:** termo em vigor, versões, aceites e pedidos do titular.
- **Editar:** rascunho do termo, encarregado, aceite em papel e atender pedidos.
- **Emitir:** publicar uma nova versão.

O termo é **versionado**:

1. **Rascunho.** Parte da versão em vigor. Os membros continuam vendo a versão em vigor até a publicação. Uma linha em branco separa os parágrafos e `**texto**` fica em negrito; HTML digitado aparece como texto.
2. **Pré-visualizar e comparar.** A comparação com a versão em vigor mostra riscado o que sai e em verde o que entra.
3. **Publicar.** É preciso dizer o que mudou. Há duas opções:
   - **Exigir novo aceite:** todos os membros, inclusive quem já está logado, são levados ao termo no próximo acesso e veem o resumo das mudanças;
   - **Ajuste sem novo aceite:** os aceites anteriores continuam valendo.

   Com novo aceite, a opção **Avisar por e-mail** (marcada por padrão) põe na fila um aviso para os membros com acesso ao portal, com o resumo das mudanças e o botão **Ler o termo**. Por ser um aviso do serviço, vai também para quem não recebe comunicados. O texto fica em **Comunicação › Modelos de e-mail** ("Termo de privacidade atualizado").

Uma versão publicada não muda mais. A aba **Versões** guarda todas, com quem publicou, quando e o texto de cada uma. Cada publicação também entra na **Auditoria geral**.

Na aba **Encarregado (DPO)** ficam o nome, o e-mail e o telefone do encarregado pelos dados (pessoa ou setor). Eles aparecem no fim do termo, no portal.

A aba **Aceites** mostra a situação de cada membro (sem crianças e sem desligados):

- **Números:** membros, quantos aceitaram a versão exigida, quantos estão com novo aceite pendente ou sem aceite, quantos não autorizam o uso de imagem e quantos não querem foto na carteirinha.
- **Filtros:** nome, congregação, situação e "não autorizam imagem". O botão de histórico mostra todos os aceites do membro.
- **Planilhas (CSV):** a tabela com os filtros e a **lista para a mídia**, só com quem não autoriza o uso de imagem, por congregação. As planilhas não levam CPF. O link `admin/privacidade.xhtml?aba=imagem` abre a aba já filtrada.
- **Aceite em papel:** para quem assinou o termo impresso na secretaria. Informe o membro, a versão assinada, a data da assinatura e as escolhas (foto, imagem, e-mails), e anexe o termo assinado digitalizado (PDF, JPG ou PNG, até 10 MB; o tipo é conferido pelo conteúdo do arquivo). O aceite fica como **Papel**, com quem registrou e quando, vale no portal como o aceite do próprio membro e entra na **Auditoria geral**. O termo assinado abre pela tabela, pelo histórico e pela ficha do membro.

O histórico de cada membro tem o **comprovante do aceite** em PDF: nome, CPF mascarado, versão aceita, como e quando (portal, com usuário e IP, ou papel, com quem registrou), as escolhas e o **texto integral** da versão aceita. O membro baixa o dele no portal.

A aba **Pedidos** reúne os **pedidos do titular** (LGPD, art. 18):

- **Tipos:** cópia dos dados, correção, exclusão, informação sobre o uso e outro. Correção e "outro" pedem a descrição.
- **Origem:** o membro pede pelo portal, em **Privacidade**, ou a secretaria registra o pedido feito pessoalmente (**Registrar pedido feito na secretaria**).
- **Prazo:** 15 dias. A tabela vem ordenada pelo prazo e mostra "faltam N dias", "vence hoje" ou "vencido há N dias". O filtro mostra os em aberto, os vencidos, os encerrados ou todos. O link `admin/privacidade.xhtml?aba=pedidos` abre a aba.
- **Atender:** situação (aberto, em andamento, atendido, recusado), responsável e a **resposta ao membro**, obrigatória para encerrar. O membro vê a resposta no portal. Para a cópia dos dados, a linha tem o atalho para a **ficha cadastral** em PDF.
- **Início do painel:** quem vê a privacidade vê quantos pedidos estão em aberto e quantos estão vencidos.

Cada pedido e cada atendimento entram na **Auditoria geral**.

Pastor e secretário veem e registram só os membros da própria congregação, salvo com "Ver todas as congregações".

| Aceites | Aceite em papel |
|---|---|
| ![Aceites do termo](docs/telas/52-admin-privacidade-aceites.jpg) | ![Aceite em papel](docs/telas/53-admin-aceite-papel.jpg) |

| Pedidos do titular | Comprovante do aceite |
|---|---|
| ![Pedidos do titular](docs/telas/58-admin-privacidade-pedidos.jpg) | ![Comprovante do aceite](docs/telas/59-comprovante-lgpd.jpg) |

Na **ficha do membro**, um selo mostra se ele aceitou a versão exigida, se o novo aceite está pendente ou se ainda não aceitou, junto com as autorizações de foto, de imagem e de e-mails. O botão **Histórico** lista todos os aceites, com versão, origem, usuário e IP. O selo é **só leitura**: as escolhas são do próprio membro, no portal.

| Termo: rascunho e comparação | Versões | Selo na ficha do membro |
|---|---|---|
| ![Rascunho e comparação](docs/telas/48-admin-privacidade-termo.jpg) | ![Versões do termo](docs/telas/49-admin-privacidade-versoes.jpg) | ![Selo LGPD na ficha](docs/telas/50-admin-membro-lgpd.jpg) |

#### Comunicação por e-mail

Menu **Comunicação**, com permissão própria (**comunicacao**) no Controle de Acesso. No começo só o administrador acessa. Ao liberar para pastor ou secretário:

- **Visualizar:** modelos e histórico.
- **Editar:** textos e parâmetros.
- **Emitir:** lançar envios.

Pastor e secretário só enviam para a própria congregação e veem só os envios que lançaram.

**Modelos de e-mail.** Todo e-mail do sistema tem um texto padrão que pode ser personalizado: assunto, mensagem e texto do botão. A tela mostra a pré-visualização com dados de exemplo e tem os botões "Enviar teste para mim" e "Restaurar padrão". As variáveis entre chaves duplas viram os dados de cada pessoa: `{{nome}}`, `{{primeiro_nome}}`, `{{congregacao}}`, `{{igreja}}` e, no evento, `{{evento_titulo}}`, `{{evento_data}}`, `{{evento_local}}` e `{{evento_descricao}}`. Variável que não existe no modelo é recusada ao salvar.

| Modelo | Quando sai |
|---|---|
| Aniversário | Todo dia, na hora definida, para os aniversariantes. Quem nasceu em 29/02 recebe em 28/02 nos anos não bissextos. |
| Boas-vindas ao membro | Quando um membro é cadastrado com e-mail. |
| Novo evento | Quando um evento é cadastrado (vai para a congregação do evento ou para todos) ou ao divulgar um evento. |
| Comunicado | Texto inicial dos comunicados lançados em Envios. |
| Termo de privacidade atualizado | Ao publicar uma versão do termo que exige novo aceite, com "Avisar por e-mail" marcado. Vai para os membros com acesso ao portal. |
| Conta criada, Esqueci minha senha, Senha alterada | E-mails da conta, sempre enviados. |

Os três primeiros têm uma chave **liga/desliga** e começam **desligados**.

| Modelos de e-mail | Edição com pré-visualização |
|---|---|
| ![Modelos de e-mail](docs/telas/41-admin-modelos-email.jpg) | ![Edição de modelo](docs/telas/42-admin-modelo-edicao.jpg) |

**Envios de e-mail.**

- **Lançar:** um comunicado ou a divulgação de um evento (a lista de eventos tem o botão "Divulgar por e-mail").
- **Para quem:** todos os membros, membros de uma congregação, usuários do sistema ou só você (teste).
- **Conferir antes:** "Conferir destinatários e prévia" mostra quantas pessoas recebem e como o e-mail chega.
- **Fila:** os e-mails saem em segundo plano, com pausa entre um e outro e limite por dia (o restante segue no dia seguinte). A fila continua depois de reiniciar o servidor.
- **Histórico:** mostra o progresso de cada envio e quem recebeu, com os botões cancelar e "reenviar os que falharam".

![Envios de e-mail](docs/telas/40-admin-envios-email.jpg)

**Parâmetros:** hora do e-mail de aniversário (padrão 08:00), limite por dia (padrão 450, abaixo do limite do Gmail) e pausa entre e-mails (padrão 1,5 s).

**Quem recebe:** membros com e-mail na ficha, que aceitam receber, de congregação ativa e não desligados. Crianças não recebem. O e-mail do membro fica na ficha (secretaria) e em **Meu Perfil** (o próprio membro).

**LGPD:** aniversário, eventos e comunicados levam o link **"não quero mais receber"**, que pede confirmação antes de gravar. O membro também escolhe em **Privacidade**, no portal; essa opção entrou no termo, que por isso pede um novo aceite. Os e-mails da conta não têm descadastro.

#### Minha conta e "Esqueci minha senha"

- **Minha conta:** clicar no nome do usuário, no topo de qualquer tela, abre a página. Lá ele altera nome, e-mail e foto e troca a senha, informando a senha atual. Login, perfil, congregação e vínculo de membro aparecem só para leitura: quem altera é a secretaria.
- **Esqueci minha senha:** fica na tela de login. O usuário informa o login ou o e-mail e recebe um link válido por 1 hora.
  - A resposta é sempre a mesma, para não revelar quais contas existem.
  - São no máximo 3 pedidos por hora para cada conta.
  - O link vale uma vez, e o banco guarda só o hash do token.
  - Ao trocar a senha, os outros links pendentes deixam de valer e o usuário recebe o aviso "sua senha foi alterada".
  - Sem servidor de e-mail ligado, a tela orienta procurar a secretaria.

![Minha conta](docs/telas/38-minha-conta.jpg)

#### No celular

O painel também funciona no celular. O menu lateral vira um menu recolhível.

![Painel no celular](docs/telas/33-admin-celular.jpg)

---

## Portal do membro

O membro entra com o próprio login e usa o mesmo menu lateral do painel.

Administrador, pastor e secretário também podem ser membros. Se o usuário tiver um cadastro de membro vinculado (em **Usuários**), o menu do painel ganha a seção **Minha área** com Meu Perfil, Minha Carteirinha, Meus Documentos e Privacidade, e o início do painel mostra os mesmos atalhos. No portal, um link leva de volta ao **Painel administrativo**. Esses perfis também aceitam o termo de privacidade no primeiro acesso ao portal e emitem, baixam e adicionam à Wallet a própria carteirinha, como qualquer membro. Sem cadastro vinculado, as páginas do portal levam de volta ao painel.

| Início | Meu Perfil |
|---|---|
| ![Início do portal](docs/telas/34-membro-inicio.jpg) | ![Meu perfil](docs/telas/35-membro-perfil.jpg) |

**Privacidade (LGPD)**: no primeiro acesso, o membro lê o termo de privacidade e confirma as autorizações:

- foto na carteirinha;
- uso de imagem em cultos, transmissões e redes sociais.

As duas vêm marcadas por padrão. Enquanto o termo não for aceito, as páginas do portal levam a ele. As escolhas podem ser mudadas depois pelo menu **Privacidade**. Cada aceite fica registrado com data, usuário, IP e versão do termo.

O texto inicial é um **modelo**, a ser padronizado com o jurídico. Ele é editado no painel, em [Privacidade (LGPD)](#privacidade-lgpd). Quando uma nova versão exige novo aceite, o portal mostra ao membro o que mudou desde o último aceite.

![Novo aceite do termo](docs/telas/51-membro-novo-aceite.jpg)

Na mesma página ficam o link **Baixar o comprovante do seu aceite (PDF)** e a seção **Seus direitos sobre os seus dados**. Nela o membro pede uma cópia dos dados, a correção de um dado errado, a exclusão de dados ou informações sobre o uso, e acompanha cada pedido: situação, prazo de resposta (15 dias) e a resposta da igreja. Essa seção não depende do aceite do termo. Para evitar excessos, cada membro tem até 5 pedidos em andamento ao mesmo tempo.

![Seus direitos no portal](docs/telas/60-membro-pedidos.jpg)

**Carteirinha**: a carteirinha digital mostra nome, função, congregação, número, validade, situação e o QR Code de conferência. O membro emite ou renova a própria carteirinha e baixa o PDF. A carteirinha da Convenção só fica disponível para quem tem os registros CGADB e CONFRAMADEGO no cadastro. Os cartões da Google Wallet e da Apple Wallet vêm numa próxima etapa e serão oferecidos só a membros com usuário no portal.

![Carteirinha](docs/telas/36-membro-carteirinha.jpg)

**Meus Documentos** reúne:

- os certificados e documentos emitidos para o membro;
- os certificados de apresentação dos filhos (ou o próprio, quando o membro foi apresentado), na via mais recente emitida pela secretaria;
- o histórico de carteirinhas.

Cada membro só consegue baixar os próprios documentos.

![Meus documentos](docs/telas/37-membro-documentos.jpg)

---

## Perfis e permissões

| Perfil | Acesso |
|---|---|
| **Administrador** | Todo o painel. Somente ele acessa controle de acesso, auditorias e modelos de documento. |
| **Pastor** | Painel conforme a matriz de **Controle de Acesso**. |
| **Secretário** | Painel conforme a matriz de **Controle de Acesso**. |
| **Recepção** | Porteiro: só a página **Registrar visitante**, da própria congregação. |
| **Membro** | Somente o portal do membro. |

Qualquer perfil vinculado a um cadastro de membro também tem o portal do membro para os próprios dados (seção **Minha área**).

Regras para pastor e secretário:

- Veem apenas a **própria congregação**: membros, documentos, carteirinhas, apresentações, pastores, cultos, eventos, relatórios e log de emissões.
- Com a permissão **"Ver todas as congregações"**, veem todas.
- Emitem carteirinhas somente para membros da própria congregação, e só se tiverem a permissão de *Emitir*.
- Para que o filtro por congregação funcione, os usuários com esses perfis precisam ter a congregação vinculada no cadastro.

---

## Identidade visual

Site, painel, portal, e-mails e carteirinhas digitais usam a cor **Marsala** (Pantone 18-1438, `#955251`).

| Uso | Cor |
|-----|-----|
| Marsala (cor principal, botões e links) | `#955251` |
| Marsala escuro (cabeçalho, menu lateral, rodapé) | `#351c1c` / `#4e2928` |
| Dourado-areia (destaques sobre fundo escuro) | `#d9b77e` |
| Texto | `#2b2322` |
| Fundo das páginas | `#f6f1f0` |
| Sucesso / aviso / erro | `#2e7d4f` / `#b7791f` / `#b42318` |

- A paleta completa fica em variáveis CSS no início de `src/main/webapp/resources/css/adealgo.css`. Use as variáveis em vez de cores soltas no código.
- Os componentes PrimeFaces usam o tema próprio **marsala** (`src/main/webapp/resources/primefaces-marsala/theme.css`). Ele é gerado a partir do tema Saga pelo script `ferramentas/gerar_tema_marsala.py`. Ao atualizar o PrimeFaces, rode o script de novo.
- **Ícones:** somente [PrimeIcons](https://primereact.org/icons/) (`<i class="pi pi-..."></i>` ou `icon="pi pi-..."`).
- **Emojis:** não são usados em nenhuma tela, mensagem ou e-mail do sistema.
- Exceções: as cores oficiais das redes sociais (nos botões flutuantes) e o botão preto da Apple e do Google Wallet.

## Tecnologias

- **Java 21**, **Spring Boot 3.5** (aplicação empacotada como WAR `ROOT.war`)
- **JoinFaces 5.5** com **Jakarta Faces 4 (Mojarra)** e **PrimeFaces 16**
- **Spring Security 6**: login, perfis e filtro de permissões por URL
- **Spring Data JPA / Hibernate 6.6** com **MySQL** (testado também em MariaDB)
- **Flyway** para as migrações do banco (`src/main/resources/db/migration` e `src/main/java/db/migration`)
- **JasperReports** para carteirinhas, certificados, cartas e relatórios em PDF
- **ZXing** para o QR Code de conferência das carteirinhas
