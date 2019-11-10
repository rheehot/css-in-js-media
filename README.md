# css-in-js-media :art:

**Minified and Simplified include-media with CSS-in-JS**

when you style with css-in-js (emotion, styled-component) you can perfectly and easily deal with responsive design with this `css-in-js-media` which is similar with [include-media](https://include-media.com/)

### :question: how-to-use

```
npm install css-in-js-media
import media from "css-in-js-media";
```

- example in `code-sandbox-link` : https://codesandbox.io/embed/k28q2nv2w7

### :school_satchel: size

![image](https://user-images.githubusercontent.com/26598542/57980351-92853600-7a65-11e9-8ce0-5e0f5acead4f.png)

### :pencil: example

#### media-query break-point

```
smallPhone: 320
phone: 375
tablet: 768
desktop: 1024
largeDesktop: 1440

```

with css-in-js library (ex: emotion.js , styled-component)

- example with `emotion.js`

```javascript
import media from "css-in-js-media";

export const exampleClass = css`
  color: red;
  ${media(">desktop")} {
    font-size: 15px;
  }
  ${media("<=desktop", ">tablet")} {
    font-size: 20px;
  }
  ${media("<=tablet", ">phone")} {
    font-size: 25px;
  }
  ${media("<=phone")} {
    font-size: 30px;
  }
`;
```

- example with `styled-component`

```javascript
import media from "css-in-js-media";

const exampleClass = styled.h1`
  color: red;
  ${media(">desktop")} {
    font-size: 15px;
  }
  ${media("<=desktop", ">tablet")} {
    font-size: 20px;
  }
  ${media("<=tablet", ">phone")} {
    font-size: 25px;
  }
  ${media("<=phone")} {
    font-size: 30px;
  }
`;
```

### :heart: THANKS

- https://github.com/koansang
- https://github.com/yongdamsh

### :bug: Bug reporting

[Issue](https://github.com/zx6658/css-in-js-media/issues)

### License

[MIT](./LICENSE)


##  comment

리액트 개발을 하면서 styled-components나 emotion.js같은 css-in-js 기법을 활용해 반응형 대응을 할때 불편한 적이 많았는데요, scss를 활용할때는 include-media 같은 라이브러리를 통해 직관적으로 반응형대응을 할 수 있었던 점에서 착안해 이를 css-in-js 기법들(styled-component, emotion.js) 에서도 사용할 수 있도록 만든 라이브러리 입니다. 
