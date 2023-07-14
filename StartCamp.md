# STARTCAMP

startcamp 기간 동안 배운것들을 모두 정리해보기

----
1. 마크다운
2. CLI
3. Git
4. Github 


## 마크다운
-  파일명은 .md
-  프로젝트 개요나 실행방법을 소개할 때 씀
-  앞에 #을 붙여 제목을 만들수 있다.
   -  #의 갯수에 따라 크기가 달라짐
- **이나 _를 이용해서 글씨를 굵게, 기울이게 할 수 있다.
  - *이나 _를 한 개씩 양 옆에 붙여주면 *기울여서*
  - **이나 __를 두개 씩 양 옆에 붙여주면 **굵게**
  - ***이나 ___를 이용하면 ***굵고 기울여서***
- ~를 이용하여 취소선도 그릴 수 있다 ~~이런식으로~~
- '-'나 '+'등을 이용하여 순서가 없는 리스트를, '1.'을 이용하여 순서가 있는 리스트를 만들 수 있다.
- Code block :```를 이용하여 코드 블럭을 만들 수 있다.
  - 언어마다 설정 가능
 ```python
 #python
   a = int(input())
   print(a)
 ```
 ```C
 //C언어
 #include<stdio.f>
 int main(){
    printf("Hello")
 }
 ```

- 링크와 이미지도 넣을 수 있다.
  - 링크는 [ ]안에 제목 + ( )안에 url를 타이핑하여 [네이버](https://www.naver.com) 과 같이 출력할 수 있다.
  - 이미지는 링크와 똑같지만 맨 앞에 !를 붙여서 가능


## CLI
CLI은 GUI와 반대되는 개념으로 그래픽이 아닌 명령어를 통해 사용자와 컴퓨터가 상호작용하는 방식을 의미한다.

- 점(dot,.)의 역할
  - 점 한개(.) : 현재 디렉토리
  - 점 두개(..) : 상위 디렉토리
  - ex) cd .. = 상위 디렉토리로 갑시다
- 여러가지 문법들
  - **touch** a.txt : a.txt라는 파일을 생성
  - **mkdir** newfolder : newfolder이라는 폴더(디렉토리)를 생성
  - **ls** : 현재 있는 디렉토리의 파일/폴더 내역을 출력
  - **cd** : 위치 이동
  - **start** a.txt : a.txt 파일 열기
  - **rm** -r newfolder : newfolder 폴더 삭제
- 경로
  1. 절대경로 : C://부터 목적지까지 모든 경로를 다 작성한 것
  2. 상대경로 : 작업하고 있는 디렉토리를 기준으로 그때부터의 경로만을 작성한 것


## Git

####  Git이란?
- Git = 분산 버전관리 시스템 (중간중간 수정한 것들도 모두 저장이 됨)
- 지금까지 온 과정을 파악할 수 있고, 이전 버전과 비교도 가능함
- 코드의 '변경 이력' 기록 + '협업'


#### Git의 영역

1. Working Directory : 실제 작업 중인 파일들이 위치하는 영역
2. Staging Area : Working Directory에서 변경된 파일 중, 다음 버전에 포함시킬 파일들을 선택적으로 추가, 제외할 수 있는 중간 준비 영역
3. Repository : 버전(commit) 이력과 파일들이 영구적으로 저장되는 영역, 모든 버전과 변경 이력이 기록됨.

- commit(버전): 변경된 파일들을 저장하는 행위
- Working Directory --**(add)**-> Staging Area--**(commit)**-> Reposity


#### Git 문법
- ***git init*** : 로컬 저장소 설정(초기화), 시작할 때
- ***git add*** : 변경사항이 있는 파일을 staging area에 추가
- ***git commit*** : staging area에 있는 파일들을 저장소로 보냄(commit을 생성하고 변경이력을 남김)
- ***git config --global (내 주소)***
- ***git config -- global (내이름)*** : commit 작성자 설정(한번만 해줘도 됨)
- ***git log*** : commit 했던 것들 확인가능
  

## GitHub
   
#### GitHub란? 
- GitHub = 원격저장소
- 코드와 버전 관리 이력을 온라인 상의 특정위치에 저장하여 여러 개발자가 협업하고 공유할 수 있는 저장공간
- 위에서 만든 commit를 올릴 수 있다

#### GitHub 이용하기(push)
1. [GitHub](https://github.com/) 가입하기
2. 새로운 repository 만들기
   - start a new repository
   - 이름 입력
   - public 설정
   - create a new repository
3. 만들어진 repository 주소 복사 해놓기
4. ***git remote add 별명 주소*** : 로컬 저장소에 원격 저장소 추가
5. ***git remote -v*** : 추가되었는지 확인
6. 추가하려고 하는 파일을 git을 이용해 우선 commit까지 완료함
7. ***git **push** -u 별명 master*** : 원격저장소에 commit 목록을 업로드
8. 원격 저장소에 잘 되었나 확인하기!
9.  현재 로컬 저장소에서 원격 저장소를 삭제하고 싶다면 ***git remote rm 별명***


#### GitHub에서 파일 가져오기(pull, clone)
1. ***git **pull** 별명 master*** : 원격저장소의 변경사항을 가져옴(업데이트)
2. ***git **clone** 주소*** : 원격 저장소 전체를 복제해서 다운로드 받아옴
- 아무것도 없는 상태에서 **처음**받는거면 clone, 이후에 변경사항이 생겨서 **업데이트**가 필요하면 pull

#### gitignore
- 공유하지 않을 파일을 추적하지 못하도록 설정하는데 사용하는 파일
- a.txt를 공유하고 싶지 않을 경우,
  - ***echo a.txt >> .gitignore***
  - 이미 git의 관리를 받으면 적용 X