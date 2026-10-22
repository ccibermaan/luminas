# Lumina Odontologia — Site Institucional

Site institucional para clínica de odontologia em São Paulo, SP.
Design elegante em tons de azul claro e ciano, interatividade inspirada em rolagem cinematográfica, vídeo de tratamento odontológico em loop e logo TAUFF com fundo transparente no rodapé.

## Estrutura do site (esqueleto)

1. **Header + Hero** — nome da clínica, descrição, chamativo e contato (com estatísticas e indicador de rolagem)
2. **O Estabelecimento** — textos institucionais, pilares e chips de contato
3. **Procedimentos** — leque interativo com 7 cards e setas de navegação
   🎬 **Vídeo em loop** — banda de vídeo com tratamento odontológico (entre as partes 3 e 4)
4. **Depoimentos** — 3 clientes + card de avaliação 5,0
5. **Footer** — contato | texto chamativo | logo TAUFF (fundo transparente)

## Tecnologias

- [Next.js 16](https://nextjs.org/) (App Router) + TypeScript
- [Tailwind CSS 4](https://tailwindcss.com/) + shadcn/ui
- [Framer Motion](https://www.framer.com/motion/) (scroll-reveal, leque com física de mola, parallax)
- Fontes: **Playfair Display** (display/itálicos) + **Inter** (corpo)

## Como executar

Pré-requisitos: Node.js 18+ (ou Bun).

```bash
# 1. Instalar dependências
npm install        # ou: bun install

# 2. Rodar em modo de desenvolvimento
npm run dev        # ou: bun run dev

# 3. Abrir no navegador
# http://localhost:3000
```

Build de produção:

```bash
npm run build
npm start
```

## Personalização rápida

| O que               | Onde                                                              |
| ------------------- | ----------------------------------------------------------------- |
| Textos e seções     | `src/components/site/*.tsx` (Hero, About, ServicesFan, Testimonials, Footer) |
| Cores do tema       | `src/app/globals.css` (variáveis CSS `--primary`, `--accent`...)   |
| Logo da clínica     | `public/assets/logo-lumina.png`                                    |
| Logo TAUFF (footer) | `public/assets/logo-tauff-white.png` (variante clara em `logo-tauff.png`) |
| Vídeo em loop       | `public/assets/dental-procedure.mp4`                               |
| Fotos               | `public/assets/photos/`                                            |

## Conteúdo do pacote

```
├── src/                  # Código-fonte (componentes, estilos, layout)
├── public/assets/        # Logos, vídeo e fotos
├── prisma/               # Schema do ORM (não utilizado pelo site estático)
├── package.json          # Dependências e scripts
└── configs               # tsconfig, next.config, tailwind, postcss, eslint
```

> Observação: o banco de dados (Prisma/SQLite) não é necessário para exibir o site; ele faz parte do template base do projeto.
