[README.md](https://github.com/user-attachments/files/34399079/README.md)[Uploading README.md…](# B1 Architecture Lab — Gamificação para Educação Continuada

Registro arquitetural vivo: **[`docs/arquitetura/README.md`](docs/arquitetura/README.md)** (6 decisões, ADR-001…006, matriz cumulativa de ASRs, C4, síntese para a AF).

| Pasta | Conteúdo |
|---|---|
| `core/` | Core Java/Spring Boot (Monólito Modular) + `ranking` com ports & adapters (D2) + `recomendacao` com fallback de IA (D3) + Micrometer (D6) |
| `evidencias/d1…d6` | Microsoluções, resultados e logs de cada desafio |
| `ci/`, `Jenkinsfile` | Pipelines por componente e `ci/gates.sh` |

## Reexecutar as evidências (só JDK 17+ e Python 3, sem rede)
```bash
ci/gates.sh all                                  # D1–D6
evidencias/d2-organizacao-interna-core/executar-lab.sh
```
## Primeiro passo ao clonar
`cd core && mvn -B verify` — o código Spring novo (D2/D3/D6) **não foi compilado** no ambiente de elaboração (sem Maven Central). Veja a tabela "Verificação" no README arquitetural.
)
