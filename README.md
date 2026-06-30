# Table JSON

**API gratuita e estática de dados de referência do Brasil em JSON** — municípios IBGE, UF, DDD, DDI, CFOP, CNAE, ICMS, CSOSN, CRT, Simples Nacional, ISSQN municipal, países, moedas, cores, unidades de medida e cadastros de pessoas.

[![Site](https://img.shields.io/badge/site-table--json.netlify.app-blue)](https://table-json.netlify.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![JSON](https://img.shields.io/badge/format-JSON-orange)](https://table-json.netlify.app/)
[![Brasil](https://img.shields.io/badge/dados-Brasil-yellow)](https://table-json.netlify.app/)

> Fonte pública de tabelas e listas brasileiras prontas para consumo em aplicações web, mobile, ERP, emissão de notas fiscais e sistemas tributários — sem autenticação, sem rate limit, hospedada no Netlify.

**Demo ao vivo:** [https://table-json.netlify.app/](https://table-json.netlify.app/)

---

## Sobre o projeto

O **Table JSON** centraliza informações de referência que mudam com pouca frequência, disponibilizando-as como arquivos `.json` acessíveis via HTTP. A ideia é evitar que cada aplicação mantenha sua própria cópia de tabelas como municípios, CFOP, CNAE ou listas cadastrais.

Características principais:

- **Gratuito e aberto** — uso livre sob licença MIT
- **Sem backend** — arquivos estáticos servidos pelo Netlify
- **CORS liberado** — consumível diretamente do navegador ou de qualquer cliente HTTP
- **URLs estáveis** — padrão `/v1/{categoria}/{arquivo}.json`
- **Catálogo navegável** — página inicial com todos os endpoints documentados

### Palavras-chave

`json` · `api json` · `dados json brasil` · `municipios ibge json` · `uf json` · `ddd json` · `cfop json` · `cnae json` · `csosn json` · `icms json` · `crt json` · `simples nacional json` · `issqn json` · `paises json` · `moedas json` · `cores json` · `unidade de medida json` · `fonte de dados json` · `tabelas fiscais json`

---

## Como usar

Basta fazer uma requisição `GET` na URL do endpoint desejado. Não é necessário token, header especial ou cadastro.

### JavaScript (fetch)

```javascript
const response = await fetch('https://table-json.netlify.app/v1/ibge/municipios.json');
const municipios = await response.json();
console.log(municipios);
```

### cURL

```bash
curl https://table-json.netlify.app/v1/impostos/cfop.json
```

### Importação em aplicações

Os arquivos podem ser consumidos em tempo de execução (fetch/axios) ou baixados e versionados no seu projeto, conforme a necessidade.

**Base URL:** `https://table-json.netlify.app`

---

## Catálogo de endpoints

### IBGE

Dados oficiais do IBGE: municípios, unidades federativas, DDD e DDI.

| Recurso | Endpoint |
|---------|----------|
| Municípios | [`/v1/ibge/municipios.json`](https://table-json.netlify.app/v1/ibge/municipios.json) |
| UF (estados) | [`/v1/ibge/uf.json`](https://table-json.netlify.app/v1/ibge/uf.json) |
| DDD | [`/v1/ibge/ddd.json`](https://table-json.netlify.app/v1/ibge/ddd.json) |
| DDI | [`/v1/ibge/ddi.json`](https://table-json.netlify.app/v1/ibge/ddi.json) |

#### Cidades por UF

Municípios separados por estado (sigla da UF no nome do arquivo):

| UF | Endpoint |
|----|----------|
| AC | [`/v1/ibge/ac.json`](https://table-json.netlify.app/v1/ibge/ac.json) |
| AL | [`/v1/ibge/al.json`](https://table-json.netlify.app/v1/ibge/al.json) |
| AP | [`/v1/ibge/ap.json`](https://table-json.netlify.app/v1/ibge/ap.json) |
| AM | [`/v1/ibge/am.json`](https://table-json.netlify.app/v1/ibge/am.json) |
| BA | [`/v1/ibge/ba.json`](https://table-json.netlify.app/v1/ibge/ba.json) |
| CE | [`/v1/ibge/ce.json`](https://table-json.netlify.app/v1/ibge/ce.json) |
| DF | [`/v1/ibge/df.json`](https://table-json.netlify.app/v1/ibge/df.json) |
| ES | [`/v1/ibge/es.json`](https://table-json.netlify.app/v1/ibge/es.json) |
| GO | [`/v1/ibge/go.json`](https://table-json.netlify.app/v1/ibge/go.json) |
| MA | [`/v1/ibge/ma.json`](https://table-json.netlify.app/v1/ibge/ma.json) |
| MT | [`/v1/ibge/mt.json`](https://table-json.netlify.app/v1/ibge/mt.json) |
| MS | [`/v1/ibge/ms.json`](https://table-json.netlify.app/v1/ibge/ms.json) |
| MG | [`/v1/ibge/mg.json`](https://table-json.netlify.app/v1/ibge/mg.json) |
| PA | [`/v1/ibge/pa.json`](https://table-json.netlify.app/v1/ibge/pa.json) |
| PB | [`/v1/ibge/pb.json`](https://table-json.netlify.app/v1/ibge/pb.json) |
| PR | [`/v1/ibge/pr.json`](https://table-json.netlify.app/v1/ibge/pr.json) |
| PE | [`/v1/ibge/pe.json`](https://table-json.netlify.app/v1/ibge/pe.json) |
| PI | [`/v1/ibge/pi.json`](https://table-json.netlify.app/v1/ibge/pi.json) |
| RJ | [`/v1/ibge/rj.json`](https://table-json.netlify.app/v1/ibge/rj.json) |
| RN | [`/v1/ibge/rn.json`](https://table-json.netlify.app/v1/ibge/rn.json) |
| RS | [`/v1/ibge/rs.json`](https://table-json.netlify.app/v1/ibge/rs.json) |
| RO | [`/v1/ibge/ro.json`](https://table-json.netlify.app/v1/ibge/ro.json) |
| RR | [`/v1/ibge/rr.json`](https://table-json.netlify.app/v1/ibge/rr.json) |
| SC | [`/v1/ibge/sc.json`](https://table-json.netlify.app/v1/ibge/sc.json) |
| SP | [`/v1/ibge/sp.json`](https://table-json.netlify.app/v1/ibge/sp.json) |
| SE | [`/v1/ibge/se.json`](https://table-json.netlify.app/v1/ibge/se.json) |
| TO | [`/v1/ibge/to.json`](https://table-json.netlify.app/v1/ibge/to.json) |

---

### Impostos

Tabelas fiscais para emissão de notas fiscais e sistemas tributários.

| Recurso | Endpoint |
|---------|----------|
| ICMS | [`/v1/impostos/icms.json`](https://table-json.netlify.app/v1/impostos/icms.json) |
| CRT | [`/v1/impostos/crt.json`](https://table-json.netlify.app/v1/impostos/crt.json) |
| CFOP | [`/v1/impostos/cfop.json`](https://table-json.netlify.app/v1/impostos/cfop.json) |
| CSOSN | [`/v1/impostos/csosn.json`](https://table-json.netlify.app/v1/impostos/csosn.json) |
| CNAE | [`/v1/impostos/cnae.json`](https://table-json.netlify.app/v1/impostos/cnae.json) |

---

### Serviços

Tabelas de serviços: LC 116/2003, Simples Nacional e ISSQN municipal.

| Recurso | Endpoint |
|---------|----------|
| Simples Nacional (LC 116/2003) | [`/v1/servicos/simples-nacional.json`](https://table-json.netlify.app/v1/servicos/simples-nacional.json) |
| São Paulo — SP (IBGE 3550308) | [`/v1/servicos/3550308.json`](https://table-json.netlify.app/v1/servicos/3550308.json) |

---

### Países

| Recurso | Endpoint |
|---------|----------|
| Países | [`/v1/paises/paises.json`](https://table-json.netlify.app/v1/paises/paises.json) |

---

### Produtos e medidas

| Recurso | Endpoint |
|---------|----------|
| Unidade de medida | [`/v1/medidas/unidade.json`](https://table-json.netlify.app/v1/medidas/unidade.json) |
| Peso | [`/v1/medidas/peso.json`](https://table-json.netlify.app/v1/medidas/peso.json) |

---

### Cores

| Recurso | Endpoint |
|---------|----------|
| Cores | [`/v1/cores/cores.json`](https://table-json.netlify.app/v1/cores/cores.json) |

---

### Monetário

| Recurso | Endpoint |
|---------|----------|
| Moedas | [`/v1/monetario/moedas.json`](https://table-json.netlify.app/v1/monetario/moedas.json) |

---

### Pessoas

Dados cadastrais de referência para formulários e sistemas de gestão.

| Recurso | Endpoint |
|---------|----------|
| Documentos | [`/v1/pessoas/documentos.json`](https://table-json.netlify.app/v1/pessoas/documentos.json) |
| Sexo | [`/v1/pessoas/sexo.json`](https://table-json.netlify.app/v1/pessoas/sexo.json) |
| Gênero | [`/v1/pessoas/genero.json`](https://table-json.netlify.app/v1/pessoas/genero.json) |
| Idiomas | [`/v1/pessoas/idiomas.json`](https://table-json.netlify.app/v1/pessoas/idiomas.json) |
| Estado civil | [`/v1/pessoas/estado-civil.json`](https://table-json.netlify.app/v1/pessoas/estado-civil.json) |
| Nível educacional | [`/v1/pessoas/nivel-educacional.json`](https://table-json.netlify.app/v1/pessoas/nivel-educacional.json) |
| Tipo de pessoa | [`/v1/pessoas/tipo-pessoa.json`](https://table-json.netlify.app/v1/pessoas/tipo-pessoa.json) |
| Dependente | [`/v1/pessoas/dependente.json`](https://table-json.netlify.app/v1/pessoas/dependente.json) |
| Categoria | [`/v1/pessoas/categoria.json`](https://table-json.netlify.app/v1/pessoas/categoria.json) |
| Instrução | [`/v1/pessoas/instrucao.json`](https://table-json.netlify.app/v1/pessoas/instrucao.json) |

---

## Estrutura do repositório

```
TableJson/
├── index.html          # Página inicial com catálogo de endpoints
├── robots.txt          # Diretivas para indexação (Google, Bing)
├── sitemap.xml         # Mapa de URLs para mecanismos de busca
├── netlify.toml        # Configuração de deploy (CORS, cache)
└── v1/
    ├── ibge/           # Municípios, UF, DDD, DDI e cidades por estado
    ├── impostos/       # CFOP, CNAE, ICMS, CSOSN, CRT
    ├── servicos/       # Simples Nacional e ISSQN municipal
    ├── paises/         # Lista de países
    ├── medidas/        # Unidades de medida e peso
    ├── cores/          # Cores
    ├── monetario/      # Moedas
    └── pessoas/        # Dados cadastrais
```

---

## Deploy

O projeto é um site estático hospedado no [Netlify](https://www.netlify.com/). Para rodar localmente:

```bash
# Com Python 3
python3 -m http.server 8080

# Ou com npx (serve)
npx serve .
```

Acesse `http://localhost:8080` e navegue pelos endpoints em `/v1/`.

Para publicar no Netlify, basta conectar o repositório GitHub — não há build step; o publish directory é a raiz do projeto.

---

## Contribuindo

Contribuições são bem-vindas! Você pode:

1. **Adicionar novos conjuntos de dados** — crie o arquivo `.json` em `v1/{categoria}/` e atualize `index.html`, `sitemap.xml` e este README
2. **Corrigir ou atualizar tabelas existentes** — especialmente dados fiscais e do IBGE
3. **Adicionar municípios em Serviços** — arquivos nomeados pelo código IBGE (ex.: `3550308.json` para São Paulo)

Abra uma issue ou pull request em [github.com/danilosoftwares/TableJson](https://github.com/danilosoftwares/TableJson).

### Topics sugeridas no GitHub

Para melhorar a descoberta do repositório, configure estas **topics** nas configurações do repo:

`json` `api` `brasil` `ibge` `municipios` `cfop` `cnae` `csosn` `icms` `simples-nacional` `issqn` `dados-abertos` `static-api` `netlify` `fiscal` `tributario`

---

## Licença

Este projeto está sob a licença MIT.
