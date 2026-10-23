# ARIA OMEGA — testemunhas externas

Cópia pública dos digests das âncoras RFC 3161 das cadeias de governança do ARIA OMEGA.

Cada linha de `testemunhas.txt` tem o formato:

```
<digest_sha256> ancora=<N> gen=<genTime UTC> repo=<owner/repo>
```

O arquivo contém só hashes, números e horários: nenhum registro, código ou dado pessoal.

## Regras

- O arquivo só cresce. Uma linha publicada nunca é trocada nem removida.
- Os ciclos do projeto acrescentam uma linha por âncora nova.

## Para que serve

Se o repositório do projeto for truncado ou reescrito, as âncoras dele deixam de bater com estas linhas. Para conferir, num clone do projeto:

```bash
python src/aria_omega/ancorar_cadeias.py --verificar --testemunhas testemunhas.txt --exigir-todas-testemunhas
```

Este repositório também é controlado pelo responsável técnico do projeto. Por isso, a testemunha fica mais forte com cópias guardadas por terceiros: clones, forks ou arquivamento.
