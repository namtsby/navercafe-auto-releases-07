# 네이버 카페 통합 자동화 — 배포 저장소

이 저장소는 **설치용 zip·sha256·update.json만** 보관하는 공개 릴리스 저장소입니다.  
소스 코드는 별도 비공개 저장소에서 관리합니다.

## 최신 버전

- Version: **1.0.0**
- ZIP: `NaverCafeManager-1.0.0.zip`
- SHA256: `904555f6da0c8c9b00fbc564f7194876446e46f0835c4b34244dbb9ebcc37c16`

## 설치

1. 최신 Release의 `NaverCafeManager-1.0.0.zip` 다운로드
2. 압축 해제
3. `install.bat` 실행
4. 바탕화면 `네이버 카페 통합 자동화` 실행
5. 설치 위치: `%LOCALAPPDATA%\NaverCafeManager\app`
6. 관리자 권한 불필요

## 업데이트 구조

`update.json`에 최신 버전, zip URL, 크기, sha256, 필수 여부, 채널을 기록합니다.

```json
{
  "version": "1.0.0",
  "min_version": "1.0.0",
  "mandatory": false,
  "channel": "stable",
  "asset": {
    "url": "https://github.com/namtsby/navercafe-auto-releases-07/releases/download/v1.0.0/NaverCafeManager-1.0.0.zip",
    "size": 131716189,
    "sha256": "904555f6da0c8c9b00fbc564f7194876446e46f0835c4b34244dbb9ebcc37c16"
  }
}
```

> 현재 v1.0.0은 설치 zip을 내려받아 `install.bat`으로 교체하는 방식입니다.  
> 앱 내부 자동 다운로드/폴더 교체는 별도 업데이트 클라이언트가 필요합니다.  
> 자동 업데이트 클라이언트가 추가되면 이 `update.json` 계약을 그대로 사용합니다.

## 릴리스 자산

- `NaverCafeManager-1.0.0.zip` — 설치용 onedir 패키지
- `NaverCafeManager-1.0.0.zip.sha256` — 무결성 확인
- `update.json` — 업데이트 메타데이터

## 보안

- 실행 파일/zip에 GitHub 토큰이나 API 키를 포함하지 않습니다.
- 계정 비밀번호는 결과/로그에 기록하지 않습니다.
- 본 프로그램은 본인 소유/운영 권한이 있는 계정과 카페에만 사용해야 합니다.
