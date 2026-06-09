# TOTEM Keymap 참고

> ZMK 펌웨어 / 동글(Prospector) 기반 / 5레이어 구성

---

## 레이아웃 개요

```
왼쪽 엄지  : Esc(길게=Fn)  Space  Ctrl
오른쪽 엄지 : Bspc         Enter  Tab(길게=Num)
```

---

## Layer 0 — Base (기본)

```
  Q    W    E    R    T  │  Y    U    I    O    P
  A    S    D    F    G  │  H    J    K    L    ;
⇧ Z    X    C    V    B  │  N    M    ,    .    /  ⇧
            Esc  SPC CTRL│ BSPC ENT  TAB
           (Fn)          │      (Num)
```

| 키 | 동작 |
|---|---|
| 왼쪽 새끼손가락 (⇧) | 탭 = Shift / 더블탭 = CapsLock |
| 오른쪽 새끼손가락 (⇧) | 탭 = Shift / 더블탭 = `'` |
| Esc 엄지 | 탭 = Esc / 길게 = Fn 레이어 |
| Tab 엄지 | 탭 = Tab / 길게 = Num 레이어 |

---

## Layer 1 — Num `[Tab 길게]`

```
  1    2    3    4    5  │ Home PgUp PgDn End   ·
  6    7    8    9    0  │  ←    ↓    ↑    →    ·
  ·    ·    ·    ·    .  │  +    -    *    /    =    ·
            ·    ·    ·  │  ·    ·    ·
```

---

## Layer 2 — Fn `[Esc 길게]`

```
  F1   F2   F3   F4   F5  │  ·      ·      ·       ·    ·
  F6   F7   F8   F9  F10  │ Alt+F4 선택줄 Win⇧S  Boot  ·
  ·   F11  F12   ·    ·   │  ·      ·      [       ]    \    ·
            ·    ·    ·   │  Del    ·      ·
```

| 단축키 | 결과 |
|---|---|
| Fn + , | `[` |
| Fn + . | `]` |
| Fn + / | `\` |
| Fn + Bspc | Del |
| Fn + H | Alt+F4 (창 닫기) |
| Fn + J | 현재 줄 선택 (Home → Shift+End) |
| Fn + K | Win+Shift+S (캡처 도구) |
| Fn + L | 펌웨어 부트로더 진입 |

---

## Layer 3 — Mac `[양쪽 새끼손가락 동시]`

```
  ·    ·    ·    ·    ·  │  ·    ·    ·    ·    ·
  ·    ·    ·    ·    ·  │  ·    ·    ·    ·    ·
  ·    ·    ·    ·    ·  │  ·    ·    ·    ·    ·    ·
            ·    ·   ⌘   │  ·    ·    ·
```

- Ctrl 엄지 → ⌘ (Command) 로 변경
- J+K 콤보 → Ctrl (Mac에서)
- D+F 콤보 → Option (그대로)
- **왼쪽 Shift + Space → CapsLock (한/영 전환)**

---

## Layer 4 — MacFn `[Mac 모드 + Fn 동시]`

```
  ·    ·    ·    ·    ·  │  ·      ·      ·       ·    ·
  ·    ·    ·    ·    ·  │  ⌘Q     ·     ⌘⇧4      ·    ·
  ·    ·    ·    ·    ·  │ ⌘⌥←  ⌘⌥↓  ⌘⌥↑  ⌘⌥→   ·    ·
            ·    ·    ·  │  ·      ·      ·
```

| 단축키 | 결과 |
|---|---|
| MacFn + H | ⌘Q (앱 종료) |
| MacFn + K | ⌘⇧4 (스크린샷) |
| MacFn + N/M/,/. | ⌘⌥ + 방향키 (창 스냅) |

---

## 콤보 정리

| 조합 | 결과 | 레이어 |
|---|---|---|
| J + K | Win키 (sticky) | Base |
| J + K | Ctrl (sticky) | Mac |
| D + F | Alt / Option (sticky) | Base, Mac |
| 양쪽 새끼손가락 동시 | Mac 모드 토글 | 전체 |
| 왼쪽 Shift + Space | CapsLock (한/영 전환) | Mac, MacFn |

> sticky = 한 번 누르면 다음 키 하나에만 적용 후 해제

---

## 맥 한/영 전환 설정

시스템 설정 → 키보드 → 키보드 단축키 → 입력 소스  
→ **"다음 입력 소스 선택"** 단축키가 `Caps Lock` 으로 되어 있으면 됨 (macOS 기본값)

실제 CapsLock이 필요할 때 : **Shift + CapsLock** (= Shift + 왼쪽 새끼 더블탭)

---

## 펌웨어 플래싱

키맵 변경 시 **동글(Prospector)만** 플래싱하면 됨.  
왼쪽/오른쪽은 키 위치 신호만 전송하므로 키맵 변경과 무관.

빌드 결과물: GitHub Actions → `totem-prospector` 브랜치 푸시 후 자동 빌드
