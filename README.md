# Git Session

# 사전 과제

- github 계정을 만들고 공유해주세요.
- github desktop app을 설치해주세요.

# Git

버전 관리 시스템.

프로젝트를 하면서 여러분의 작업 히스토리를 남기고 싶을 때, 여러 사람들과 동시에 작업해도 서로의 작업이 꼬이지 않게 관리하고 싶을 때 git을 사용해요.

아래 git의 핵심 구성 요소들을 살피며 알아봐요.

# Commit

일정 작업을 한 이후 언제든지 현재 상태로 돌아오고 싶을 때(체크포인트를 만들고 싶을 때) commit을 남겨요.

### 사실 다른 작업을 할 때도 Git 같은 게 필요해요.

- 문서 작업 : 실행 취소(Ctrl + Z), 실행 취소 취소(Shift + Ctrl + Z)로 작업 히스토리를 넘나들 수 있음
- 디자인 작업 : 최종, 최종최종, 최종최종최종 파일을 만들어서 작업 히스토리를 넘나들 수 있음

얼마나 비효율적이었나요. 코딩 작업은 git이 효율적으로 작업 히스토리를 관리해 줄 뿐이에요. 겁 먹지 마세요.

## Commit History

commit을 여러 개 만들다 보면 자연스럽게 commit들의 목록이 생기겠죠? 이게 commit history예요.

# Branch

그런데 여러 사람들이 한 곳에 commit을 쌓으면 서로의 작업 순서가 뒤죽박죽 되겠죠?

그래서 그러면 안돼요.

여러분은 각자의 branch를 만들 거예요.

일단은 다른 사람들의 작업에 영향을 받지 않고 자신만의 commit history를 만들 수 있는 공간이라고 이해해주시면 돼요.

### main branch

우리의 작업들이 합쳐지는 branch예요.

### feature_* branch

여러분의 개인 작업이 진행되는 branch예요.

*에는 본인의 닉네임을 작성하는 걸 권해드리지만, 작업의 내용을 식별할 수 있는 다른 키워드도 좋아요.

# Pull Request

결국 여러분의 작업이 끝나면 각자의 branch에 있는 그 코드를 우리 모두의 branch인 main에 합쳐야겠죠?

맡은 작업을 끝내기 위해 쌓인 commit history는 개인의 성향에 따라 짧거나 길수도 있겠지만, main에 합칠 때는 이 작업을 하나의 단위로 보내주셔야 해요. (그래야 서로 보기 편하니까요.)

그때 github에서 pull request를 사용해주시면 돼요.

# 프로세스 정리

### 우리의 Repository Clone 하기

[Github Desktop]
- Clone Repository 클릭
- 우리의 레파지토리 이름 입력

### 본인의 Branch 만들기

[Github Desktop]
- Current branch > New Branch 클릭
- feature_* 입력

### 본인의 작업 Commit 하기

[Xcode]
- 열심히 코드를 짠다.

[Github Desktop]
- Changes(이전 커밋과 비교했을 때 변경된 코드들)에서 본인이 한 작업을 다시 한 번 체크하고, 제목과 함께 커밋을 남긴다.
- 하고싶을 때 마다 반복한다.

### 본인의 작업 Pull Request 올리기

[Github Desktop]
- 작업 완료 후 (Publish branch 클릭) -> Push origin 클릭

[Github]
- 인터넷 브라우저에서 우리 레파지토리 링크 접속
- New pull request 클릭
- base: main <- compare: feature_*(본인의 브랜치) 확인
- 작업에 대한 제목, 설명(optional) 작성 후 Create pull request 클릭
- 테크팀의 코드 리뷰를 기다린다.

### 본인 맥북에 최신 상태 코드 불러오기

[Github Desktop]
- Current branch > “main” 클릭
- Fetch origin 클릭 : “main” branch의 최신 상태를 불러오기
