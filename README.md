# Indice de plugins agenticos de la organizacion

Este repositorio contiene **solo un archivo relevante**: `.claude-plugin/marketplace.json`,
el indice de plugins publicados del banco.

## Como lo usa un desarrollador

```bash
copilot plugin marketplace add Banca-Copilot-demo/marketplace   # una sola vez
copilot plugin install migracion-cnf@agentico                      # cada vez que quiera algo
```

## Reglas

- **El indice se GENERA, no se edita.** Lo escribe `regenerar-indice.yml` cuando un
  repositorio de dominio publica un release.
- **Sin atestacion no hay entrada.** El generador exige que exista atestacion antes de
  incluir un plugin. Es lo que cierra el hueco de que `publicar.yml` viva en el repo del
  dominio y sea editable.
- **Cada entrada lleva `ref` y `sha`.** El `ref` para que un humano lo lea; el `sha` porque
  es inmune a que una etiqueta se mueva, y es lo que se compara contra la atestacion.
