---
publishDate: 2025-03-28T09:11:39Z
title: Obsidian + Cursor IED를 활용한 AI 기반 통합 환경 구축
excerpt: ''
image: https://images.unsplash.com/photo-1561069934-eee225952461?auto=format&fit=crop&w=2070&q=80
tags:
  - obsidian
  - cursor
category: research
metadata:
  canonical: https://your-blog.vercel.app/{{slug}}
sticker: emoji//1f4d6
---

# Obsidian & Cursor IED를 활용한 AI 기반 통합 환경 구축

> 오늘날의 AI 기술은 코드 생성, 문서 요약, 검색, 자동화 등 단순 반복 작업을 넘어 개발자 개인이 아이디어를 빠르게 구현하고 실행할 수 있는 환경을 제공하고 있습니다. 특히 대규모 언어 모델 GPT 등의 발전으로 기획 문서 작성이나 연구 일지와 같은 시간 소모적인 작업을 AI를 통해 빠르고 효율적으로 처리할 수 있는 가능성이 열렸습니다.

이 글에서는 AI 기반 생산성 도구 **Cursor**와 연결 중심 지식관리 도구 **Obsidian**을 조합하여, 개인 개발자가 기획부터 구현, 정리까지 하나의 흐름으로 수행할 수 있는 통합 개발 환경(Integrated Environment for Development, IED) 구축 사례를 소개합니다.

## 1. 글 작성과 지식 관리 도구 선정 배경 (Cursor + Obsidian)

통합 개발 환경을 설계하면서, 문서 **작성**과 **지식 관리**를 효율화할 수 있는 도구를 선정하는 것이 중요했습니다. 초안 작성 단계에는 AI 도구를 활용하고, 결과물의 체계적인 보관에는 지식관리 도구를 사용하는 조합을 고려했습니다.

### Cursor: AI 기반 코드 에디터

![[file/Pasted image 20250329070424.png]]

먼저 **Cursor**를 글 초안 작성 도구로 선택했습니다. Cursor는 VS Code 기반으로 GPT-4 등의 AI 모델을 통합한 AI 코드 에디터로서, 코드뿐 아니라 텍스트 작성에도 뛰어난 생산성을 보여줍니다 ([Cursor AI: The AI-powered code editor changing the game](https://daily.dev/blog/cursor-ai-everything-you-should-know-about-the-new-ai-code-editor-in-one-place#:~:text=,Pro%20plan%20for%20advanced%20features)).

예를 들어 자연어 프롬프트를 입력하면 코드나 설명을 자동 완성해주고, 오류를 바로잡거나 코드를 리팩터링해주기도 합니다 ([Cursor AI: The AI-powered code editor changing the game](https://daily.dev/blog/cursor-ai-everything-you-should-know-about-the-new-ai-code-editor-in-one-place#:~:text=,in%20JavaScript%2C%20Python%2C%20and%20TypeScript)). 실제 개발자들 사이에서도 Cursor는 _페어 프로그래밍_ 파트너처럼 작동하며 개발 속도를 높여주고, 문서화 작업까지 도와주는 도구로 주목받고 있습니다 ([Cursor AI: The AI-powered code editor changing the game](https://daily.dev/blog/cursor-ai-everything-you-should-know-about-the-new-ai-code-editor-in-one-place#:~:text=Key%20benefits%3A)).

주요 특징:

- 자연어 프롬프트를 통한 코드/텍스트 자동 완성
- 오류 수정 및 코드 리팩터링 지원
- 페어 프로그래밍 파트너 역할
- 문서화 작업 지원

이러한 능력을 통해 반복적인 코드 작성이나 문서 초안 작업을 대신함으로써, 개발자는 보다 창의적인 작업에 집중할 수 있게 됩니다.

### Obsidian: 연결 중심 지식관리 도구

![[file/Pasted image 20250329070322.png]]

다음으로 **Obsidian**을 지식관리 및 아카이빙 도구로 선정했습니다. Obsidian은 로컬 폴더의 Markdown 파일들을 기반으로 동작하는 노트 앱으로, 각 노트 사이를 하이퍼링크로 연결하여 거미줄처럼 얽힌 지식 베이스를 구축할 수 있습니다 ([A Guide to Obsidian: Local, Markdown-Powered Networked Notes — SitePoint](https://www.sitepoint.com/obsidian-beginner-guide/#:~:text=started%20quickly%20with%20this%20Obsidian,notes%20tutorial)).

이처럼 개별 파일들을 유기적으로 연결해줌으로써 마치 개인 위키나 '세컨드 브레인'처럼 활용할 수 있는 점이 큰 장점입니다. Obsidian을 사용하면 코드 스니펫, 아이디어 메모, 참고 자료 등을 한 곳에 모아 체계적으로 관리할 수 있고, 강력한 검색과 시각화(그래프 뷰)를 통해 필요한 정보를 빠르게 찾아낼 수 있습니다. 또한 수많은 플러그인으로 기능을 확장하거나 개인에 맞게 커스터마이징할 수 있기 때문에, 자신의 작업 흐름에 꼭 맞는 지식관리 환경을 구축할 수 있습니다.

주요 특징:

- 개인 위키/세컨드 브레인 기능
- 강력한 검색과 시각화(그래프 뷰)
- 플러그인 기반 기능 확장
- 코드 스니펫, 아이디어 메모 관리

### 통합 환경의 시너지 효과

이 두 도구를 결합함으로써 **AI의 생산성과 인간의 조직화 능력**을 한데 모을 수 있었습니다. Cursor를 통해 얻은 초안 콘텐츠를 Obsidian에 바로 저장하고 다듬음으로써, 아이디어 발상부터 정리까지의 사이클이 끊기지 않고 이어집니다. 예를 들어 Cursor가 생성한 코드 조각이나 설명을 Obsidian 노트에 저장해 두면, 이후 관련 주제로 글을 쓸 때 해당 노트를 쉽게 참조하거나 링크로 연결할 수 있습니다. 이러한 시너지를 통해 개발 과정의 **기획-작성-정리** 단계가 하나의 흐름으로 통합되었습니다.

## 2. 문서 구조 설계: 템플릿, 카테고리 설정 및 YAML 자동화

효율적인 글 작성과 관리를 위해서는 문서의 **구조를 미리 설계**하고 반복 작업을 줄이는 것이 중요합니다. 이를 위해 블로그 포스트용 **Markdown 템플릿**을 만들고, 카테고리/태그 체계를 정의했으며, 메타데이터는 **YAML** 형식으로 관리하도록 했습니다.

### 📦 1. 필요한 프로그램 설치

#### ✅ Obsidian

- 공식 사이트: [https://obsidian.md/](https://obsidian.md/)
- 설치 후, 새로운 Vault 생성 (예: `blog`)

#### ✅ Cursor (AI 코드 IDE)

- 사이트: [https://www.cursor.so](https://www.cursor.so)
- GitHub 계정으로 로그인 → 무료 플랜 또는 유료 플랜 선택

#### ✅ Git + GitHub 계정

- Git 설치: [https://git-scm.com](https://git-scm.com)
- GitHub에 레포지토리 생성 후, Obsidian Vault와 연동

#### ✅ Vercel 계정

- 사이트: [https://vercel.com](https://vercel.com)
- GitHub 계정 연동 → 배포할 프로젝트 연결

옵시디언 플러그인

### 📦 **옵시디언 기본 세팅**

---

옵시디언을 처음 설치하였으면 아마 백지와 같은 상태일 것이다.

비슷한 노트 앱이었던 노션과 비교하면 문서를 작성하기 위한,
알기쉬운 생성 아이콘도 없고.
글자의 크기, 색상을 바꾸는 방법도 테이블을 만드는 방법도 쉽게 만들 수 없다.

물론 md파일 작성에 친숙한 숙련자라면 문제가 없다만 그렇지 않다면 다음과 같은 세팅을 하는 것을 추천한다.

#### 🎨 1. **필수 설정 변경하기**

| 설정 항목                                | 추천 값                          |
| ---------------------------------------- | -------------------------------- |
| `설정 → 편집기 → 편집 모드`              | **라이브 프리뷰**                |
| `설정 → 편집기 → 자동 쌍괄호`            | ✅ 체크                          |
| `설정 → 파일 & 링크 → 기본 새 노트 위치` | 원하는 폴더 설정                 |
| `설정 → 인터페이스 → 테마`               | **Minimal** 또는 **Border** 추천 |

#### 🔌2. **설치된 플러그인 목록**

| 플러그인 이름             | 버전      | 개발자            | 설명                                      |
| ------------------- | ------- | -------------- | --------------------------------------- |
| **Advanced Tables** | 0.22.1  | Tony Grosinger | 마크다운 테이블 편집을 쉽게 만들어주는 플러그인              |
| **Calendar**        | 1.5.10  | Liam Cain      | Daily Note 기능과 연결된 달력 뷰 제공              |
| **Dataview**        | 0.5.68  | Michael Brenan | 노트 데이터를 쿼리하고 시각화할 수 있게 해주는 데이터 뷰 플러그인   |
| **Editing Toolbar** | 3.1.111 | Cumm           | Obsidian을 Word 스타일 툴바처럼 사용할 수 있게 해주는 도구 |
| **make.md**         | 1.0.9   | make.md        | 노트 작성과 개인 워크플로우를 통합 관리하기 위한 도구 모음       |
| **Metadata Menu**   | 0.8.7   | mdebelle       | 메타데이터 필드를 쉽게 생성, 수정할 수 있는 도구            |
| **Style Settings**  | 1.0.9   | mgmeyers       | 테마와 플러그인 스타일을 시각적으로 커스터마이징 가능           |
| **Templater**       | 2.11.1  | SilentVoid     | 템플릿 자동 삽입 및 스크립팅 자동화 기능                 |


### 📦 **Cursor 기본 세팅**

---

커서는 코드를 작성하기 위한 ide이다.
ide에 세팅에는 정답이 없으며 개발자의 작업 스타일마다 각이 각색이다. 하지만 기본적으로 추천할 수 있는 세팅은 있다 이 글에서는

1. 확장 프로그램
2. settings.json
3. cursor settings

#### 1. **Cursor 추천 확장 프로그램 목록**

| 확장 프로그램 이름                             | 버전       | 설명                   |
| -------------------------------------- | -------- | -------------------- |
| Bookmarks                              | 13.3.1   | 북마크 관리               |
| Astro                                  | 3.0.2    | Astro 개발 지원          |
| Tailwind CSS IntelliSense              | 0.11.1   | Tailwind CSS 지원      |
| npm Intellisense                       | 1.4.0    | NPM 자동 완성            |
| Path Intellisense                      | 2.8.4    | 파일 경로 자동 완성          |
| ESLint                                 | 2.4.2    | ESLint 통합            |
| ES7+ React/Redux/React-Native snippets | 4.4.3    | React/JS 코드 스니펫      |
| GitLens                                | 14.8.1   | Git 기능 확장            |
| EditorConfig for VS Code               | 0.16.4   | EditorConfig 지원      |
| Prettier - Code formatter              | 10.1.0   | Prettier 코드 포맷터      |
| Jest Runner                            | 0.4.59   | Jest 테스트 러너          |
| Auto Close Tag                         | 0.5.14   | 태그 자동 닫기             |
| Auto Rename Tag                        | 0.1.10   | 태그 자동 이름 변경          |
| Next.js snippets                       | 1.0.0    | Next.js 지원           |
| GraphQL                                | 0.8.11   | GraphQL 지원           |
| GraphQL: Syntax Highlighting           | 1.0.5    | GraphQL 문법 지원        |
| REST Client                            | 0.25.1   | REST API 클라이언트       |
| Comment Translate                      | 1.5.0    | 주석 번역                |
| DeepL                                  | 3.6.0    | DeepL 번역             |
| Git Graph                              | 1.30.0   | Git 그래프 시각화          |
| DotENV                                 | 1.0.1    | .env 파일 지원           |
| GraphQL for VSCode                     | 2.1.0    | GraphQL 추가 지원        |
| Docker                                 | 1.28.0   | Docker 통합            |
| Korean Language Pack for VS Code       | 1.87.0   | 한국어 언어 팩             |
| Kubernetes                             | 1.3.13   | Kubernetes 도구        |
| Python Debugger                        | 2024.0.0 | Python 디버거           |
| Python                                 | 2024.2.1 | Python 지원            |
| Pylance                                | 2024.3.1 | Python 언어 서버         |
| PowerShell                             | 2024.2.0 | PowerShell 지원        |
| Debugger for Chrome                    | 4.13.0   | Chrome 디버거           |
| Jest                                   | 5.2.3    | Jest 통합              |
| Prisma                                 | 5.9.1    | Prisma ORM 지원        |
| Thunder Client                         | 2.17.1   | API 클라이언트            |
| YAML                                   | 1.14.0   | YAML 지원              |
| Next.js Snippets                       | 2.1.0    | Next.js 스니펫          |
| Tailwind Fold                          | 0.2.0    | Tailwind 클래스 접기      |
| Code Spell Checker                     | 3.0.1    | 맞춤법 검사               |
| vscode-styled-components               | 1.7.9    | Styled Components 지원 |
| Windows Terminal                       | 0.2.1    | Windows 터미널 통합       |
| Error Lens                             | 3.16.0   | 인라인 에러 표시            |
| Vue Language Features (Volar)          | 1.8.27   | Vue.js 지원            |
| TODO Highlight                         | 2.0.5    | TODO 하이라이트           |
| React code snippets                    | 2.9.0    | React 스니펫            |
| One Dark Pro                           | 3.16.0   | Material 테마          |

#### 2. **Setting.json**

```md
{
"prettier.singleQuote": true,
"prettier.trailingComma": "all",
"prettier.printWidth": 80,
"editor.formatOnType": true,
"editor.formatOnSave": true,
"editor.tabSize": 2,
"editor.wordWrap": "on",
"editor.fontFamily": "'Fira Code', 'Consolas', 'Courier New', monospace",
"editor.fontLigatures": true,
"editor.codeActionsOnSave": {
"source.fixAll.eslint": "explicit"
},
"tailwindCSS.emmetCompletions": true,
"editor.quickSuggestions": {
"strings": true
},
"eslint.format.enable": true,
"eslint.lintTask.enable": true,
"prisma.formatOnSave": true,
"docker.languageserver.diagnostics.enable": true,
"gitlens.showWelcomeOnInstall": false,
"git.autofetch": true,
"editor.minimap.enabled": false,
"workbench.colorTheme": "One Dark Pro",
"vs-kubernetes": {
"vscode-kubernetes.helm-path-windows": "C:\\Users\\<USERNAME>\\.vs-kubernetes\\tools\\helm\\windows-amd64\\helm.exe",
"vscode-kubernetes.kubectl-path-windows": "C:\\Users\\<USERNAME>\\.vs-kubernetes\\tools\\kubectl\\kubectl.exe",
"vscode-kubernetes.minikube-path-windows": "C:\\Users\\<USERNAME>\\.vs-kubernetes\\tools\\minikube\\windows-amd64\\minikube.exe"
},
"diffEditor.maxComputationTime": 0,
"terminal.integrated.defaultProfile.windows": "Command Prompt",
"terminal.integrated.profiles.windows": {
"PowerShell": {
"path": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
"args": [],
"icon": "terminal-powershell"
},
"Command Prompt": {
"path": "cmd.exe",
"args": [],
"icon": "terminal-cmd"
},
"Git Bash": {
"source": "Git Bash"
}
},
"roo-cline.allowedCommands": [
"npm test",
"npm install",
"tsc",
"git log",
"git diff",
"git show",
"python",
"pip",
"pip install",
"npm run",
"npm",
"pnpm install",
"cd",
"npx",
"Always approve execute operations",
"pnpm run",
"pnpm",
"pnpm add",
"pytest"
],
"aider-composer.pythonPath": "C:\\Python312\\python.exe",
"cursor.terminal.usePreviewBox": true,
"cursor.composer.cmdPFilePicker2": true,
"cursor.composer.collapsePaneInputBoxPills": true,
"cursor.composer.shouldShowMarkdownHoverParticipantActions2": true,
"terminal.explorerKind": "external",
"[javascript]": {
"editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[typescript]": {
"editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[json]": {
"editor.formatOnSave": true,
"editor.formatOnType": true,
"editor.defaultFormatter": "vscode.json-language-features"
},
"commentTranslate.source": "Google",
"commentTranslate.targetLanguage": "ko",
"commentTranslate.hover.enabled": true,
"deeplTranslate.apiFree": true,
"deeplTranslate.authKey": "<YOUR_DEEPL_AUTH_KEY>",
"typescript.inlayHints.parameterNames.enabled": "all"
}
```

#### 3. **cursor settings**

커서 세팅은 크게 2가지 정도 변경하면 된다. 

##### 1. User Rules

우선 가장 중요한건 User Rules이다. 커서의 강력한 기능 중 하나인 AI 어시스트 기능을 설정하는 부분이다.
설정은 프롬포트 형태로 작성하면 되며, 크게 건들 점이 없다면. 편의성을 위해 자신에게 친숙한 언어로 답변할 수 있도록 프롬포트를 작성하면 된다.

![[Pasted image 20250421162740.png]]

##### Models

모델 부분은 자신이 AI 채팅에 사용할 Model을 설정하면 된다. Cursor은 기본적으로 Claude를 사용하며, 개발자의 작업 방식과 스타일에 따라 알맞은 모델을 설정하면 된다.

![[Pasted image 20250421163541.png]]
#### 🗂️ 3. **폴더 구조 (기획 + 개발용)**

```md
📁 Vault/
└── 📁 file/
└── 📁 tags/
└── 📁 templates/ - 템플릿을 모아두는 폴도
├── 📁 개발/
├── 📁 디자인/
├── 📁 기획/
└── 📁 프로젝트/
└── 📁 연구노트/
```

옵시디언 폴더의 구조는 다음과 같이 구성하였다.

- 📁 **file**: 이미지, PDF 등 외부 파일들을 저장하는 폴더
- 📁 **tags**: 태그 관련 메타데이터와 태그별 문서 연결을 관리하는 폴더
- 📁 **templates**: 문서 작성 시 사용할 템플릿 파일들을 보관하는 폴더
- 📁 **개발**: 프로그래밍, 기술 스택 등 개발 관련 문서를 저장하는 폴더
- 📁 **디자인**: UI/UX, 그래픽 디자인 등 디자인 관련 문서를 보관하는 폴더
- 📁 **기획**: 프로젝트 기획, 아이디어 등 기획 관련 문서를 저장하는 폴더
- 📁 **프로젝트**: 실제 진행 중인 프로젝트별 문서를 관리하는 폴더
- 📁 **연구노트**: 학습 내용, 연구 기록 등을 정리하는 폴더

이 폴더는 필수적으로 설정해야 하는 것은 file, tags, templates이며 나머지는 자신이 작성할 문서 카테고리에 맞게 수정하면 된다.

### 템플릿 구조

새 글을 작성할 때마다 일관된 형식을 유지하기 위해 Obsidian의 템플릿 기능을 활용했습니다. 템플릿에는 글의 기본 골격과 함께 YAML 형태의 머리말(metadata)이 포함되어 있습니다. YAML 머리말에는 글 제목, 작성 날짜, 카테고리, 태그, 요약 등의 정보가 들어가며, 이는 블로그에서 글을 분류하고 표시하는 데 활용됩니다.

예시:

```md
<%*
const folder = tp.file.folder(true).split('/').pop();
const map = {
  "기획": "planning",
  "디자인": "design",
  "개발": "dev",
  "연구노트": "research",
  "프로젝트": "project",
};
tR += `---
publishDate: "${tp.date.now('YYYY-MM-DDTHH:mm:ss') + 'Z'}"
title: "${tp.file.title}"
excerpt: ""
image: https://images.unsplash.com/photo-1561069934-eee225952461?auto=format&fit=crop&w=2070&q=80
tags:
  - landing-pages
  - front-end
  - resources
category: "${map[folder] || 'etc'}"
metadata:
  canonical: https://your-blog.vercel.app/{{slug}}
---`
%>


# <% tp.file.title %>

## 개요

- 이 문서는 랜딩 페이지에 대한 종합적인 가이드입니다.
- 랜딩 페이지의 정의, 종류, 중요성, 실전 사례를 다룹니다.

## 본문 예시

> 여기에 내용을 자유롭게 작성해 주세요!  
> 필요하면 아래 요소를 참고해서 복붙해도 돼요!

- **특징 나열**
- **CTA 버튼 안내**
- **이미지 삽입**:  
  `![설명](https://링크)`
- **예시 링크**  
  `[예시 제목](landing/slug)`

## 마무리

랜딩 페이지는 단순한 마케팅 수단이 아닌, 강력한 전환 도구입니다.  
항상 A/B 테스트를 하고, 사용자의 흐름을 관찰하세요.

```

위 템플릿을 적용하면 기본적인 문서 구조가 즉시 잡히고, **메타데이터 자동화**를 통해 작성 시간도 단축됩니다. Obsidian의 Templater 플러그인 등을 이용하여 새 노트를 만들 때 현재 날짜가 `date` 필드에 자동 입력되도록 하고, 파일명을 제목으로 활용하여 `title` 필드를 채워 중복 입력을 줄였습니다. 덕분에 글을 쓸 때 매번 머리말 포맷을 일일이 작성하지 않아도 되고, 카테고리나 태그 같은 분류 정보도 빠뜨리지 않고 포함될 확률이 높아졌습니다.

### 실제 작업 흐름

문서 작성 **실제 작업 흐름**은 다음과 같습니다:

1. **Obsidian에서 템플릿으로 새 노트 생성**

   - 미리 만들어둔 템플릿으로 노트 생성
   - YAML 메타데이터 자동 입력

2. **Cursor로 얻은 초안 내용 붙여넣기**

   - AI가 생성한 초안 텍스트 복사
   - 노트에 붙여넣기

3. **Markdown 형식으로 내용 다듬기**

   - 마크다운 문법에 맞게 형식 수정
   - 문장 표현 매끄럽게 고치기

4. **다른 노트 참조 링크 추가**

   - 관련 노트에 대한 하이퍼링크 연결
   - 참조 정보 추가

5. **이미지 삽입 등 최종 마무리**
   - 필요한 이미지 삽입
   - 최종 검토 및 수정

## 3. AstroWind 기반 블로그 구조 및 GitHub/Vercel 배포

![[Pasted image 20250421171344.png]]

블로그를 구축하는 기술 스택으로는 **AstroWind** 템플릿을 사용했습니다. AstroWind는 Astro 5.0과 Tailwind CSS를 기반으로 한 무료 오픈소스 웹사이트 템플릿으로, 모던하고 최적화된 정적 사이트 구축을 쉽게 시작할 수 있게 해줍니다 ([GitHub - onwidget/astrowind: ⭕️ AstroWind: A free template using Astro 5 and Tailwind CSS. Astro starter theme.](https://github.com/onwidget/astrowind#:~:text=%2A%20%E2%9C%85%20Production,tags%20for%20social%20media%20sharing)).

이 템플릿을 사용하면 초기 디자인 작업 없이도 깔끔한 반응형 사이트를 얻을 수 있고, 블로그 운영에 필요한 여러 기능을 바로 활용할 수 있습니다. 예를 들어 AstroWind는 페이지 속도와 SEO 최적화에 신경 쓴 구성은 물론, **RSS 피드 자동 생성**, **다크 모드 지원**, **카테고리 및 태그 분류**, **소셜 공유 기능** 등 개발자 블로그에 유용한 요소들을 기본으로 포함하고 있습니다.

### AstroWind의 주요 기능

- 페이지 속도와 SEO 최적화
- RSS 피드 자동 생성
- 다크 모드 지원
- 카테고리 및 태그 분류
- 소셜 공유 기능

### AstroWind 세팅

![[Pasted image 20250421170755.png]]

Astro Wind를 ide로 불러 왔다면 디렉토리 구조가 다음과 같을 것이다.
이 중에서 우리가 주목 해야한 점은 src/data/post이다. 이 템플릿은 기본적으로 포스트를 다음과 같은 경로에 문서를 작성하는 것을 요구한다. 

하지만 다소 사소한 문제가 있는데 바로 /post 안에 있는 폴더 안에 있는 포스트를 인식을 할 수 없다는 점이다. 이를 해결하기 위해서는 다음과 같은 경로에 있는 파일을 수정해줘야 한다.


    ```
    src\content\config.ts
    ```
이 파일은 포스트 데이터를 어떻게 읽고 정의할지를 설정하는 파일이다.
해당 파일을 다음과 같이 수정한다.

```ts
import { z, defineCollection } from 'astro:content';

import { glob } from 'astro/loaders';

  

const metadataDefinition = () =>

  z

    .object({

      title: z.string().optional(),

      ignoreTitleTemplate: z.boolean().optional(),

  

      canonical: z.string().url().optional(),

  

      robots: z

        .object({

          index: z.boolean().optional(),

          follow: z.boolean().optional(),

        })

        .optional(),

  

      description: z.string().optional(),

  

      openGraph: z

        .object({

          url: z.string().optional(),

          siteName: z.string().optional(),

          images: z

            .array(

              z.object({

                url: z.string(),

                width: z.number().optional(),

                height: z.number().optional(),

              })

            )

            .optional(),

          locale: z.string().optional(),

          type: z.string().optional(),

        })

        .optional(),

  

      twitter: z

        .object({

          handle: z.string().optional(),

          site: z.string().optional(),

          cardType: z.string().optional(),

        })

        .optional(),

    })

    .optional();

  

const postCollection = defineCollection({

  loader: glob({

    pattern: ['**/*.md', '!templates/*.md', '!snippets/*.md', '!file/**/*'],

    base: 'src/data/post',

  }),

  schema: z.object({

    publishDate: z.preprocess((val: string | number | Date) => new Date(val), z.date()),

    updateDate: z.date().optional(),

    draft: z.boolean().optional(),

  

    title: z.string(),

    excerpt: z.string().optional(),

    image: z.string().optional(),

    category: z.string().optional(),

    tags: z.array(z.string()).optional(),

    author: z.string().optional(),

    metadata: metadataDefinition(),

  }),

});

  

export const collections = {

  post: postCollection,

};
```

이 중에서 astro wind  템플릿이 파일을 읽는 패턴을 정의하는 구간은 다음과 같다.
```ts
    pattern: ['**/*.md', '!templates/*.md', '!snippets/*.md', '!file/**/*'],
// '**/*.md' - 모든 md파일 읽기
//'!templates/*.md' - 펨플릿 폴더 내부 md 읽게 하지 않기
//'!snippets/*.md', - 스니펫 폴더 내부 md 읽게 하지 않기
//'!file/**/*'- 파일 폴더 파일 내부 md 읽게 하지 않기
    base: 'src/data/post',
```

위와 같이 포스트와 관련 없는 md 파읽을 필터링 하는 이유는 이 템플릿은 포스트의 서식이 조금이라도 잘못 된다면 재대로 실행이 되지 않기 때문에 그런 것이다.

이 이외도 랜딩 페이지나, 네비게이션 등 페이지를 상세하게 커스텀 가능하지만. 그 내용은 해당 문서와 관련이 없어 포함시키지 않았다.

### 배포 환경 구성

콘텐츠와 코드가 모두 들어있는 **AstroWind 프로젝트**는 GitHub에 저장소로 관리되고 있습니다. Git을 사용함으로써 모든 변경 사항이 버전 관리되고 백업될 뿐 아니라, 배포 프로세스와도 연계됩니다.

저는 이 저장소를 Vercel에 연결하여 **지속적 배포(CI/CD)** 환경을 구성했습니다. 그 결과, 저장소의 main 브랜치에 새로운 커밋이 푸시(push)될 때마다 Vercel이 이를 감지하고 자동으로 사이트를 빌드 및 배포합니다.

배포 과정은 완전 자동화되어 별도의 신경을 쓸 필요가 없습니다. 새로운 글을 작성하고 GitHub에 푸시하면 수십 초 내에 Vercel이 최신 버전으로 사이트를 업데이트해 줍니다. Vercel은 Astro로 구성된 정적 사이트를 빌드한 뒤 결과물을 자체 CDN에 배포하므로, 별도로 서버를 관리하거나 수동으로 빌드 명령을 내릴 필요가 없습니다.

또한 GitHub과 Vercel의 연동 설정은 한 번만 해두면 되기 때문에, 초기 설정 이후에는 **"글 작성 → 커밋 → 배포"** 사이클이 완전히 원클릭으로 이루어집니다. 이처럼 GitHub을 통한 버전 관리와 Vercel의 무중단 배포를 활용하여, 코드와 콘텐츠 수정 사항이 실시간으로 웹사이트에 반영되는 편리한 블로그 환경을 구축했습니다.

## 4. 통합 환경 구현 흐름: 프롬프트 입력부터 자동 배포까지

이제 앞서 설명한 도구들과 설정이 실제로 어떻게 하나의 워크플로우로 이어지는지, **아이디어 구상 단계부터 블로그에 게시되기까지**의 과정을 정리해보겠습니다:

### 1. AI 프롬프트로 초안 얻기

먼저 Cursor의 AI에게 작성하려는 내용에 대한 프롬프트를 입력합니다. 가령 "Obsidian과 Cursor를 활용한 개발 환경에 대해 소개하는 글의 아웃라인을 작성해줘"와 같은 요청을 하면, Cursor가 해당 주제에 대한 개요를 제시하고 본문 초안을 작성해줍니다. 작성자는 AI가 제시한 초안을 토대로 글의 뼈대를 빠르게 잡을 수 있습니다.

### 2. 초안 검토 및 수정

Cursor가 생성한 초안 내용을 검토하면서 부족한 부분을 수정하거나 내용을 보강합니다. 필요한 경우 Cursor에게 추가 프롬프트를 보내 특정 단락을 더 상세히 써달라고 하거나, 잘못된 부분을 바로잡습니다. 이 단계에서는 AI가 제공한 초안을 **필터링 및 편집**하여 최종 글감으로 발전시키게 됩니다. 이렇게 하면 백지 상태에서 직접 쓰는 것보다 훨씬 적은 시간에 글의 초안을 완성할 수 있습니다.

### 3. Obsidian 템플릿 적용 및 내용 정리

초안이 준비되면 Obsidian에서 블로그 포스트 템플릿으로 새 노트를 만듭니다. 자동으로 추가된 YAML 메타데이터를 확인하고, Cursor로부터 얻은 초안 텍스트를 복사해 이 노트에 붙여넣습니다. 그런 다음 Obsidian에서 마크다운 문법에 맞게 형식을 다듬고, 문장 표현을 매끄럽게 고칩니다. 이 단계에서 다른 노트에 대한 참조를 링크로 걸거나, 필요한 이미지를 삽입하는 등 **콘텐츠를 최종 마무리**합니다. 템플릿 덕분에 제목, 날짜, 태그 등의 메타정보도 이미 갖춰져 있어 내용만 채우면 됩니다.

### 4. GitHub에 커밋 및 푸시

글 내용 정리가 끝난 Markdown 파일을 Git 저장소에 커밋하고 원격 저장소(GitHub)의 메인 브랜치로 푸시합니다. Obsidian에서 바로 Git 커밋을 할 수도 있고, 터미널이나 데스크톱 Git 클라이언트를 사용해 커밋할 수 있습니다. 커밋 메시지를 작성한 뒤 푸시하면, GitHub 저장소에 새로운 글이 추가된 기록이 반영됩니다. 이 저장소에는 AstroWind 기반 블로그의 전체 소스가 포함되어 있기 때문에, 글 하나만 추가해도 프로젝트 전체를 다시 빌드해야 합니다.

### 5. Vercel 자동 빌드 및 배포

GitHub에 변경 사항이 푸시되면 Vercel이 연결된 프로젝트에 대해 자동 배포를 진행합니다. Vercel은 최신 커밋을 받아와서 Astro 사이트를 **빌드(정적 파일 생성)**하고, 완료된 정적 사이트를 배포합니다. 몇십 초 후에는 새로운 글이 포함된 업데이트된 블로그가 웹에 반영됩니다. 작성자는 브라우저를 열어 자신의 블로그를 새로고침함으로써 방금 작성한 글이 잘 보이는지 확인하면 됩니다.

이로써 *프롬프트 입력부터 배포까지*의 전 과정을 한자리에서 수행하게 되었으며, 별도의 수동 작업이나 복잡한 절차 없이도 아이디어가 실시간으로 웹에 공유될 수 있습니다.

## 5. 생산성과 아카이빙 효율 향상 효과

위와 같은 통합 환경을 구축하여 활용한 결과, 여러 측면에서 **개발 생산성**과 **지식 아카이빙 효율**이 향상되는 것을 체감했습니다:

### 작성 속도 대폭 향상

AI의 도움으로 글 초안을 마련하는 시간이 획기적으로 줄었습니다. 이전에는 새로운 주제로 글을 쓸 때 구상부터 완성까지 많은 시간이 들었지만, 이제는 Cursor가 기본적인 초안을 제시해주기 때문에 작성 시작 시간이 단축되고 글 전개에 집중할 수 있습니다.

### 일관된 문서 포맷 유지

템플릿을 사용함으로써 모든 글이 일정한 포맷과 구조를 갖추게 되었습니다. 매번 서식을 고민하거나 메타데이터 입력을 잊을 일이 없어졌고, 블로그 포스트 간의 일관성이 유지되어 나중에 보더라도 체계적인 아카이빙이 가능합니다.

### 맥락 전환 최소화

Obsidian에서 글 작성 → GitHub 커밋 → Vercel 배포까지 한 흐름으로 이어지다 보니, 도구 간의 **컨텍스트 전환**이 크게 줄었습니다. 한 가지 환경(Obsidian + Cursor)에서 모든 작업이 이루어지므로 집중력이 흐트러지지 않고, 작업 효율이 높아졌습니다.

### 지식 축적과 활용 증대

작성된 모든 글이 Obsidian 지식库에 축적되므로 별도의 아카이빙 노력을 들이지 않아도 자동으로 개인 지식 베이스가 확장됩니다. 또한 Obsidian 내에서 이전에 작성한 관련 글이나 노트를 하이퍼링크로 연결해둘 수 있어, 시간이 지나도 지식들이 고립되지 않고 서로 유기적으로 이어집니다.

### 신속한 배포와 피드백

자동 배포 환경 덕분에 글을 완성한 직후 바로 퍼블리싱할 수 있게 되었고, 이를 통해 외부 피드백을 더욱 빠르게 받을 수 있게 되었습니다. 아이디어를 빠르게 공유하고 검증할 수 있으므로, 개발 과정에서의 **피드백 사이클**도 단축되었습니다.

## 6. 마무리 및 사용 소감

지금까지 살펴본 Cursor와 Obsidian, AstroWind 기반 통합 개발 환경(IED)은 **개인 개발자의 작업 흐름을 혁신적으로 개선**해준 사례였습니다. AI 도구의 강력함과 개인 지식관리의 중요성이 결합되면서, 아이디어 구상부터 결과물 공유까지의 여정이 한층 부드러워졌습니다. 특히 번거롭게 느껴질 수 있는 문서 작성과 정리 작업이 자연스럽게 개발 프로세스의 일부가 되어, 결과적으로 프로젝트 진행 속도와 완성도를 높이는 데 기여했습니다.

직접 이러한 환경을 구축하고 몇 달간 활용해본 결과, 가장 크게 느낀 점은 **"문서화에 대한 심리적 부담이 줄었다"**는 것입니다. 과거에는 개발에 집중하느라 기록을 소홀히 하거나, 별도의 문서화 시간이 필요해 미루는 경우가 많았습니다. 그러나 이제는 Cursor가 초안을 도와주고 Obsidian이 정리를 책임져주니, 개발과 동시에 문서화가 병행되는 **자연스러운 흐름**이 만들어졌습니다. 덕분에 지식이 누락되거나 잊혀지는 일이 줄고, 축적된 정보가 고스란히 제 자산으로 남게 되었습니다.

물론 이러한 통합 환경을 설정하기까지 약간의 초기 러닝커브와 노력이 필요했습니다. 새로운 툴 조합에 익숙해지고, 템플릿과 자동화 스크립트를 조정하는 데 시간이 들기도 했습니다. 하지만 일단 환경이 갖춰지고 나니 그 이후의 효율 향상은 투자 대비 훨씬 컸습니다. 개발자마다 선호하는 도구나 작업 방식은 다르겠지만, 본 글의 사례가 자신의 워크플로우에 맞는 통합 환경을 고민하는 분들께 작은 인사이트가 되길 바랍니다.

빠르게 변화하는 개발 도구 생태계 속에서, **자신만의 통합 환경을 구축**함으로써 얻을 수 있는 생산성 향상과 만족도는 생각 이상으로 크다는 것을 직접 경험하였습니다. 앞으로도 이러한 도구들을 유기적으로 활용하여 더 스마트하고 즐거운 개발 문화를 만들어갈 수 있을 것으로 기대합니다.
