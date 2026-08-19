# 서몬나이트 크래프트 소드 이야기 한국어 패치

> **v1.0.3 공개 릴리스**

게임보이 어드밴스 일본판 `Summon Night - Craft Sword Monogatari`용 비공식 한국어 현지화 패치 배포 저장소입니다.

- 게임 코드: `AB4J`
- 지원 원본 크기: `8,388,608 bytes`
- 지원 원본 SHA-256: `3f7ec3d21d8f2fa5bac04afe31f9e5d4e93176ab3e79a9138925c67546663a4f`
- 버전·태그: `v1.0.3`
- 저장소: `TeamLimRyan/SUMMON_NIGHT_CRAFT_SWORD_MONOGATARI_KOREAN_LOCALIZATION_RELEASE`

## 포함 범위

- 활성 텍스트 30,812행 한국어화
- 이미지 텍스트 자산 72개와 런타임 타이틀·메뉴 보정 5건 반영
- 무기 종류별 아이콘·비전 판정 회귀와 도끼·창·드릴 계열 진행 정지 방지 수정
- 장비·비전·액세서리·아이템·귀중품 이름 표시를 한글 문자열로 연결
- 하단 메뉴의 `LR:캐릭터 전환`·`LR:입력 전환` 그래픽 한국어화
- 현대 한글 완성형 11,172자 글리프
- 조합식 한글 이름 입력과 한글 자모 키보드
- 용어집·제어 코드·포인터·압축·팔레트·보호 픽셀 정적 검증
- mGBA 부팅, 타이틀·메뉴, 이름 입력과 `임라이언`·`꽃`·`꼼`·`힣` 조합 확인

## 다운로드

최신 안정판은 [GitHub Releases의 v1.0.3](https://github.com/TeamLimRyan/SUMMON_NIGHT_CRAFT_SWORD_MONOGATARI_KOREAN_LOCALIZATION_RELEASE/releases/tag/v1.0.3)에서 받으십시오.

- 패치: `Summon_Night_Craft_Sword_Monogatari_KO.xdelta`
- 패치 크기: `928,771 bytes`
- 패치 SHA-256: `f1bc7801b4f3d402d8c0da161c6c24f79dcc5619a828f34001a90e8112938316`

이 저장소와 GitHub Release에는 원본 ROM, 완성 ROM, BIOS, 세이브 데이터를 포함하지 않습니다.

## 설치

Python 3과 `xdelta3`가 준비되어 있으면 저장소 루트에서 다음 명령으로 원본 확인, 패치 적용, 결과 검증을 한 번에 수행할 수 있습니다.

```powershell
python scripts/apply_patch.py "Summon Night - Craft Sword Monogatari (Japan).gba"
```

직접 적용할 때는 다음 명령을 사용합니다.

```powershell
xdelta3 -d -s "Summon Night - Craft Sword Monogatari (Japan).gba" `
  "Summon_Night_Craft_Sword_Monogatari_KO.xdelta" `
  "summon_night_craft_sword_ko.gba"
```

자세한 절차는 [설치 안내](INSTALL_KO.md), 지원 범위와 검증 한계는 [호환성](COMPATIBILITY_KO.md)을 확인하십시오.

## 결과 무결성

- 결과 크기: `16,777,216 bytes`
- 결과 SHA-256: `235c901f5d37f6cc7d8286f2446ad300d8cb81830895e686638a52d659500d10`

배포 xdelta를 지원 원본에 역적용한 결과가 최종 승인 ROM과 바이트 단위로 일치합니다. 전체 체크섬은 [SHA256SUMS.txt](SHA256SUMS.txt)에 있습니다.

## 오류 제보

[지원 안내](SUPPORT_KO.md)에 따라 원본·패치·출력 해시, xdelta 버전, 운영체제, 에뮬레이터 정보와 재현 순서를 Issues에 남겨 주십시오. ROM·BIOS·세이브 파일은 첨부하지 마십시오.

## 권리

이 프로젝트는 비공식 팬메이드 한국어 패치입니다. 게임, 상표, 로고와 원본 데이터의 권리는 각 권리자에게 있습니다. 사용자는 정당하게 보유한 대상 일본판 ROM을 직접 준비해야 합니다.
