# CLAUDE.md

## Uppgiftsdump (claude-todo)

Roger lägger uppgifter som GitHub-issues med etiketten `claude-todo` när han inte är på kontoret.

- I början av varje session: hämta öppna uppgifter med
  `gh api "repos/rogeraberg/hoppborg/issues?labels=claude-todo&state=open" --jq '.[] | "#\(.number) \(.title)"'`
  (GraphQL-baserade `gh issue`-kommandon fungerar inte i Claude Code på webben, använd REST.)
- Finns det öppna uppgifter: nämn dem kort och fråga om du ska ta dem nu. Läs hela issuen med kommentarer (`gh api repos/rogeraberg/hoppborg/issues/N` och `.../issues/N/comments`) innan du börjar.
- En issue i taget, på egen branch. Skriv `Closes #N` i PR:en så stängs issuen vid merge.
- Är något oklart: fråga Roger hellre än att gissa.
