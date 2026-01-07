
# 문서 이미지 뷰어 구현

## ✏️ 과제의 개요

| 카테고리 | 난이도 | 제한시간 |
|----------|--------|----------|
| frontend | hard | 7d |

### 💻 과제에서 요구하는 개발언어

- typescript
- react


## 📜 과제의 내용

> 과제 설명과 요구사항을 참고하여, 구현해 주세요.

### 👀 과제의 설명

# 문서 이미지 뷰어 구현

​

Chrome PDF 뷰어와 비슷한 문서 이미지 뷰어를 구현해보는 과제 입니다.

​

### 기능 요구 사항

\*전반적인 UX경험을 Chrome에서 PDF문서를 보는 경험과 비슷하게 구현해 주시면 됩니다.

<!-- <video isUpload="true" name="null" src="https://commitnow-bucket.s3.ap-northeast-2.amazonaws.com/temp/ef81eb14-a069-4312-90fd-187eb7835e30/assignment/2f7e43e1-2c71-4ca4-afa4-65dba2d65e4d-1767763961920.mov" /> -->
[Download the video](https://commitnow-bucket.s3.ap-northeast-2.amazonaws.com/temp/ef81eb14-a069-4312-90fd-187eb7835e30/assignment/2f7e43e1-2c71-4ca4-afa4-65dba2d65e4d-1767763961920.mov)

​

### 구현 요구 사항

* 아이콘 사용이 필요한 경우, Lucide Icon([https://lucide.dev/icons/](https://lucide.dev/icons/)) 패키지를 활용합니다.
* 폰트는 `Pretendard` 를 사용합니다.
* 문서 이미지 뷰어 스펙

  * 이미지 뷰어 컴포넌트

    * 이미지를 렌더링 하는 부분입니다.
    * 이미지는 브라우저 화면의 수평 정중앙에 정렬되어 보여집니다.
    * 이미지의 width는 768px로 고정입니다.
    * [총 10개의 이미지](https://drive.google.com/file/d/1LEFVKcy9eW7C-699HXC05_YvAwQJl6IY/view?usp=sharing)를 위에서부터 아래 방향으로 순차적으로 렌더링하여 보여주세요. `1.png`파일이 가장 위에 렌더링 되고, `10.png`파일이 가장 아래에 렌더링 됩니다.
    * \[❗직접 구현 필수] **이미지에 마우스 hover가 되었을 때, 커서를 중심으로 하는 가로/세로 300px 크기의 정사각형 돋보기 영역을 보여 주고 해당 돋보기 내부에서는 원본 이미지가 1.5배 scale up 되어 보입니다. 커서를 움직였을 때 해당 돋보기 box 영역도 커서를 따라서 같이 움직입니다. 커서가 이미지 밖으로 벗어나면 돋보기 영역은 사라집니다.**
  * 이미지 뷰어 컨트롤러 컴포넌트

    * 이미지 뷰어를 조작 하는 부분입니다.
    * 화면 최상단에 위치하며, 브라우저 스크롤과 상관없이 해당 위치에 그대로 머뭅니다.
    * 컨트롤러의 맨 왼쪽에는 “Document Image Viewer”라는 텍스트를 배치합니다.
    * 컨트롤러의 중앙에는 이미지 뷰어를 조작할 수 있는 Toolbar를 배치합니다.

      * Toolbar 에는 다음과 같은 기능이 포함되어 있습니다.

        * **\[현재 보고 있는 페이지 번호 / 총 페이지 수]를 표시하는 부분** → 현재 보고 있는 페이지 번호 부분은 사용자가 직접 입력이 가능한 input 필드입니다. 해당 input 필드에 원하는 페이지 번호를 입력하면 이미지 뷰어에서 해당 페이지를 보여주어야 합니다.
        * **이미지 뷰어의 zoom level을 조절할 수 있는 부분** → ‘-’ 아이콘 버튼을 클릭하면 이미지 뷰어가 축소되어 보여지고, ‘+' 아이콘 버튼을 클릭하면 이미지 뷰어가 확대되어 보여집니다. 이 때, 버튼을 통해 조절되는 zoom level의 단위는 25%입니다. Minimum zoom level은 25%이고, Maximum zoom level은 400%입니다.
          사용자는 현재 zoom level을 표시하는 부분에 직접 원하는 값을 입력할 수 있고, 그에 따라 이미지 뷰어에서는 해당 zoom level로 문서를 축소/확장하여 보여줍니다.


### 🎯 과제의 요구사항

- React 사용. 돋보기 기능을 제공하는 라이브러리(react-image-magnify) 사용 불가
- TypeScript 사용
