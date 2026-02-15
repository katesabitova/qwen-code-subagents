# Подключение агентов Qwen Code

## Расположение агентов

Все агенты находятся в директории:
```
.qwen\agents\
```

Всего: **36 агентов**

## Категории агентов

### Development (15 агентов)

| Агент | Назначение |
|-------|------------|
| `agent-organizer.md` | Оркестратор для сложных многоэтапных задач |
| `frontend-developer.md` | Senior frontend engineer (React, TypeScript, доступность) |
| `backend-architect.md` | Архитектор бэкенда (микросервисы, API, базы данных) |
| `python-pro.md` | Эксперт Python (декораторы, async, оптимизация) |
| `golang-pro.md` | Go инженер (goroutines, каналы, производительность) |
| `typescript-pro.md` | TypeScript эксперт (generics, типизация, архитектура) |
| `react-pro.md` | React специалист (Hooks, компоненты, оптимизация) |
| `nextjs-pro.md` | Next.js эксперт (SSR/SSG, App Router, деплой) |
| `full-stack-developer.md` | Full-stack разработчик |
| `mobile-developer.md` | Мобильный разработчик (React Native, Flutter) |
| `ui-designer.md` | UI дизайнер (визуальный дизайн, компоненты) |
| `ux-designer.md` | UX дизайнер (пользовательский опыт, исследования) |
| `electron-pro.md` | Electron разработчик (десктоп приложения) |
| `dx-optimizer.md` | DX оптимизатор (инструменты, процессы) |
| `legacy-modernizer.md` | Специалист по модернизации legacy систем |

### Infrastructure (5 агентов)

| Агент | Назначение |
|-------|------------|
| `cloud-architect.md` | Cloud архитектор (AWS/Azure/GCP, Terraform) |
| `deployment-engineer.md` | DevOps инженер (CI/CD, Kubernetes, Docker) |
| `performance-engineer.md` | Performance инженер (оптимизация, нагрузочное тестирование) |
| `devops-incident-responder.md` | Incident response для DevOps |
| `incident-responder.md` | Incident Commander (SRE практики) |

### Quality Testing (5 агентов)

| Агент | Назначение |
|-------|------------|
| `debugger.md` | Специалист по отладке |
| `code-reviewer.md` | Рецензент кода |
| `qa-expert.md` | QA эксперт (тестирование, качество) |
| `test-automator.md` | Автоматизация тестирования |
| `architect-reviewer.md` | Архитектурный ревьюер |

### Data & AI (7 агентов)

| Агент | Назначение |
|-------|------------|
| `data-engineer.md` | Data Engineer (Spark, Airflow, Kafka) |
| `data-scientist.md` | Data Scientist (SQL, BigQuery, аналитика) |
| `ml-engineer.md` | ML Engineer (MLOps, деплой моделей) |
| `ai-engineer.md` | AI Engineer (LLM, RAG, prompt engineering) |
| `database-optimizer.md` | Оптимизация баз данных |
| `graphql-architect.md` | GraphQL архитектор |
| `postgresql-pro.md` | PostgreSQL эксперт |

### Security, Specialization & Business (4 агента)

| Агент | Назначение |
|-------|------------|
| `security-auditor.md` | Security аудитор (pentesting, OWASP) |
| `api-documenter.md` | API документация (OpenAPI, Postman) |
| `documentation-expert.md` | Технический писатель |
| `product-manager.md` | Product Manager |

## Подключение в Qwen Code

### Автоматический вызов

Qwen Code автоматически анализирует запрос и выбирает подходящего агента на основе контекста:

```bash
# Примеры автоматического вызова
"Найди и исправь баг" → debugger
"Спроектируй REST API" → backend-architect
"Оптимизируй запросы к БД" → database-optimizer
"Создай документацию API" → api-documenter
```

### Явный вызов

Для указания конкретного агента:

```bash
"Используй debugger для анализа ошибки в app.py"
"Примени code-reviewer для проверки качества"
"Используй agent-organizer для анализа проекта"
```

### Использование agent-organizer

**agent-organizer** анализирует проект и формирует рекомендации:

1. Анализирует структуру проекта
2. Формирует команду агентов
3. Планирует последовательность выполнения
4. Определяет критерии успеха

## Структура файла агента

```markdown
---
name: agent-name
description: Когда использовать этого агента
tools: read_file, write_file, Edit, Grep, Glob, Bash, TodoWrite, Task, WebSearch, WebFetch
---

# Agent Name

**Role**: Описание роли

**Expertise**: Области экспертизы

**Key Capabilities**:
- Возможность 1
- Возможность 2

## Core Development Philosophy
...

## Core Competencies
...

## Guiding Principles / Standard Operating Procedure
...
```

## Быстрый справочник

| Задача | Агент |
|--------|-------|
| Отладка ошибок | `debugger` |
| Рецензирование кода | `code-reviewer` |
| Архитектура бэкенда | `backend-architect` |
| Frontend разработка | `frontend-developer`, `react-pro` |
| DevOps/CI-CD | `deployment-engineer` |
| Incident response | `incident-responder`, `devops-incident-responder` |
| Тестирование | `test-automator`, `qa-expert` |
| Data engineering | `data-engineer`, `database-optimizer` |
| ML/AI системы | `ml-engineer`, `ai-engineer` |
| Безопасность | `security-auditor` |
| Документация | `api-documenter`, `documentation-expert` |
| Оркестрация | `agent-organizer` |

## Workflow примеры

### Полный цикл разработки фичи

```
1. agent-organizer → Анализ требований, формирование команды
2. backend-architect / frontend-developer → Проектирование
3. security-auditor → Проверка безопасности
4. test-automator → Написание тестов
5. code-reviewer → Финальная проверка
```

### Incident response

```
1. incident-responder → Координация
2. devops-incident-responder → Техническое расследование
3. cloud-architect → Если проблема в инфраструктуре
```

### Data pipeline

```
1. data-engineer → Проектирование pipeline
2. database-optimizer → Оптимизация запросов
3. postgresql-pro → Если используется PostgreSQL
```

## Дальнейшие шаги

1. Добавить агенты в конфигурацию Qwen Code
2. Протестировать интеграцию с реальными проектами
