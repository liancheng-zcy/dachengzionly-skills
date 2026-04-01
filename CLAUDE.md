# CLAUDE.md

Development guidelines for dachengzionly-skills repository.

## Project Overview

This is a Claude Code plugin marketplace providing skills based on Munger's thinking framework. Each skill is a structured workflow for decision-making and productivity.

## Key Files

| File | Purpose |
|------|---------|
| `.claude-plugin/marketplace.json` | Marketplace definition, version number |
| `.claude-plugin/plugin.json` | Plugin config, points to skills directory |
| `skills/<name>/SKILL.md` | Skill content with frontmatter |

## Development Rules

### Adding New Skill

1. Create `skills/<skill-name>/SKILL.md`
2. Required frontmatter:

   ```yaml
   ---
   name: skill-name
   description: One-line description。触发场景：用户说"..."
   ---
   ```

3. Structure: 使用场景 → 核心概念 → 执行流程 → 检查清单

### Version Management

- Version in `marketplace.json` `metadata.version`
- Bump version when skill content changes
- Users receive updates only when version changes

### Plugin.json Format

Correct:

```json
{
  "skills": "./skills/"
}
```

Wrong (will cause plugin load failure):

```json
{
  "skills": [
    { "name": "...", "path": "..." }
  ]
}
```

### Git Workflow

- Commit each skill separately
- Use conventional commits: `feat:`, `fix:`, `docs:`, `chore:`
- Keep eval data (`munger-*`) in .gitignore, never commit

## Testing

Eval data goes to `munger-skills-workspace/` and `munger-skills-workflow/` directories (gitignored).

## Commit Checklist

Before committing:

- [ ] SKILL.md has valid frontmatter
- [ ] `metadata.version` bumped if skill changed
- [ ] No eval/test data included
- [ ] README.md updated if new skill added