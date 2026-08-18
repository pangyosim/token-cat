# TokenCat

고양이가 Claude 토큰 사용량을 알려줘요.

메뉴바의 픽셀 고양이가 Claude의 작업 상태를 모션으로, 남은 토큰을 게이지로 보여주는 앱입니다.
이 저장소는 공개 배포(다운로드 페이지 + 릴리스) 전용입니다.

**다운로드: https://pangyosim.github.io/token-cat/**

또는 [Releases](https://github.com/pangyosim/token-cat/releases/latest)에서 직접 받을 수 있습니다.

## 지원 플랫폼

| 플랫폼 | 파일 |
|---|---|
| macOS (Apple Silicon) | `TokenCat-x.y.z-arm64.dmg` |
| macOS (Intel) | `TokenCat-x.y.z.dmg` |
| Windows (x64) | `Token.Cat-x.y.z-win.zip` |
| Windows (ARM64) | `Token.Cat-x.y.z-arm64-win.zip` |

## 고양이 모션

마지막 Claude 활동 시각에 따라 고양이의 모션이 바뀝니다.

| 모션 | 의미 |
|---|---|
| 달리기 | Claude가 지금 일하는 중 |
| 공놀이 | 10분 안에 활동이 있었음 |
| 리듬 타기 | 1시간 안에 활동이 있었음 |
| 잠자기 | 한동안 조용함 |

게이지는 쓴 토큰만큼 차오르고 초록 → 노랑 → 빨강으로 경고합니다.

## 설치 안내

무서명 개인 빌드라 처음 한 번만 아래 과정이 필요합니다.

- **macOS**: 앱을 우클릭 → 열기 하거나 `xattr -cr /Applications/TokenCat.app` 실행
- **Windows**: zip 압축을 풀고 `TokenCat.exe` 실행 (SmartScreen이 뜨면 추가 정보 → 실행)

## 배포 메모

다운로드 페이지(`index.html`)는 최신 릴리스를 GitHub API로 읽어오므로,
새 버전은 릴리스만 올리면 됩니다:

```
gh release create vX.Y.Z -R pangyosim/token-cat dist/*.dmg dist/*win.zip
```
