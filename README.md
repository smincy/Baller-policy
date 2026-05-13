# Baller Policy

Baller 앱의 개인정보처리방침 정적 웹페이지입니다.

## 파일 구성

```
Baller-policy/
├── index.html      # privacy.html로 자동 리다이렉트
├── privacy.html    # 개인정보처리방침 본문
└── README.md
```

## GitHub Pages 배포 방법

### 1. 이 repo를 GitHub에 push

```bash
cd Baller-policy
git init
git branch -M main
git add .
git commit -m "Add Baller privacy policy page"
git remote add origin https://github.com/smincy/Baller-policy.git
git push -u origin main
```

### 2. GitHub Pages 활성화

1. GitHub에서 `smincy/Baller-policy` repo로 이동
2. **Settings** → **Pages**
3. **Source** 섹션에서 Branch: `main` / Folder: `/ (root)` 선택
4. **Save** 클릭
5. 수 분 후 배포 완료

### 3. 배포 후 공개 URL

| URL | 내용 |
|-----|------|
| `https://smincy.github.io/Baller-policy/` | index.html → privacy.html로 리다이렉트 |
| `https://smincy.github.io/Baller-policy/privacy.html` | 개인정보처리방침 본문 직접 접근 |

## 앱 URL 상수 업데이트

GitHub Pages 배포 후 Baller 앱의 아래 상수를 실제 URL로 변경하세요.

파일: `FE/app/(tabs)/profile.tsx`

```ts
// 배포 전 (임시)
const PRIVACY_POLICY_URL = 'https://baller.app/privacy';

// 배포 후 (GitHub Pages)
const PRIVACY_POLICY_URL = 'https://smincy.github.io/Baller-policy/privacy.html';
```

## 내용 수정 방법

- **문의 이메일**: `privacy.html` 파일에서 `privacy@baller.app` 검색 후 교체
- **운영자명**: `서비스 운영자` 텍스트 교체
- **시행일**: `2026년 5월 13일` 검색 후 교체
