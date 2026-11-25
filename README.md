# PlaySnack for Claude

[한국어](#한국어) · [English](#english)

## 한국어

[PlaySnack](https://playsnack.app/)은 링크 하나로 각자 폰 브라우저에서 같이 하는 파티 게임 모음이에요. 이 저장소는 Claude에 PlaySnack 커넥터(원격 MCP 서버 `https://playsnack.app/mcp`)를 추가하는 플러그인 설정만 담고 있어요.

### Claude에 추가하기

**Claude 앱**: 설정 → 플러그인 → 추가 → 마켓플레이스 추가 → URL에 `playsnack/playsnack-claude` 입력 → 목록에서 **PlaySnack** 설치

**Claude Code**:

```bash
claude plugin marketplace add playsnack/playsnack-claude
claude plugin install playsnack@playsnack
```

로그인이나 API 키는 필요 없어요.

### 할 수 있는 것 (도구 4개)

| 도구 | 하는 일 |
|---|---|
| `recommend_games` | 인원·분위기·시간에 맞는 게임 최대 5개 추천 |
| `list_games` | 전체 게임 목록 |
| `get_game` | 게임 하나의 규칙 |
| `open_friend_room` | 친구 방 열기: 모두 여는 참여 링크 하나 + QR |

예: "6명이 10분 동안 할 게임 추천해 줘", "그 게임으로 방 열어 줘"

- 개인정보처리방침: https://playsnack.app/privacy/
- 문의: contact@playsnack.app

## English

[PlaySnack](https://playsnack.app/) is a set of party games played together from one link, each person in their own phone browser. This repository only holds the plugin config that adds the PlaySnack connector (remote MCP server `https://playsnack.app/mcp`) to Claude.

### Add it to Claude

**Claude app**: Settings → Plugins → Add → Add marketplace → enter `playsnack/playsnack-claude` → install **PlaySnack** from the list

**Claude Code**:

```bash
claude plugin marketplace add playsnack/playsnack-claude
claude plugin install playsnack@playsnack
```

No login or API key needed.

### What it can do (4 tools)

| Tool | What it does |
|---|---|
| `recommend_games` | Up to 5 games that fit a group's size, mood and time |
| `list_games` | Every game |
| `get_game` | One game's rules |
| `open_friend_room` | Opens a friends room: one join link for everyone, plus a QR page |

Example: "Suggest a game for 6 people for 10 minutes", "Open a room for that game"

- Privacy policy: https://playsnack.app/privacy/
- Support: contact@playsnack.app

## Repository layout

| Path | Purpose |
|---|---|
| `.claude-plugin/marketplace.json` | Claude plugin marketplace |
| `plugins/playsnack/` | Claude plugin (`.claude-plugin/plugin.json`, `.mcp.json`, `icon.png`) |
| `openai/` | [Agent Plugins 1.0.0](https://agent-plugins.org/) manifest (`plugin.json`, `mcp.json`) |

Config files: MIT ([LICENSE](LICENSE)).
