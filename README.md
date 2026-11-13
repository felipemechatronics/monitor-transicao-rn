# Monitor da Transição RN

Painel dos formulários do **Relatório Consolidado Setorial** (art. 4º da IN) preenchidos pelos órgãos do Governo do RN na pasta "DADOS - IN - ART. 4º" do Google Drive.

Na abertura aparece a visão geral das 39 pastas com formulário preenchido, com filtro por eixo. Há também uma aba para cada um dos 6 eixos (links `index.html#eixo-1` a `#eixo-6`), com totais, comparativo das pastas, mapa e as unidades do eixo que ainda não enviaram o formulário. A visão geral lista também as unidades que ainda não subiram formulário, com link para a pasta de cada uma no Drive. O filtro por município (seletor ou clique no mapa) mostra as obras e os bens localizados no município e combina com o eixo. Escolha uma pasta no seletor (ou clique num cartão) para ver identificação, indicadores, controle dos incisos I a XXVI, contratos, obras com mapa por município, finanças, pessoal, patrimônio e as demais abas. Cada pasta tem link próprio, por exemplo `index.html#SESED`.

## Como abrir

A página lê os arquivos em `data/`, então precisa ser servida por HTTP (abrir o `index.html` direto do disco não funciona):

```bash
python3 -m http.server 8000
# depois abra http://localhost:8000
```

Ou publique pelo GitHub Pages (Settings → Pages → branch `main`, pasta `/`).

## Dados

- Cópia lida em **13/11/2026** (leituras anteriores em 10 e 11/11/2026). Alterações posteriores nas planilhas não aparecem até os arquivos de `data/` serem gerados de novo.
- Quando uma pasta tinha mais de uma planilha, cada aba vem da versão com mais linhas preenchidas.
- Situações escritas livremente foram agrupadas (ex.: "Disponibilizado" e "Concluída" contam como Atendido); o texto original está nos arquivos.
- Obras e bens são localizados pela sede do município informado. Malha municipal: IBGE.
- A SIN não tem pasta no Drive e não aparece entre as pastas; na aba do Eixo 4 ela consta entre as unidades sem formulário.
- Os eixos vêm da planilha "UGs por eixo" do acompanhamento dos processos SEI. CONTROL, JUCERN e SEPLAN estão em dois eixos e aparecem nas duas abas.
- Os arquivos trazem nomes de responsáveis e de contratados: mantenha o repositório privado a menos que a divulgação esteja autorizada.
