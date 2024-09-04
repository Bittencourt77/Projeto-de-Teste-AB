**Projeto de Teste A/B**  

Descrição
Este projeto analisa um teste A/B realizado para avaliar a eficácia de duas estratégias de marketing em um aplicativo. O objetivo é determinar se há uma diferença significativa na conversão de usuários e na receita gerada entre os dois grupos de teste: Grupo A e Grupo B.

- Dados
Os dados foram coletados em diferentes arquivos CSV:

final_ab_participants_upd_us.csv - Contém informações sobre os participantes do teste.
ab_project_marketing_events_us.csv - Registra eventos de marketing.
final_ab_new_users_upd_us.csv - Dados sobre novos usuários.
final_ab_events_upd_us.csv - Registra eventos dos novos usuários.
- Análise
1. Análise da Proporção de Usuários Comuns
Proporção de Usuários Comuns:

Grupo A: 18,10%
Grupo B: 6,04%
Observamos que a proporção de usuários comuns é significativamente maior no Grupo A em comparação ao Grupo B. Isso pode indicar que os grupos não são totalmente independentes, o que pode influenciar os resultados do teste.

Estatísticas de Engajamento e Conversão:

Usuários Comuns:

Média de eventos: 6,44
Taxa de conversão: 31,34%
Usuários Exclusivos:

Média de eventos: 6,53
Taxa de conversão: 30,49%
A análise mostra que a taxa de conversão e o engajamento dos usuários comuns e exclusivos são bastante similares, sugerindo que a contaminação entre os grupos pode não afetar significativamente as métricas de desempenho.

2. Análise da Receita
Receita Média:

Grupo A: $24,03
Grupo B: $22,39
Usuários Comuns: $21,02
Usuários Exclusivos: $19,18
A receita média dos usuários no Grupo A é maior do que no Grupo B. Além disso, usuários comuns geram mais receita em média do que usuários exclusivos.

Teste de Normalidade e Teste T:

O teste de normalidade indicou que a receita dos usuários não segue uma distribuição normal.
O teste t para comparar a receita entre os grupos A e B mostrou um p-valor de 0,5230, o que indica que a diferença observada na receita entre os grupos não é estatisticamente significativa.

- Bibliotecas Utilizadas
   
**pandas:** *Manipulação e análise de dados.  
Funções principais: pd.read_csv(), DataFrame.describe(), DataFrame.isnull()*

**numpy:** *Operações numéricas e manipulação de arrays.  
Funções principais: np.nan, np.corrcoef()*

**matplotlib:** *Visualização de dados em gráficos e plots.  
Funções principais: plt.hist(), plt.plot(), plt.show()*

**seaborn:** *Visualização estatística baseada em matplotlib.  
Funções principais: sns.heatmap(), sns.histplot(), sns.pairplot()*

**scipy:** *Para realizar testes estatísticos.  
Funções principais: scipy.stats.ttest_ind(), scipy.stats.chi2_contingency()*

**statsmodels:** *Para modelagem estatística e testes A/B.  
Funções principais: sm.Logit(), sm.OLS(), sm.stats.proportions_ztest()*

- Conclusões
  
*A análise revelou diferenças na proporção de usuários comuns entre os grupos e variações na receita média. No entanto, a falta de significância estatística na diferença de receita sugere que, embora existam variações, elas podem não ser suficientemente grandes para impactar a decisão de forma conclusiva.*
