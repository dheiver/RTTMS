📊 Simulador de Riser Avançado 🚀

**Descrição:**

Este repositório contém um simulador de riser avançado desenvolvido em Python. O simulador é projetado para modelar e analisar a tensão verdadeira em risers submarinos, levando em consideração gradientes de temperatura, gradientes de pressão, erros de medição, compensação de temperatura e pressão, forças aplicadas e ruído.

O simulador é uma ferramenta poderosa para engenheiros e pesquisadores que trabalham em projetos relacionados à exploração de petróleo e gás em ambientes submarinos. Ele fornece informações valiosas para avaliar a integridade estrutural dos risers e tomar decisões informadas sobre o projeto e operação.

**Funcionalidades Principais:**

- Definição de parâmetros personalizados, como número de segmentos, tensão medida, coeficiente de erro, desvio de ruído e muito mais.
- Simulação de gradientes de temperatura e pressão para cada segmento do riser.
- Ajuste de uma função não linear aos gradientes de temperatura.
- Cálculo da tensão verdadeira considerando vários fatores, incluindo erros, compensação de temperatura e pressão e forças aplicadas.
- Visualização dos resultados em gráficos interativos.
- Geração de relatórios detalhados com estatísticas de tensão verdadeira.

**Instruções de Uso:**

1. Clone o repositório para sua máquina local.
2. Configure os parâmetros iniciais no código-fonte, se necessário.
3. Execute o simulador para gerar simulações de risers avançados.
4. Visualize os resultados em gráficos interativos.
5. Gere relatórios detalhados para análise.

**Exemplo de Uso:**

```python
# Defina os parâmetros iniciais
parametros = Parametros(
    num_segmentos=10, 
    tensao_medida=150.0, 
    coef_erro=0.0, 
    desvio_ruido=1.0, 
    forca=500.0, 
    kt=0.0002, 
    kp=0.00005, 
    kf=0.001, 
    dia_interno=0.35, 
    dia_externo=0.45
)

# Execute o simulador para um segmento específico
segmento_selecionado = 0
tensao_cabeca = criar_riser_avancado(parametros, gradientes_temp, gradientes_pressao, segmento_selecionado)

# Visualize os resultados
criar_visualizacoes_tempo(tensao_cabeca, gradientes_temp, gradientes_pressao, dias, segmento_selecionado)

# Gere um relatório completo
gerar_relatorio_completo(tensao_cabeca, segmento_selecionado)
