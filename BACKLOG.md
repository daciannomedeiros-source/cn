# Backlog — o que fica para melhorar

Versão atual: **0.2.0** (núcleo + aplicativo com painel e janela de saída; fala simulada por texto). Cada rodada fecha uma parte e abre a próxima.

## Próximas rodadas (ordem sugerida)
1. **Adaptador do Holyrics** — ler Bíblia e músicas pela API Server (ações de Bíblia ainda a confirmar na documentação). Cache local em SQLite.
2. **Contagem de versículos por capítulo** — validar "Salmo 23:50" e rejeitar versículos que não existem (hoje o limite é 176).
3. **Entrada de áudio + transcrição em streaming** — nuvem como principal e Whisper local como reserva automática.
4. **Saída NDI com alfa** para OBS/vMix/Arena (a janela em tela cheia já existe).
5. **Painel do operador, parte 2** — lista do dia, trocar candidatos com um clique, indicador de saúde da conexão, atalhos configuráveis, Stream Deck/MIDI.
6. **Citação sem referência** — busca por palavras na base do Holyrics.
7. **Paráfrase + segunda análise por IA** — só nos casos difíceis, com níveis de confiança.
8. **Louvor** — acompanhar o canto pelas letras do Holyrics/ProPresenter, com controle manual.
9. **Instaladores** — Windows e Mac (um build em cada sistema).

## Melhorias conhecidas no núcleo
- Abreviações curtas ("Mt", "Sl", "Rm") e variações de pronúncia do reconhecedor de voz.
- "Jo" é tratado como João; "Jó" só funciona com o acento (transcrição precisa vir acentuada).
- Livros de capítulo único com intervalo ("Judas 1 a 5") ainda não tratados.
- Duas referências coladas ("Romanos 8 1 João 3 16") podem ser lidas de forma ambígua.
- Confiança é fixa (0.95 com versículo, 0.75 só capítulo); falta calibrar com áudio real.
- Janela de duplicidade e tempo de exibição precisam de ajuste fino no culto.
- Comandos de voz: avaliar palavra de ativação por padrão para evitar disparo acidental.

## Decisões já tomadas
- Modo AUTO envia tudo que for detectado; o operador pode contribuir e corrigir.
- Atraso de cancelamento (autoDelayMs) existe, desligado por padrão.

## Melhorias conhecidas no aplicativo (v0.2.0)
- Não foi testado rodando em Windows/Mac: a primeira rodada serve para achar ajustes (tela cheia em segundo monitor, atalhos, tamanhos).
- A saída mostra só a referência (ex.: João 3:16); o texto da Bíblia depende do Holyrics.
- Sem ícone próprio do aplicativo (usa o ícone padrão do Electron).
- Instalador sem assinatura (aviso do SmartScreen no Windows e do Gatekeeper no Mac).
- No Auto com atraso de cancelamento, o painel ainda não mostra a contagem regressiva.
- Janela de saída: falta escolher fundo (preto ou transparente) e estilo do texto.
