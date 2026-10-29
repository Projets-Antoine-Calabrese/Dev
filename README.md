# Dev — méthode et qualité de code

Compétences et sous-agents que Claude utilise pour coder les applications des projets (Finances, Sport-Santé…).
Sélection tirée de dépôts publics ; provenance exacte et commits dans `SOURCES.md`.

| Dossier | Contenu |
|---|---|
| `.claude/skills/` | 33 compétences |
| `.claude/agents/` | 15 sous-agents spécialisés |
| `.claude/commands/` | 2 commandes : `/feature-dev` (développement guidé d'une fonctionnalité), `/revise-claude-md` |
| `.claude/references/` | Check-lists : accessibilité, performance, sécurité, définition de « fini », tests |
| `licenses/`, `scripts/` | Licences des sources ; `sources.txt` + `sync.sh` pour mettre à jour |

## Compétences
| Étape | Compétences |
|---|---|
| Cadrer | `interview-me`, `idea-refine`, `spec-driven-development`, `constraint-driven-development`, `brainstorming` (sur demande : `/brainstorming`) |
| Planifier | `planning-and-task-breakdown`, `writing-plans`, `incremental-implementation`, `source-driven-development` |
| Coder | `frontend-ui-engineering`, `modern-javascript-patterns`, `error-handling-patterns`, `playground` (explorateurs HTML interactifs autonomes), `dispatching-parallel-agents` (plusieurs sous-agents en parallèle), `context-engineering` (donner à Claude le bon contexte) |
| Tester | `test-driven-development`, `javascript-testing-patterns`, `e2e-testing-patterns`, `browser-testing-with-devtools`, `webapp-testing` (Playwright, officiel Anthropic), `testing-strategy`, `verification-before-completion` |
| Corriger / relire | `systematic-debugging`, `debugging-and-error-recovery`, `receiving-code-review`, `code-review-and-quality`, `code-simplification`, `doubt-driven-development`, `tech-debt` |
| Durcir | `security-and-hardening`, `performance-optimization` |
| Livrer / documenter | `git-workflow-and-versioning`, `documentation-and-adrs`, `avoid-ai-writing`, `claude-md-improver`, `shipping-and-launch` (liste de contrôle avant mise en ligne), `finishing-a-development-branch` (clôturer une branche) |

## Sous-agents
| Source | Agents |
|---|---|
| Officiel Anthropic | `code-explorer`, `code-architect`, `code-reviewer`, `code-simplifier`, `silent-failure-hunter` (erreurs avalées en silence), `pr-test-analyzer`, `comment-analyzer` |
| agency-agents | `engineering-frontend-developer`, `engineering-minimal-change-engineer`, `engineering-privacy-engineer` (données financières et de santé), `engineering-rapid-prototyper`, `testing-reality-checker`, `testing-accessibility-auditor`, `testing-performance-benchmarker`, `testing-evidence-collector` |

## Sécurité
Chaque source a été vérifiée avant ajout (octobre 2026) : licence libre (MIT, Apache 2.0, domaine public), auteur identifié, projet actif.
Le code exécutable a été relu : pas de lecture de secrets, pas de consignes cachées, connexions réseau limitées à des CDN connus et à des banques d'images publiques.
Règle pour toute nouvelle source : même vérification avant de l'ajouter à `scripts/sources.txt`.

## Mise à jour
`bash scripts/sync.sh` puis commit. Pour changer la sélection : modifier `scripts/sources.txt`.
