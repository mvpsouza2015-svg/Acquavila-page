# Acquavilla Distribuidora - Catálogo e Pedidos Online

Loja virtual moderna e responsiva para catálogo e envio de pedidos via WhatsApp da **Acquavilla Produtos de Limpeza e Descartáveis LTDA**.

## 🚀 Como Executar Localmente

### Opção 1: Abrir diretamente no Navegador
Basta dar dois cliques no arquivo `index.html` ou arrastá-lo para qualquer navegador moderno (Chrome, Edge, Firefox, Safari).

### Opção 2: Servidor Local Simples (Node.js)
```bash
# Com npx (não precisa instalar nada globalmente):
npx serve .

# Ou com live-server:
npx live-server
```

### Opção 3: Servidor Local com Python
```bash
python3 -m http.server 3000
# Acesse: http://localhost:3000
```

---

## 🛠️ Onde Editar Marca, Contatos, Categorias e Produtos

Tudo está centralizado no início da tag `<script>` dentro de `index.html`:

1. **Informações da Empresa (`STORE_CONFIG`)**:
   - `name`: Nome fantasia da empresa.
   - `corporateName`: Razão social.
   - `cnpj`: CNPJ cadastrado.
   - `whatsappNumber`: Número com DDD (apenas dígitos) para o link da API do WhatsApp.
   - `whatsappDisplay`: Formatação exibida visualmente nos textos e rodapé.
   - `phone`: Telefone fixo da empresa.
   - `address`, `neighborhood`, `city`, `cep`: Endereço completo do Centro de Distribuição.
   - `minOrderCents`: Valor mínimo do pedido em centavos (ex: `15000` = R$ 150,00).

2. **Categorias (`CATEGORIES`)**:
   - Adicione, remova ou renomeie categorias no array `CATEGORIES`.

3. **Catálogo de Produtos (`PRODUCTS`)**:
   - Cada produto possui `id`, `sku`, `name`, `category`, `description`, `unit`, `priceCents`, `originalPriceCents`, `inStock`, `minQty`.

---

## 🌐 Instruções de Publicação Gratuita (Deploy)

### Vercel
1. Instale a CLI: `npm i -g vercel` (ou conecte seu repositório no [vercel.com](https://vercel.com)).
2. Na pasta do projeto, execute: `vercel`
3. Pronto! O site estará online com HTTPS gratuito.

### Netlify
1. Acesse [app.netlify.com/drop](https://app.netlify.com/drop).
2. Arraste a pasta deste projeto diretamente para o navegador.
3. Seu catálogo estará no ar em segundos.

### GitHub Pages
1. Crie um repositório no GitHub.
2. Envie o arquivo `index.html`.
3. Vá em **Settings > Pages** e ative a publicação na branch `main`.
