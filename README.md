# GlauWeb Instant (PWA)

Ferramenta web leve que permite colar código HTML e gerar automaticamente um arquivo `.html` para download. Esta versão funciona também como **PWA (Progressive Web App)**, podendo ser instalada em dispositivos móveis e utilizada offline.

## Visão geral

O **GlauWeb Instant** foi criado para simplificar o processo de transformar código HTML gerado por IA ou por editores em um arquivo `.html` pronto para uso.

O usuário apenas cola o código no campo de texto e toca em **Salvar**, e o arquivo é automaticamente gerado e baixado no dispositivo.

Nesta versão, o aplicativo também pode ser **instalado no celular ou tablet**, funcionando como um app offline graças ao suporte a **Service Worker**.

## Funcionalidades

- Interface simples e otimizada para mobile
- Campo para colar código HTML
- Contador automático de caracteres
- Botão para limpar o campo rapidamente
- Geração automática de arquivo `.html`
- Download direto no dispositivo
- Nome do arquivo gerado automaticamente a partir de:
  - `<title>` da página
  - ou `<h1>` caso não exista título
- Normalização automática do nome do arquivo
- Inserção automática de `<meta charset="UTF-8">` caso esteja ausente
- Suporte a **PWA (Progressive Web App)**
- Funcionamento **offline com Service Worker**

## Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript puro (Vanilla JS)
- Progressive Web App (PWA)
- Service Worker
- Web App Manifest

## Como funciona

1. O usuário cola o código HTML no campo de texto.
2. O sistema verifica se há conteúdo válido.
3. O script tenta extrair um nome de arquivo a partir de:
   - `<title>`
   - ou `<h1>`
4. O código verifica se existe `<meta charset="UTF-8">`.
5. Caso não exista, ele é automaticamente inserido.
6. O conteúdo é convertido em um **Blob HTML**.
7. Um link de download é criado dinamicamente.
8. O arquivo é baixado automaticamente como `.html`.

Todo o processo acontece **localmente no navegador**, sem envio de dados para servidores.

## Estrutura do projeto

Arquivos principais do projeto:

- `index.html` — interface e lógica da aplicação
- `manifest.json` — configuração do Progressive Web App
- `sw.js` — Service Worker para funcionamento offline
- `icon-192.png` — ícone do aplicativo

## Como usar

1. Clone ou baixe o repositório:

```
git clone <URL_DO_REPOSITORIO>
```

2. Abra o arquivo `index.html` no navegador.

3. Cole o código HTML no campo de texto.

4. Clique ou toque em **SALVAR COMO .HTML**.

5. O arquivo será gerado automaticamente.

## Instalação como aplicativo (PWA)

Em dispositivos compatíveis:

1. Abra a página no navegador.
2. Escolha **Adicionar à tela inicial** ou **Instalar aplicativo**.
3. O GlauWeb Instant poderá ser usado como um app independente.

## Casos de uso

Esta ferramenta é útil para:

- converter HTML gerado por IA em arquivos reais
- salvar protótipos rapidamente
- ensinar HTML em ambientes educacionais
- gerar páginas simples para testes
- trabalhar com snippets HTML

## Possíveis melhorias

- pré-visualização da página antes do download
- modo escuro
- compressão automática de HTML
- suporte a múltiplos arquivos
- integração com armazenamento local
- exportação em `.zip`

## Público-alvo

- professores
- estudantes
- desenvolvedores iniciantes
- usuários de ferramentas de IA que geram HTML

## Créditos

Desenvolvido pelo **Professor Glauber Santiago — DAC/UFSCar**.

Links:

- https://servidores.ufscar.br/glauber/
- https://sites.google.com/view/glauberia

## Licença

Este projeto pode ser distribuído sob a licença de sua escolha (por exemplo, MIT).
