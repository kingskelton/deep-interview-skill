# DevBrother Skills

개발동생이 실제 작업 흐름에서 사용하는 Agent Skills 공유 저장소입니다.

첫 공개 스킬은 `deep-interview`입니다. 앞으로 다른 스킬도 하나씩 추가할 예정입니다.

## Skills

| Skill | 설명 |
|---|---|
| [`deep-interview`](deep-interview/SKILL.md) | 러프한 요청을 바로 실행하지 않고, AI가 사용자에게 한 번에 하나씩 질문하여 목표, 범위, 제약, 완료 기준을 구체화하도록 만드는 스킬 |

## deep-interview

`deep-interview`는 프롬프트를 처음부터 완벽하게 쓰기 어려운 상황에서 사용합니다. 핵심은 AI에게 바로 실행을 맡기는 것이 아니라, AI가 역으로 사용자를 인터뷰하게 만들어 요구사항을 명확히 하는 것입니다.

질문은 한 번에 하나만 묻고, 매 질문은 아래 구조를 따릅니다.

```md
현재 이해: {요청을 한 문장으로 요약}
막힌 결정: {가장 중요한 불확실성}
추천 답안: {있으면 제시}
질문: {한 가지 질문}
```

## 설치 예시

Codex 계열:

```bash
mkdir -p ~/.agents/skills
cp -R deep-interview ~/.agents/skills/deep-interview
```

Claude Code 계열:

```bash
mkdir -p ~/.claude/skills
cp -R deep-interview ~/.claude/skills/deep-interview
```

## 라이선스

MIT
