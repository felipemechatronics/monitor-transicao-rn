# Monitor da Transição RN

Painel dos formulários do **Relatório Consolidado Setorial** (art. 4º da IN) preenchidos pelos órgãos do Governo do RN na pasta "DADOS - IN - ART. 4º" do Google Drive.

Na abertura aparece a visão geral das 23 pastas com formulário preenchido. Escolha uma pasta no seletor (ou clique num cartão) para ver identificação, indicadores, controle dos incisos I a XXVI, contratos, obras com mapa por município, finanças, pessoal, patrimônio e as demais abas. Cada pasta tem link próprio, por exemplo `index.html#SESED`.

## Como abrir

A página lê os arquivos em `data/`, então precisa ser servida por HTTP (abrir o `index.html` direto do disco não funciona):

```bash
python3 -m http.server 8000
# depois abra http://localhost:8000
```

Ou publique pelo GitHub Pages (Settings → Pages → branch `main`, pasta `/`).

## Dados

- Cópia lida em **10/11/2026**. Alterações posteriores nas planilhas não aparecem até os arquivos de `data/` serem gerados de novo.
- Quando uma pasta tinha mais de uma planilha, cada aba vem da versão com mais linhas preenchidas.
- Situações escritas livremente foram agrupadas (ex.: "Disponibilizado" e "Concluída" contam como Atendido); o texto original está nos arquivos.
- Obras e bens são localizados pela sede do município informado. Malha municipal: IBGE.
- A SIN não tem pasta no Drive e não aparece.
- Os arquivos trazem nomes de responsáveis e de contratados: mantenha o repositório privado a menos que a divulgação esteja autorizada.
