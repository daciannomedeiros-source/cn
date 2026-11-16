# Versículo ao Vivo — v0.2.0

Aplicativo para Windows e Mac: painel do operador (Manual / Auto ao vivo, preview, Take, Limpar), janela de saída em tela cheia e detector de referências bíblicas em português. Nesta versão a fala é **simulada por texto**; a transcrição, o Holyrics e o NDI vêm nas próximas rodadas (veja BACKLOG.md).

## Gerar os instaladores (.exe e .dmg) no GitHub
1. Crie um repositório novo e privado em github.com (botão "New").
2. Descompacte este zip e envie **todos os arquivos** para o repositório (Add file > Upload files).
   - A pasta `.github` é oculta. Se ela não subir, no GitHub use Add file > Create new file, digite `.github/workflows/build.yml` como nome e cole o conteúdo de `COLE-NO-GITHUB-build.yml`.
3. Abra a aba **Actions**, escolha **Gerar instaladores** e clique em **Run workflow**.
4. Espere uns 5 a 10 minutos. Na página da execução, em **Artifacts**, baixe `instalador-windows-latest` (.exe) e `instalador-macos-latest` (.dmg).

## Avisos na primeira abertura
- **Windows:** o SmartScreen pode avisar "aplicativo não reconhecido". Clique em Mais informações > Executar assim mesmo.
- **Mac:** o app não é assinado pela Apple. Arraste para Aplicativos, clique com o botão direito > Abrir > Abrir. Se aparecer bloqueio, vá em Ajustes do Sistema > Privacidade e Segurança > Abrir mesmo assim.

## Rodar no computador (desenvolvimento)
    npm install
    npm start
    npm test
