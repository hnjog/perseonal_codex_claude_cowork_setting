# perseonal_codex_claude_cowork_setting

Codex와 Claude Code의 공통 작업 규칙과 수동 교대 절차를 관리하는 저장소

- 기준 폴더: Contexts / AGENTS.md를 이동·복제하지 않고 단일 원본으로 관리
- 프로젝트 소스 폴더 내부에 문서·컨텍스트·에이전트 지침 파일 생성 금지
- Git 관리: 공통 지침·교대 절차·PR 형식·설치 안내·빈 양식
- 로컬 전용: 프로젝트 설정·Git 및 코딩 컨벤션·실제 작업 인계·분석·계획·리뷰·백업

## 문서

- [공통 지침](AGENTS.md)
- [교대 절차](docs/AI_WORK_HANDOFF.md)
- [PR 작성 형식](docs/PR_FORMAT.md)
- [설치와 폴더 구성](docs/SETUP.md)
- [빈 인계 양식](templates/HANDOFF_TEMPLATE.md)

## 구성

```text
Contexts/
  .git/                         이 저장소의 Git 메타데이터
  .gitignore                    기본 제외 + 공통 파일 허용 목록
  AGENTS.md                     공통 규칙 원본
  CLAUDE.md                     Contexts에서 시작한 Claude의 진입점
  README.md
  templates/                    빈 양식과 전역 진입점 예시
  docs/
    AI_WORK_HANDOFF.md           공통 교대 절차
    PR_FORMAT.md                공통 PR 형식
    SETUP.md                    설치 안내
    tasks/                      실제 작업 문서 / Git 제외
    projects/                   프로젝트별 설정과 분석 / Git 제외
    reviews/                    검토 기록 / Git 제외
    local/                      백업과 로컬 이력 / Git 제외
```

## 다른 PC에서 사용

1. 프로젝트 소스 폴더 밖의 원하는 Contexts 경로에 이 저장소 clone
2. 프로젝트 설정 양식을 참고해 docs/projects에 로컬 프로젝트 설정 작성
3. 프로젝트별 Git·코딩 컨벤션을 로컬에 준비하고 설정 문서에 경로 등록
4. 필요 시 사용자 홈의 Codex·Claude 전역 진입점 설치 / 예시의 경로를 실제 절대 경로로 변경
5. 새 세션에서 실제 읽은 지침 경로와 승인 절차 확인

.gitignore는 이미 추적된 파일에는 적용되지 않으므로 기존 추적 여부도 확인
공개 파일에서 로컬 파일을 참조할 수 있지만 해당 로컬 설정은 clone에 포함되지 않음
실제 프로젝트 설정 없이 예시 값만으로 코드 작업을 시작하지 않기
