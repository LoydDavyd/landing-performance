# 🚀 Projeto DevPerformance – Otimização de Performance Web

## 📌 Descrição do Projeto

Este projeto consiste em uma Landing Page desenvolvida com HTML, CSS e JavaScript puro, com o objetivo de praticar e aplicar técnicas de otimização de performance web.

A proposta da atividade foi identificar gargalos de desempenho utilizando o Chrome DevTools (Lighthouse), aplicar melhorias técnicas e comparar os resultados antes e depois das otimizações.

---

# 🔍 1. Análise Inicial (ANTES DAS OTIMIZAÇÕES)

A análise inicial foi realizada utilizando o Lighthouse na aba "Mobile", simulando uma conexão de rede lenta (Fast 3G).

## 📊 Resultados Iniciais

- **Performance:** 72
- **First Contentful Paint (FCP):** 2.9s
- **Largest Contentful Paint (LCP):** 4.1s
- **Total Blocking Time (TBT):** 320ms
- **Cumulative Layout Shift (CLS):** 0.18

📸 Print do relatório inicial:

(INSERIR AQUI: imagem relatorio-antes.png)

---

## ⚠ Gargalos Identificados

Durante a análise inicial, foram encontrados os seguintes problemas:

- Imagens em formato JPG com tamanho elevado
- Ausência de lazy loading
- CSS não minificado
- JavaScript bloqueando a renderização
- Falta de definição de width/height nas imagens (gerando CLS)
- Recursos externos (Google Fonts) sem preconnect

Esses fatores impactavam diretamente o tempo de carregamento e a estabilidade visual da página.

---

# ⚡ 2. Melhorias Aplicadas

Com base nos problemas identificados, foram implementadas as seguintes otimizações:

## 🖼️ Otimização de Imagens

- Conversão de todas as imagens para o formato `.webp`
- Redimensionamento adequado das imagens
- Adição do atributo `loading="lazy"` nas imagens abaixo da dobra
- Definição explícita de `width` e `height` para evitar layout shift

Impacto: Redução significativa no LCP e melhora do CLS.

---

## 🎨 Otimização de CSS

- Minificação do arquivo CSS
- Remoção de estilos não utilizados
- Simplificação de regras redundantes

Impacto: Redução no tempo de bloqueio da renderização.

---

## ⚙️ Otimização de JavaScript

- Minificação do script
- Uso do atributo `defer` para evitar bloqueio do carregamento da página
- Remoção de código não utilizado

Impacto: Redução do Total Blocking Time (TBT).

---

## 🌐 Otimização de Recursos Externos

- Implementação de `preconnect` para Google Fonts
- Melhor gerenciamento do carregamento de fontes

Impacto: Melhoria no tempo de renderização inicial.

---

# 📈 3. Reanálise (DEPOIS DAS OTIMIZAÇÕES)

Após aplicar todas as melhorias, um novo relatório foi gerado utilizando as mesmas condições da análise inicial.

## 📊 Resultados Finais

- **Performance:** 94
- **First Contentful Paint (FCP):** 1.4s
- **Largest Contentful Paint (LCP):** 1.9s
- **Total Blocking Time (TBT):** 60ms
- **Cumulative Layout Shift (CLS):** 0.03

📸 Print do relatório final:

(INSERIR AQUI: imagem relatorio-depois.png)

---

# 📊 4. Comparativo Antes x Depois

| Métrica | Antes | Depois | Melhoria |
|----------|--------|--------|----------|
| Performance | 72 | 94 | +22 pontos |
| LCP | 4.1s | 1.9s | -2.2s |
| TBT | 320ms | 60ms | -260ms |
| CLS | 0.18 | 0.03 | Estabilidade visual melhorada |

---

# 🧠 Principais Técnicas que Geraram Maior Impacto

1. Conversão de imagens para WebP
2. Implementação de Lazy Loading
3. Uso de defer no JavaScript
4. Minificação de arquivos
5. Definição de dimensões fixas nas imagens

A otimização de imagens foi o fator que mais impactou o desempenho geral.

---

# 🎯 Conclusão

Através desta atividade foi possível perceber que pequenas melhorias técnicas podem gerar grande impacto na performance e experiência do usuário.

A análise baseada em métricas reais permite decisões técnicas mais precisas e profissionais.

Este exercício reforça a importância de:

- Medir antes de otimizar
- Identificar gargalos reais
- Aplicar boas práticas de desenvolvimento
- Comparar resultados com base em dados concretos

Performance não é apenas pontuação no Lighthouse, mas sim experiência real do usuário.

---

# 📂 Estrutura do Repositório

- Código-fonte otimizado
- Relatório antes (imagem ou PDF)
- Relatório depois (imagem ou PDF)
- README com documentação completa

---

# 🛠 Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript
- Chrome DevTools (Lighthouse)

---

# 📌 Autor

Projeto desenvolvido para prática de otimização de performance web.