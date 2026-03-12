# Poli-Gyn Embalagens - Infografia Geopolítica

Site responsivo com análise de impacto geopolítico do Estreito de Ormuz no mercado de PE e PP.

## Características

- ✅ Design responsivo (desktop, tablet, mobile)
- ✅ Formulário de contato funcional
- ✅ Google Analytics integrado
- ✅ Acessibilidade (WCAG)
- ✅ Performance otimizada
- ✅ SEO-friendly

## Configuração

### 1. Google Analytics

Para ativar o rastreamento de analytics:

1. Crie uma conta em [Google Analytics](https://analytics.google.com/)
2. Copie seu ID de medição (formato: G-XXXXXXXXXX)
3. Abra `index.html` e substitua `G-XXXXXXXXXX` por seu ID real em dois lugares:
   - Linha 12: `<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>`
   - Linha 15: `gtag('config', 'G-XXXXXXXXXX');`

### 2. Formulário de Contato

O formulário usa [Formspree](https://formspree.io/) para enviar emails:

1. Acesse [formspree.io](https://formspree.io/) e crie uma conta
2. Crie um novo formulário e copie o ID
3. Abra `index.html` e substitua `FORM_ID` na linha 1138:
   ```javascript
   const response = await fetch('https://formspree.io/f/FORM_ID', {
   ```
4. Substitua `FORM_ID` pelo ID do seu formulário (ex: `f/xyzabc123`)

### 3. Email de Contato

Atualize o email de contato no footer:
- Linha 1286: `<a href="mailto:contato@poligyn.com.br">contato@poligyn.com.br</a>`

### 4. Telefone de Contato

Atualize o telefone no footer:
- Linha 1287: `<a href="tel:+551140000000">(11) 4000-0000</a>`

## Deployment no GitHub Pages

### Pré-requisitos
- Conta GitHub
- Git instalado

### Passos

1. **Crie um repositório no GitHub**
   - Vá para [github.com/new](https://github.com/new)
   - Nome do repositório: `poligyn-infographic` (ou seu nome preferido)
   - Deixe público
   - Clique em "Create repository"

2. **Configure o repositório local**
   ```bash
   cd /home/ubuntu/poligyn-site
   git remote add origin https://github.com/SEU_USUARIO/poligyn-infographic.git
   git branch -M main
   ```

3. **Faça o primeiro commit**
   ```bash
   git add .
   git commit -m "Initial commit: Poli-Gyn geopolitical analysis infographic"
   git push -u origin main
   ```

4. **Ative GitHub Pages**
   - Vá para Settings do repositório
   - Navegue até "Pages"
   - Em "Source", selecione "Deploy from a branch"
   - Branch: `main`, Folder: `/ (root)`
   - Clique em "Save"

5. **Seu site estará disponível em**
   ```
   https://SEU_USUARIO.github.io/poligyn-infographic
   ```

## Apontar Domínio Customizado

Quando tiver acesso ao DNS do domínio `poligyn.com.br`:

1. **Adicione um registro CNAME** no seu provedor DNS:
   - Host: `www` (ou `@` para root)
   - Valor: `SEU_USUARIO.github.io`

2. **Em GitHub Pages Settings**:
   - Custom domain: `poligyn.com.br`
   - Ative "Enforce HTTPS"

3. **Seu site estará acessível em**:
   ```
   https://poligyn.com.br
   ```

## Estrutura de Arquivos

```
poligyn-site/
├── index.html          # Arquivo principal do site
├── README.md           # Este arquivo
└── .gitignore          # Arquivos ignorados pelo Git
```

## Customizações Possíveis

### Cores
As cores estão definidas em variáveis CSS no início do `<style>`:
```css
:root {
  --blue-primary: #342985;
  --blue-dark: #2a2070;
  --blue-light: #4a3fa3;
  /* ... */
}
```

### Tipografia
Fontes importadas do Google Fonts:
- Montserrat (títulos)
- Open Sans (corpo)

### Conteúdo
Todo o conteúdo está no HTML e pode ser editado diretamente.

## Analytics Rastreados

O site rastreia automaticamente:
- Visualizações de página
- Profundidade de scroll (50%)
- Envios de formulário
- Erros de formulário

## Suporte

Para dúvidas sobre configuração, consulte:
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Formspree Documentation](https://formspree.io/docs)
- [Google Analytics Help](https://support.google.com/analytics)

---

**Versão**: 1.0  
**Última atualização**: 2026  
**Autor**: Manus
