# 설치 안내

## 준비물

- 대상 일본판 GBA ROM
- `xdelta3`
- 저장소 루트의 `Summon_Night_Craft_Sword_Monogatari_KO.xdelta`

원본 ROM은 이 저장소에서 제공하지 않습니다.

## 원본 확인

```powershell
Get-FileHash "Summon Night - Craft Sword Monogatari (Japan).gba" -Algorithm SHA256
```

정상 원본은 크기 `8,388,608 bytes`, SHA-256 `3f7ec3d21d8f2fa5bac04afe31f9e5d4e93176ab3e79a9138925c67546663a4f`입니다. 해시가 다르면 적용하지 마십시오.

## 자동 적용과 검증

```powershell
python scripts/apply_patch.py "Summon Night - Craft Sword Monogatari (Japan).gba"
```

기본 출력은 `summon_night_craft_sword_ko.gba`입니다. 출력 경로와 xdelta 실행 파일을 직접 지정할 수도 있습니다.

```powershell
python scripts/apply_patch.py "원본.gba" "내 폴더/서몬나이트 한국어.gba" `
  --xdelta "C:\Tools\xdelta3.exe"
```

## 직접 적용

```powershell
xdelta3 -d -s "Summon Night - Craft Sword Monogatari (Japan).gba" `
  "Summon_Night_Craft_Sword_Monogatari_KO.xdelta" `
  "summon_night_craft_sword_ko.gba"
```

## 결과 확인

```powershell
Get-FileHash "summon_night_craft_sword_ko.gba" -Algorithm SHA256
```

- 크기: `16,777,216 bytes`
- SHA-256: `235c901f5d37f6cc7d8286f2446ad300d8cb81830895e686638a52d659500d10`

기존 일본판 세이브를 사용하기 전에는 별도 백업을 권장합니다.

기존 버전의 결과 ROM에 다시 적용하지 말고, 항상 위 해시의 깨끗한 일본판 원본에 `v1.0.3` 패치를 적용하십시오.
