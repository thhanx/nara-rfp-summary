# nara-rfp-summary

한국 공공기관의 나라장터 제안요청서(RFP), 과업지시서, 입찰공고를 분석하는 Codex 스킬입니다. 원문 전체를 구조화해 요약하고, 입찰 검토에 필요한 핵심정보를 고정된 6개 필드로 제공합니다.

## 주요 기능

- 사업명, 발주기관, 사업기간, 사업예산, 목적, 핵심 서비스 추출
- 사업 개요와 일정, 참가자격, 요구사항, 평가배점 정리
- 제출서류, 계약조건, 보안조건 및 실무 리스크 분석
- 문서에 없는 정보는 추정하지 않고 `문서에 명시되지 않음`으로 표시
- 예산, 일정, 배점 등 주요 정보에 원문 페이지 근거 표시
- 기존 RFP 요약 Markdown에서 6개 핵심정보만 다시 추출

## 지원 입력

- PDF 제안요청서, 과업지시서 및 입찰공고
- DOCX 등 텍스트를 읽을 수 있는 문서
- 기존에 작성된 RFP 요약 Markdown

HWP 원본은 PDF로 변환한 후 사용하는 것을 권장합니다.

## 설치

Git Bash에서 Codex 개인 스킬 폴더에 저장소를 복제합니다.

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/thhanx/nara-rfp-summary.git ~/.codex/skills/nara-rfp-summary
```

설치 후 Codex에서 새 작업을 열거나 앱을 다시 시작합니다.

## 사용법

RFP 원문을 첨부하고 다음과 같이 호출합니다.

```text
$nara-rfp-summary를 사용해 첨부한 제안요청서를 분석해 주세요.
```

기존 요약 Markdown에서 핵심정보만 추출할 수도 있습니다.

```text
$nara-rfp-summary를 사용해 이 Markdown에서 핵심정보를 추출해 주세요.
```

## 핵심정보 출력 형식

```text
사업명: {값}
발주기관: {값}
사업기간: {값}
사업예산: {값}
목적: {값}
핵심 서비스: {값}
```

원문 RFP를 분석할 때는 위 핵심정보와 함께 다음 항목을 포함한 상세 Markdown 보고서를 생성합니다.

1. 사업 개요
2. 주요 일정
3. 참가자격 및 제한
4. 과업 범위 및 요구사항
5. 평가 방식 및 배점
6. 제출서류 및 제안서 규격
7. 사업관리·품질·보안
8. 계약조건
9. 리스크 및 주의사항
10. 추가 확인이 필요한 사항

## 저장소 구조

```text
nara-rfp-summary/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   └── report-template.md
├── README.md
└── LICENSE
```

## 주의사항

- 본 스킬의 결과는 문서 검토를 돕기 위한 참고자료이며 법률·계약 자문이 아닙니다.
- 실제 입찰 참여 전 원문과 나라장터 공고 내용을 반드시 다시 확인하세요.
- 비밀번호, API 키, 개인정보 등 민감한 자료를 공개 저장소에 커밋하지 마세요.

## License

This project is licensed under the [MIT License](LICENSE).
