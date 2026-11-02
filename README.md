# Financeiro do lar

App de finanças pessoais (Melqui e Daniele). Este repositório tem **só o código**; os dados ficam no repositório privado `financeiro-dados`.

- Melqui: https://melquiraraujo-create.github.io/Financeiro/
- Daniele: https://melquiraraujo-create.github.io/Financeiro/daniele.html

## Como configurar (uma vez)
1. **Pages**: Settings → Pages → Source: *Deploy from a branch* → Branch `main` / pasta `/ (root)` → Save. Em 1–2 minutos o endereço acima funciona.
2. **Repositório de dados**: crie `financeiro-dados` como **Private** (marque "Add a README").
3. **Token**: foto do perfil → Settings → Developer settings → Personal access tokens → **Fine-grained tokens** → Generate new token:
   - Repository access: *Only select repositories* → `financeiro-dados`
   - Permissions → Repository permissions → **Contents: Read and write**
   - Expiration: o prazo que preferir (ex.: 1 ano). Copie o token (`github_pat_…`).
4. **Levar seus dados**: no HTML antigo, Dados → Baixar backup (.json). No site novo: Restaurar um backup → depois Dados → Sincronizar com o GitHub… → cole o token → Criar.
5. **Celular**: abra o endereço, menu do navegador → *Adicionar à tela inicial*. Na primeira vez toque em "Conectar ao GitHub" e cole o mesmo token.

## Como funciona
- Cada alteração é salva neste aparelho e enviada ao GitHub em ~2 s (status "☁ salvo" no topo). Cada envio vira um commit em `financeiro-dados`, então o histórico serve de backup.
- Se dois aparelhos alterarem ao mesmo tempo, o app pergunta qual versão manter.
- Sem internet o app continua funcionando e envia na próxima alteração com conexão.
- Leitura de fatura em PDF e o OCR usam bibliotecas baixadas na hora (precisa de internet).
