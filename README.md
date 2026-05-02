<div align="center">

# Olá, eu sou Rilder Araujo 👋

**Desenvolvedor C# · .NET · Next.js · IA**

> Construo sistemas que resolvem problemas reais — do controle financeiro ao SaaS multi-tenant completo.

[![Portfolio](https://img.shields.io/badge/🌐_Portfólio-rilder--araujo.netlify.app-00f5c4?style=for-the-badge)](https://rilder-araujo.netlify.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Rilder_Araujo-0077B5?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/rilder-araujo-00078b365)
[![Email](https://img.shields.io/badge/Email-rilder2025.1@gmail.com-D14836?style=for-the-badge&logo=gmail)](mailto:rilder2025.1@gmail.com)

</div>

---

## 🚀 Sobre mim

- 💻 Desenvolvedor focado em **C#, .NET, Next.js e Inteligência Artificial**
- 🎓 Cursando **Análise e Desenvolvimento de Sistemas** 
- 🏗️ Criador do **NexoSaaS** — plataforma SaaS multi-tenant para pequenas e médias empresas
- 🤖 Uso **IA no desenvolvimento** para entregar mais rápido e com mais qualidade
- 🎯 Buscando minha primeira vaga como desenvolvedor.
- 📍 Natal, RN — Brasil

---

## 🏆 Projeto Principal — NexoSaaS

> Plataforma SaaS multi-tenant com 9 módulos, desenvolvida do zero com arquitetura profissional.

### Módulos desenvolvidos

| Módulo | Descrição |
|--------|-----------|
| 🛒 **Vendas** | PDV completo com controle de carrinho e pagamentos |
| 📦 **Estoque** | Controle de produtos, categorias e movimentações |
| 💰 **Caixa** | Abertura, fechamento e relatórios financeiros |
| 👥 **Clientes** | Cadastro e histórico de compras |
| 🍽️ **Restaurante** | Controle de mesas e pedidos |
| 🚚 **Entregas** | Gestão de deliveries |
| 🏭 **Fornecedores** | Cadastro e gestão de fornecedores |
| 📊 **Financeiro** | Contas a pagar e receber |
| 👨‍💼 **Funcionários** | Cadastro e controle de equipe |

### Arquitetura

```typescript
// Isolamento multi-tenant com Supabase RLS
// Cada tenant só acessa seus próprios dados

create or replace function get_tenant_id()
returns uuid as $$
  select tenant_id 
  from tenants 
  where user_id = auth.uid()
$$ language sql security definer;

-- RLS aplicado em todas as tabelas
create policy "tenant_isolation" on products
  using (tenant_id = get_tenant_id());
```

```typescript
// Estrutura de planos — 3 verticais de negócio
const plans = {
  basic:      { name: 'Básico',     price: 49,  target: 'Lojas de roupas' },
  premium:    { name: 'Premium',    price: 99,  target: 'Bares e restaurantes' },
  enterprise: { name: 'Enterprise', price: 199, target: 'Distribuidoras' },
}
```

> 🔒 **Repositório privado** — sistema em produção ativo

---

## 📂 Repositórios Públicos

### 💰 [Sistema Financeiro](https://github.com/rilderaraujo/Sistema-Financeiro)
Controle financeiro em C# com gerenciamento de receitas, despesas e relatórios.

```csharp
// Exemplo de lançamento financeiro
public void AdicionarLancamento(Lancamento lancamento)
{
    if (lancamento.Tipo == TipoLancamento.Receita)
        SaldoAtual += lancamento.Valor;
    else
        SaldoAtual -= lancamento.Valor;
        
    _repositorio.Salvar(lancamento);
}
```

![C#](https://img.shields.io/badge/C%23-239120?style=flat&logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat&logo=dotnet&logoColor=white)

---

### 🌐 [Portfólio Pessoal](https://rilder-araujo.netlify.app)
Site de portfólio desenvolvido com HTML, CSS e JavaScript puro. Design dark moderno.

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

---

## 🛠️ Tecnologias

### Desenvolvimento
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

### Banco de Dados & Backend
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)

### Ferramentas
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)

### Inteligência Artificial & Produtividade
![Claude](https://img.shields.io/badge/Claude_AI-CC785C?style=for-the-badge&logo=anthropic&logoColor=white)
![ChatGPT](https://img.shields.io/badge/ChatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white)
![GitHub Copilot](https://img.shields.io/badge/GitHub_Copilot-000000?style=for-the-badge&logo=github&logoColor=white)
![Cursor](https://img.shields.io/badge/Cursor_AI-000000?style=for-the-badge&logo=cursor&logoColor=white)
![Obsidian](https://img.shields.io/badge/Obsidian-7C3AED?style=for-the-badge&logo=obsidian&logoColor=white)

---

## 📊 Estatísticas

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=rilderaraujo&show_icons=true&theme=tokyonight&hide_border=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=rilderaraujo&layout=compact&theme=tokyonight&hide_border=true)

</div>

---

## 📬 Contato

<div align="center">

Estou disponível para oportunidades como desenvolvedor júnior!

[![Portfolio](https://img.shields.io/badge/🌐_Portfólio-Acesse_aqui-00f5c4?style=for-the-badge)](https://rilder-araujo.netlify.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Conectar-0077B5?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/rilder-araujo-00078b365)
[![Email](https://img.shields.io/badge/Email-Enviar_mensagem-D14836?style=for-the-badge&logo=gmail)](mailto:rilder2025.1@gmail.com)

</div>

---

<div align="center">
  <sub>💡 Transformando ideias em código · Natal, RN — Brasil · 2026</sub>
</div>
