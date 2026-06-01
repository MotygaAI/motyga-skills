# Contributing a skill

Thanks for adding to Motyga Skills! Keep it simple and clean.

## Rules

1. **One skill per directory** under `skills/<skill-id>/` with `skill.yaml` + `SKILL.md`.
2. **Your own content only.** Do not submit proprietary, leaked, copied, or license-incompatible
   prompts/content. Vendor system prompts are not accepted unless their license permits redistribution.
3. **Attribution.** If a skill is *inspired by* someone, credit them in `skill.yaml → attribution`.
   Inspiration is fine; copying is not.
4. **No secrets.** No API keys, tokens, private URLs, customer data, or internal endpoints — anywhere
   (including examples). PRs are secret-scanned.
5. **Apache-2.0.** By contributing you agree your contribution is licensed under Apache-2.0 and that
   you have the right to submit it.
6. **Model-agnostic.** A skill must not hard-depend on one vendor; it should work on any capable model.

## PR checklist

- [ ] `skill.yaml` is valid and complete (id, name, summary, category, license, permissions).
- [ ] `SKILL.md` is self-contained and safe (least-privilege `permissions`).
- [ ] No secrets / private data / copied proprietary prompts.
- [ ] I have the rights to submit this content under Apache-2.0.
- [ ] Optional `examples/` are sanitized.

## Categories

`coding` · `research` · `content` · `data` · `creative` · `security`
