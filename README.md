# Viewer SketchUp com React + PlayCanvas

App de estudo para visualizar projetos de arquitetura exportados em `.glb` diretamente no navegador.

## O que este projeto faz

- Upload local de arquivo `.glb`
- Validacao de extensao e tamanho do arquivo
- Viewer 3D com PlayCanvas
- Controles de camera:
	- arrastar com botao esquerdo: orbita
	- roda do mouse: zoom

## Requisitos

- Node.js 20+ (recomendado LTS)
- npm

## Como rodar

```bash
npm install
npm run dev
```

Depois abra o endereco mostrado no terminal (normalmente `http://localhost:5173`).

## Build de producao

```bash
npm run build
npm run preview
```

## Fluxo SketchUp -> Web

1. No SketchUp, exporte o modelo para `.glb`.
2. Caso sua versao nao exporte GLB direto, converta via Blender para `.glb`.
3. No app, envie o arquivo na area de upload.
4. Use orbita/zoom para revisar volumes e espacamento do projeto.

## Observacoes

- O upload atual e local, sem backend (nao salva em servidor).
- Para uso real em producao, o proximo passo e criar API de upload com autenticacao e armazenamento seguro (S3, Blob Storage etc.).
