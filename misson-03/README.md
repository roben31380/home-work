# Netflix promotion page

![view](/https://github.com/roben31380/home-work/blob/main/misson-03/images/readme/view.png)

## 작업순서

1. variable, font, reset
   - 시안을 참고하여 theme.css, base.css, reset.css 로 작업
2. components (buttons, forms)
   - button
     1. normal, arrow, 언어선택 으로 나누어 작업
     2. :hover, :focus, :disabled 으로 state 구성
     3. mobile: size, border-radius 변경
   - form
     1. 이메일(일반), 비밀번호 로 나누어 작업
     2. .is--focus, .is--invalid 로 state 구성
     3. mobile: size, border-radius 변경
3. header, footer
   - header
     1. logo, button-group으로 작업
     2. mobile : logo size, button size, 여백 size 조절
   - footer
     1. footer-group 1~5 로 작업
     2. footer-group : flex, link-group : grid 로 작업
     3. mobile : 여백 사이즈 조절, link-group grid column 조절
4. template
5. page - main
6. mobile view

### buttons

![buttons](//https://github.com/roben31380/home-work/blob/main/misson-03/images/readme/button.png)

#### states

```css
&:hover {
  background-color: var(--red-600, #b70710);
  border: 1px solid #000;
}

&:focus {
  background-color: var(--red-500, #e50914);
  border: 1px solid var(--green-400, #58e590);
  outline: 2px solid var(--green-400, #58e590);
}

&:disabled {
  background-color: var(--gray-500, #757575);
}
```

### forms

#### states

```css
.is--focus {
  & .form-label {
    color: var(--red--500, #e50914);
    top: 10%;
    font-size: 0.75rem;
  }

  & .form-input::placeholder {
    visibility: visible;
  }
}

.is--invalid {
  & .form-label {
    color: var(--red--500, #e50914);
    top: 10%;
    font-size: 0.75rem;
  }
  & .form-input {
    border-bottom: 3px solid var(--red--500, #e50914);
  }

  & .form-message,
  .password-message {
    display: block;
  }
}
```

## 회고

1. button은 가상클래스로, form은 클래스로 상태를 구분했는데 한가지 방법으로 통일시켜 작업해야 이후 유지보수나 스크립트를 활용할때 용이하겠다.
2. 반응형 unit을 사용했을때 예상한 레이아웃이 나오지 않아 수정에 많은 시간이 걸림. 많이 만들어보면서 감 익히기.
3. mobile view 작업을 페이지까지 완성하고 했는데, 예상과 다르게 나오는 부분이 많다.
   각각의 components 를 작업할때 mobile까지 작업을 하고 조립하는게 좋겠다.
