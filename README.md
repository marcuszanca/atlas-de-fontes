# Atlas de Fontes

Diretório pesquisável de fontes **legais e abertas** de mangás, livros, acervos e artigos.
Filtre por letra, categoria, tema, tipo de arquivo, idioma e acesso, e abra a busca direto em cada fonte.

- Arquivo único, sem dependências e sem build
- Instalável no celular e no computador (PWA) e funciona offline
- Tema preto e branco, claro ou escuro conforme o aparelho


## como testar localmente

```bash
python3 -m http.server 8000
```
Abra http://localhost:8000. O `index.html` também funciona com dois cliques, só sem o modo offline.

## Adicionar fontes

No `index.html`, procure `const D=[`. Cada linha segue este formato:

```
["Nome","Categoria",["Temas"],["Arquivos"],"Idioma","Acesso","https://site","https://site/busca?q={q}","Descrição"]
```

Use `null` no lugar do endereço de busca se a fonte não tiver busca por URL.
Categorias: Mangá, Livros, Artigos, Acervos.
Ao alterar arquivos, mude `CACHE = "atlas-v1"` em `sw.js` (por exemplo para `atlas-v2`) para os usuários receberem a atualização.

## Aviso

Só são listadas plataformas oficiais, de acesso aberto ou de domínio público. Confira a licença de cada obra.
O MangaDex reúne conteúdo oficial e de comunidade, e o Periódicos CAPES exige login institucional.

## Licença

MIT
