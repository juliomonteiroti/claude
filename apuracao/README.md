# Apuração Presidente 2026 — 1º turno

Página estática (um único `index.html`, sem build nem servidor) que mostra a apuração
do cargo de Presidente consumindo diretamente os arquivos públicos de divulgação do TSE.

- **Dados:** `https://resultados.tse.jus.br/oficial/ele2026/6257/dados/br/br-c0001-e006257-u.json`
  (eleição `6257` = Eleição Ordinária Federal 2026, 1º turno; cargo `0001` = Presidente).
  Os códigos vêm de `https://resultados.tse.jus.br/oficial/comum/config/ele-c.json`.
- **Fotos:** `.../ele2026/6257/fotos/br/<sqcand>.jpeg`
- **Atualização:** a cada 30 s (constante `INTERVALO_S`) e ao voltar para a aba.
  Respostas mais antigas que a última exibida são ignoradas.

## Como rodar

Abra `index.html` no navegador, ou publique a pasta em qualquer hospedagem estática
(GitHub Pages, Netlify etc.). O servidor do TSE envia `Access-Control-Allow-Origin`,
então o navegador busca os dados direto.

Para o 2º turno, troque `ELEICAO` para `6258` no script.
