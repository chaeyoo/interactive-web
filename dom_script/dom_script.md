#### DOM (Document Object Model)

- structured representation
- 프로그래밍 언어가 DOM 구조에 접근할 수 있는 방법을 제공, 그들이 문서, 구조, 스타일, 내용 등을 변경할 수 있게 함
- 문서(document) 와 문서의 요소(element) 에 접근하기 위해 DOM과 JavaScript 사용

#### 사용예제

```
const ilbuni = document.querySelector('.a');

document.querySelector('.ilbuni') // 맨앞의 한 개만 가져옴

document.querySelectorAll('.ilbuni')


document.querySelector('.ilbuni:nth-child(2)')
```

#### data- 로 시작하는 표준 커스텀 속성

- data-index, data-id, data-role 등 data-의 형식으로 시작하면 어떤 속성이든 필요에 따라 임의로 추가 가능

```
characters.setAttribute('data-id', 123)
```

- dataset 객체로도 확인 가능

```
characters.dataset // DOMStringMap {id: '123'}
```

#### 동적으로 child 추가

```
const pElm = document.createElement('p');
pElm.innerHTML = '<a href="#">안녕</a>';
const characters = document.querySelector('.characters');
characters.appendChild(pElm);
```

#### 동적으로 child 삭제

```
const chars = document.querySelector('.characters');
chars.removeChild(document.querySelector('.b'));
```

#### 클래스명 추가하기

```
const ilbuni = document.querySelector('.a');
ilbuni.classList.add('special');
```

#### 클래스명 삭제하기

```
const ilbuni = document.querySelector('.a');
ilbuni.classList.remove('ilbuni');
```

#### 클래스명 토글하기

```
const ilbuni = document.querySelector('.a');
ilbuni.classList.toggle('ilbuni')
```
