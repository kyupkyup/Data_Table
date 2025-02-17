# table

테이블은 대규모의 데이터를 잘 정리해서 보여줄 수 있는 데이터 형식이다. 하지만 접근성이 떨어지는 사람들에게나, 기계는 해당 테이블을 사람이 읽는 만큼 잘 해석할 수 없다.

이를 위해 table을 마크업할 때 접근성을 잘 고려해서 작성해야 될 필요성이 있다.

## caption

caption은 테이블의 제목과 간단한 요약을 전달한다.

caption 은 테이블의 정보를 접근성이 떨어지는 독자가 접했을 때, 해당 테이블의 정보가 필요할 지 안 필요할지 판단하는 데 도움을 준다. caption이 없다면 독자는 테이블의 모든 정보를 들으면서 해당 테이블이 어떤 내용인지 판단할 수 있을 것이다.

이를 미리 파악할 수 있게 전체적인 정보를 주는 것이 caption의 목적이다.

table 요소의 첫 번째 자식으로만 올 수 있다.

## thead

헤더 영역을 지정해주는 태그

## th

수많은 행 중의 헤더로 작동한다. 전체적인 행들의 공통점을 묶어주는 요소이므로 반드시 th 로 선언해주어야 하며, 이렇게 하지 않고 td로 선언할 시 접근성이 매우 떨어지게 된다.

아래의 속성은 th 내부에 사용할 수 있는 속성 중 표준이 아닌 내용은 모두 제외했다.

### abbr

해당 셀에 대한 간단한 설명을 넣을 수 있는 속성이다.

### scope

해당 th 요소와 관련된 모든 셀들을 묶어줄 수 있는 속성이다.

>

- row: 헤더는 자신이 속한 행의 모든 셀과 관련됩니다.
- col: 헤더는 자신이 속한 열의 모든 셀과 관련됩니다.
- rowgroup: 헤더는 행 그룹에 속하며 모든 셀과 관련됩니다. 이러한 셀은 요소 의 dir속성 값에 따라 헤더의 오른쪽 또는 왼쪽에 배치 될 수 있습니다.
- colgroup: 헤더는 colgroup에 속하며 모든 셀과 관련됩니다.
  https://developer.mozilla.org/ko/docs/Web/HTML/Element/th

#### row

row는 해당 헤더가 자신이 속한 **행**의 모든 셀과 관련이 된다. 일반적으로 td 앞의 th에 사용해서 가로행의 헤더로 사용할 때 사용한다.

#### col

col 은 해당 헤더가 자신이 속한 **열**의 모든 셀과 관련이 된다. 열의 th에 적용시킨다.

#### colgroup

colgroup은 caption 직후에만 사용할 수 있다. colgroup은 헤더가 그룹화되어 있을 시 span 속성을 통해 몇개의 헤더가 그룹화 되어 있는지, 명시해주는 기능을 한다.

### rowspan

셀이 확장되는 행 수를 정의한다. 즉 행 병합이라고 보면 된다.

### colspan

셀이 확장되는 열 수를 정의한다. 즉 열 병합이라고 보면 된다.

### headers

td에서 설명 예정

## tr

일반적으로 하나 하나의 행을 정의하는 데 쓰인다.

## td

tr 태그 안에서 하나 하나의 셀을 나타내는 데 쓰인다.

### rowgroup

rowgroup 은 행이 병합되는 경우 해당 row에 속하는 row가 어떻게 구성되는지 명시하는 역할을 한다.

### headers

headers에는 해당 셀에 해당하는 id 값의 집합이 문자열로 들어가게 된다. 이를 통해, 명확하게 해당 셀이 어떤 영역의 id 속성을 포함하고 있는지 명시할 수 있다.

### 내용 없는 셀 표현

Table 내의 내용 없는 셀(td) 표현.

값이 없는 경우에는 빈 셀로 남기지 말고 없음이라고 표기 후, CSS 를 통해 텍스트를 제공하면 정보 접근성을 높히면서 디자인의 문제 없이 서비스를 할 수 있다.

## 결론

이 과제를 하면서 스크린리더를 다운받아서 만들어진 표를 모두 들어봤다. 내가 받은 스크린리더가 잘 못 된건지 내가 접근성 설정을 잘 못한건지는 모르겠지만, 접근성 설정을 한 표와 하지 않은 표의 실질적인 차이는 없었다. 하지만 이 스크린리더로 듣는게 얼마나 불편한건지 접근성이 떨어지는게 얼마나 불편한지 명확하게 알게 되었다. 내가 조금 더 고생해서 불편한 사람 한 명이라도 더 편하게 웹 사이트를 이용할 수 있게 된다면 의미 있는 일일 것이다.
