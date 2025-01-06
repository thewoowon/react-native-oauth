# @thewoowon/react-native-oauth

**한국 서비스에 최적화된, 완벽한 OAuth 통합 라이브러리 for React Native**

`@thewoowon/react-native-oauth`는 React Native 환경에서 **Google, Kakao, Naver, Line** 등 한국을 포함한 다양한 OAuth 2.0 기반 로그인을 손쉽게 통합할 수 있는 종합 라이브러리입니다.

✅ **주요 기능**

- **국내 서비스 완벽 지원**: Kakao, Naver, Line과 같은 국내 OAuth 제공자 지원
- **글로벌 서비스 호환**: Google, Apple, Facebook 등의 글로벌 OAuth 플랫폼 지원
- **손쉬운 사용성**: `useOAuthLogin()` 훅으로 간편하게 로그인 로직 작성
- **스타일 커스터마이징 가능**: 기본 제공 버튼 디자인은 물론, 손쉬운 커스텀 지원
- **TypeScript 완벽 지원**: 안정적인 타입 관리 및 자동 완성 기능 제공
- **보안 강화**: PKCE 지원, JWT 기반 토큰 검증

---

## 📦 설치

```bash
npm install @thewoowon/react-native-oauth
```

## 🚀 사용법

```tsx
import React from 'react';
import { useOAuthLogin, OAuthButton } from '@thewoowon/react-native-oauth';

const LoginScreen = () => {
  const { login, isLoading } = useOAuthLogin('kakao');

  return (
    <OAuthButton
      provider="kakao"
      onPress={login}
      loading={isLoading}
    />
  );
};

export default LoginScreen;
```

---

## 🌟 지원하는 OAuth 플랫폼

- ✅ Kakao
- ✅ Naver
- ✅ Line
- ✅ Google
- ✅ Apple
- ✅ Facebook

---

## 🎨 커스텀 버튼 디자인

```tsx
<OAuthButton
  provider="naver"
  style={{ backgroundColor: '#1EC800', borderRadius: 10 }}
  textStyle={{ fontWeight: 'bold' }}
/>
```

---

## 📖 API

### `useOAuthLogin(provider: string)`

- **`provider`**: `kakao`, `naver`, `line`, `google`, `apple`, `facebook`
- **반환값**: `{ login, logout, isLoading, userInfo }`

### `<OAuthButton />`

- **`provider`**: 로그인 제공자 (필수)
- **`onPress`**: 버튼 클릭 시 호출될 함수
- **`style`**: 버튼 스타일 커스텀
- **`textStyle`**: 버튼 텍스트 스타일 커스텀

---

## 🔒 보안

- **PKCE 지원** (Proof Key for Code Exchange)
- **JWT 기반 사용자 데이터 검증**
- **OAuth 2.0 표준 준수**

---

## 🌐 라이선스

[MIT](LICENSE)

---

## ⭐ 기여

이 프로젝트는 오픈소스입니다. Issue와 PR을 통해 자유롭게 기여해주세요!

---

> @thewoowon/react-native-oauth – **한국 서비스에 최적화된, 최고의 OAuth 라이브러리!**

