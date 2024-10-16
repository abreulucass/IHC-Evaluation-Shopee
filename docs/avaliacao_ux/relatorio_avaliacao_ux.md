# Relatório de Avaliação de UX da Shopee com Lighthouse

## Introdução
Este relatório tem como objetivo analisar os resultados gerados pela ferramenta Lighthouse (via Chrome DevTools) para o site da Shopee, com foco nas métricas de desempenho e acessibilidade. Além da interpretação dessas métricas, uma discussão sobre os problemas de acessibilidade identificados também será abordada. O intuito é identificar oportunidades de melhoria que impactam diretamente a experiência do usuário.

## Interpretação das Métricas

![img]()

### Avaliação das Core Web Vitals
Core Web Vitals é um conjunto de métricas essenciais para medir a qualidade da experiência de uso, como o desempenho de carregamento, interatividade e estabilidade visual. No caso do teste realizado, o site da Shopee foi reprovado nas Core Web Vitals, e os resultados obtidos foram os seguintes:

### Maior Tinta de Conteúdo (LCP): 11,7s
O INP é uma métrica experimental que quantifica a responsividade de uma página ao longo de sua interação. Um tempo ideal de INP seria inferior a 200ms, enquanto o valor de 648ms indica que a responsividade está aquém do esperado, impactando negativamente a usabilidade.

### Interação com a Próxima Pintura (INP): 648ms
O "Índice de Velocidade" mede a rapidez com que o conteúdo visual da página é carregado. Com um valor de 9,7 segundos, a página leva um tempo considerável para preencher visualmente o conteúdo. Este índice reflete uma experiência de carregamento lenta, o que pode resultar em insatisfação dos usuários e possível abandono da página.

### Mudança Cumulativa de Layout (CLS): 0,14
Esta métrica avalia a estabilidade visual de uma página, medindo quantos elementos visuais se movem inesperadamente durante o carregamento. O CLS ideal deve ser inferior a 0,1, e com o valor de 0,14, embora não esteja tão longe do recomendado, ainda há espaço para melhorias na estabilidade visual.

## Outras metricas importantes
Além das Core Web Vitals, outras métricas foram analisadas no teste com Lighthouse:

![img]()

### Primeira Pintura de Conteúdo (FCP): 2,3s
O FCP mede o tempo em que o primeiro conteúdo (texto, imagem, ou SVG) é renderizado no navegador. Embora o valor obtido (2,3s) seja aceitável, está ligeiramente acima do valor recomendado (1,8s ou menos). Esse tempo pode ser uma das causas do atraso na percepção inicial do usuário.

### Tempo até o Primeiro Byte (TTFB): 1,6s
O TTFB mede o tempo que o servidor leva para responder ao navegador com o primeiro byte de dados. Um TTFB inferior a 0,8s é o ideal. Com 1,6 segundos, o site apresenta uma resposta lenta, o que pode prejudicar a experiência inicial de navegação.

## Acessibilidade
A pontuação de acessibilidade da Shopee foi de 70, indicando que há várias áreas a melhorar. Embora o valor não seja baixo, ele não atinge o ideal para garantir uma navegação acessível a todos os usuários.

### Principais Problemas de Acessibilidade Identificados:
- `[user-scalable="no"] no elemento <meta name="viewport">`: O uso de uma metatag viewport que impede a escalabilidade da página afeta negativamente usuários com baixa visão. Esses usuários muitas vezes dependem da função de zoom do navegador para aumentar o tamanho do conteúdo da página e torná-lo legível. Ao desativar essa funcionalidade, o site cria barreiras de acesso para pessoas com deficiência visual, comprometendo a experiência de uso.
- **Elementos falhos no uso da metatag `<meta>`**: O relatório sugere que a configuração da metatag `<meta name="viewport">` não segue as melhores práticas, e isso deve ser corrigido para melhorar a acessibilidade. Essa falha, se corrigida, pode evitar problemas na visualização em diferentes dispositivos e tamanhos de tela.

### Discussão dos Impactos:
Esses problemas afetam diretamente a experiência de usuários com deficiência visual, que não conseguem ampliar o conteúdo da página para melhor leitura. A falta de escalabilidade pode tornar o site praticamente inutilizável para essas pessoas, violando as diretrizes de acessibilidade. Corrigir essas questões ajudaria a Shopee a atender a uma maior diversidade de usuários e melhorar sua pontuação de acessibilidade.

## Outras Métricas
Além das métricas de desempenho e acessibilidade, outros aspectos do site foram analisados pela ferramenta Lighthouse:
- **Desempenho: 33** O desempenho geral do site foi considerado baixo, principalmente devido aos tempos altos de carregamento e bloqueio da página. Este é um aspecto que deve ser priorizado para proporcionar uma experiência de usuário mais eficiente e rápida.
- **Práticas Recomendadas: 100** A pontuação perfeita em práticas recomendadas indica que o site segue as diretrizes e padrões web modernos, o que é positivo para manter a compatibilidade com diferentes navegadores e dispositivos.
- **SEO: 91** O site também obteve uma excelente pontuação em SEO, sugerindo que ele é bem otimizado para mecanismos de busca, o que ajuda a garantir uma boa visibilidade nos resultados de pesquisa.

## Conclusão
A análise do site da Shopee utilizando o Lighthouse revelou áreas importantes para melhoria, especialmente relacionadas ao tempo de carregamento, bloqueios na interatividade e acessibilidade. Os maiores pontos críticos são o Tempo Total de Bloqueio e a Maior Pintura de Conteúdo, que afetam significativamente a experiência do usuário. Quanto à acessibilidade, corrigir o problema com a metatag viewport pode melhorar a experiência para usuários com deficiências visuais. Essas melhorias seriam essenciais para aumentar a satisfação do usuário e garantir uma navegação mais eficiente e inclusiva.

