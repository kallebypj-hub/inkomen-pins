# inkomen-pins

Imagens públicas dos pins da loja [InkOmenPress](https://www.etsy.com/shop/InkOmenPress).

Este repositório existe por um motivo técnico só: a importação em massa do
Pinterest (*Settings → Bulk create Pins*) exige que cada imagem esteja num
**endereço público** — ela baixa o arquivo pela URL. Imagem no computador não
serve.

O GitHub Pages serve os arquivos deste repositório em:

```
https://kallebypj-hub.github.io/inkomen-pins/pins/semana_N/arquivo.jpg
```

E é essa URL que vai na coluna `Media URL` do CSV de importação.

## O que tem aqui

```
pins/semana_1/ … semana_5/    175 imagens, 5 por dia, 22/09 a 26/10/2026
```

Nada mais. Sem código, sem dado pessoal, sem nada da loja além das próprias
imagens de divulgação — que são feitas para serem vistas.

## Como foi gerado

    python motor/pins_agenda.py --semana 35 --saida agenda-envio \
        --inicio 2026-09-22 \
        --url https://kallebypj-hub.github.io/inkomen-pins/pins

no repositório do motor (`etsy-motor`). O mesmo comando escreve o
`importar.csv` que aponta para estas imagens.
