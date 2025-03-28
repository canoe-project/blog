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
