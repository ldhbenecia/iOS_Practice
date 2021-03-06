# I learned this from this project
#### 2021.12.21 ~ 2021.12.29

* 네이버 부스트코스 iOS 프로그래밍 강의 중 두 번째 프로젝트이다.  
일단 시작부터 엄청나게 난감했고, 기능 구현 중 서칭을 하기도 애매한 텍스트뷰 델리게이트 구간을  
지인에게 물어서 해결하였다.

* 전체적으로 처음부터 직접 코드를 작성해본 프로젝트라 정말 갈 길이 먼 것을 깨달았다.  
또한 이 앞 musicPlayer에서 깨달은 점은 진짜 아무것도 아니고 지금 이 프로젝트 또한 그럴 것이다.    
* 2021.12.26자로 기능구현이 전부 끝났다.  
    - 오토레이아웃만 잡으면 이번 프로젝트는 끝날 예정
    - 좀 쉬다가 12.29일자 오토레이아웃 구현 끝
---
## 어플 설명
* I. 첫 번째 메인 화면 (메인)
    - sign up 버튼을 누를 시 다음 화면으로 전환된다.  
    - 여기서 전환 방식은 모달이다.
    - NavigationController를 사용할 수 있게 되었다.
* II. 두 번째 화면 (회원가입)
    - 상단 왼쪽 이미지뷰를 클릭하면 UIImagePickerController가 떠서 이미지 크기를 수정 후에 프로필 사진으로 선택이 가능하다.  
    - 이미지 수정 같은 경우는 ImagePicker에  
    picker.allowsEditing = true를 강의 외에 별도로 학습하여 추가해주었다.  
    - 화면 중간의 텍스트뷰에 자기 소개를 입력할 수 있다.  
    - 화면 왼쪽 하단의 취소 버튼을 누르면 첫 화면으로 돌아간다.  
    - 처음 두 번째 화면에서는 다음 버튼을 누를 수가 없다. 다음 버튼은 처음 비활성화 되어 있으며, 프로필 사진, 아이디, 자기소개가 모두 채워진 이후, password와 checkpassword에 입력된 값이 같을 경우 다음 버튼이 파란색으로 바뀌면서 활성화가 되어 그때 다음 화면으로 갈 수 있다.  
    - 이 다음 버튼 구현하는데 진짜 애를 너무 많이 먹었다.
    - textField는 IBAction으로 쉽게 해결할 수 있었는데 textView같은 경우는 sentEvent가 사용 불가해서 델리게이트를 구현해서 풀어내야했는데  
        이 과정에서 지인이 없었으면 진짜 때려칠 뻔 했다. 너무 고마웠다,,
* III. 세 번째 화면 (회원가입 부가정보 설정)
    - 전화번호 입력란과 생년월일 날짜 위젯을 입력해야한다.
    - 전화번호 텍스트필드를 누르면 숫자키패드가 올라온다. (story board에서 설정)
    - 이 전 화면과 같이 가입 버튼은 처음 비활성화가 되어있고 전화번호와 생년월일 날짜를 입력해야한다.
    - 여기서 프로젝트 예시안의 datePicker 모양이 달라서 구글링을 해보았는데 iOS14 패치 이후부터 datePicker의 Preferrend Style이 Automatic으로 되어있는데 이것을 wheels로 바꾸어서 예시안과 같이 보기 좋게 설정하였다.
    - 전화번호, 생년월일을 입력하고 활성화 된 가입 버튼을 누르면 첫 번째 메인 화면으로 넘어가며 넘어갔을 때 첫번째 메인 화면에는 자동으로 id textField에 가입한 아이디 정보가 입력되어있다.
* IV. Singleton 사용
    - 강의에서 배운대로 UserInformation이라는 Swift file추가로 싱글턴을 사용하였다.
    - id, password, introduce, phonenumber, dateofbirth로 변수명을 지어서 사용하였다.
* V. info.plist
    - 프로필 사진 설정을 위해 사용자 휴대폰의 사진을 사용하기 위해 info.plist에 사진 추가 요청을 하였다.
