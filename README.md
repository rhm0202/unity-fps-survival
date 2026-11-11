# Unity FPS Survival Crafting

> 3D FPS 생존 크래프팅 | Unity 6 (URP 3D) | 메타버스 플랫폼 수업 프로젝트

메타버스 플랫폼 수업에서 주차별 강의를 따라 만든 3D FPS 생존 크래프팅 게임입니다.
Unity 3D 게임 개발의 핵심 기법을 익히는 것이 목표였습니다.

---

## 프로젝트 개요

| 항목 | 내용 |
|---|---|
| 장르 | 3D FPS 생존 크래프팅 |
| 엔진 | Unity 6.3 (6000.3.11f1), URP 3D |
| 수업 | 메타버스 플랫폼 |
| 기간 | 2026.04.03 ~ 2026.05.22 |
| 플랫폼 | PC / Mobile (렌더 파이프라인 분리 구성) |

---

## 핵심 게임플레이

- **자원 수집**: 곡괭이로 돌을 캐면 아이템 드롭
- **인벤토리**: 아이템 획득·보관·드래그&드롭 슬롯 이동
- **전투**: SubMachineGun으로 동물(Pig) 사냥
- **회복**: 소비 아이템 우클릭으로 HP·DP·배고픔·갈증 회복
- **생존**: 체력·스태미나·배고픔·갈증 관리

## 조작법

| 키 | 동작 |
|---|---|
| `W / A / S / D` | 이동 |
| `Left Shift` / `Left Ctrl` / `Space` | 달리기 / 앉기 / 점프 |
| `좌클릭` | 공격 / 채집 |
| `우클릭` | 정조준 / 인벤토리에서 장비 장착·소비 아이템 사용 |
| `E` | 아이템 줍기 |
| `I` | 인벤토리 열기/닫기 |
| `1` / `2` / `3` / `4` | 맨손 / 총기 / 도끼 / 곡괭이 |
| `R` | 재장전 |

---

## 수업에서 배운 내용

| 주제 | 내용 |
|---|---|
| 물리 기반 이동·카메라 | Rigidbody 이동, `Mathf.Clamp`로 시점 회전 제한 |
| 코루틴과 Lerp | 앉기 시 카메라 전환, 무기 교체·공격 딜레이 |
| 레이캐스트 | 총기·근접 공격 판정, 아이템 줍기 |
| 상속과 추상 클래스 | `CloseWeaponController` 기반 맨손·도끼·곡괭이 |
| 애니메이터 연동 | `SetBool`·`SetTrigger`로 애니메이션 제어 |
| ScriptableObject | `CreateAssetMenu`로 아이템 데이터를 코드와 분리 |
| UI 이벤트 인터페이스 | 드래그·드롭·포인터 Handler로 인벤토리와 툴팁 구현 |
| 싱글톤 매니저 | SoundManager 효과음 관리 |
| 간단한 동물 AI | 랜덤 행동 전환, 피격 시 도주 |
| 프리팹 인스턴스화 | 채굴 시 아이템 랜덤 개수 드롭 |
| URP 설정 | PC·Mobile 렌더 에셋 분리 |

> 강의 코드를 Unity 6에서 진행하며 생긴 Input System·애니메이션 연결 문제를 수정했고, 수정 사항이 이후 수업 기준 코드에 반영되었습니다.

---

## 프로젝트 구조

```
Assets/
├── script/
│   ├── Player/          # PlayerController
│   ├── Weapon/          # Gun, GunController, CloseWeapon, Hand/Axe/PickaxeController, WeaponManager, WeaponSway
│   ├── UI/              # Crosshair, HUD, Inventory, Slot, DragSlot, SlotToolTip, StatusController
│   ├── Item/            # Item, ItemPickUp, ActionController
│   ├── Environment/     # Rock, Pig
│   └── Manager/         # SoundManager, ItemEffectDatabase
├── Prefab/ Animation/ Scenes/ Settings/ ...
```

## 기술 스택

- **Engine**: Unity 6, URP 3D
- **Language**: C#
