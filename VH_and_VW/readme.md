```css
html {
    font-size: 62.5%;
}

html, body {
    height: 100%;
}

div {
    height: 100%;
    background: blue;
}

/* 위 코드는 아래와 같다 */
html {
    font-size: 62.5%;
}

div {
    background: blue;
    height: 100vh;
}


/* ------------------------------------------ rem 을 사용하는 이유*/
html {
    font-size: 62.5%;
}

div {
    min-height: 50vh;
    font-size: 2.4rem
}

div h2 {

}

@media (max-width: 1024px) {
    body {
        background: lightblue;
    }

    html {
        font-size: 50%;
        /* 위의 div에 정의해둔 font-size를 일일히 px을 사용 할 필요 없이 유연히 자동으로 조절됨 */
    }
}

/* 더 cool 한 방법 */
html {
    font-size: 62.5%;
}

div {
    min-height: 50vh;
    /* 사이즈에 따라서 1vw가 다르기 떄문에 조금 더 쿨한 방법 */
    /* font-size: calc(2.4rem + 0.5vw) */
    /* font-size: calc(2.4rem + 1vw);  */
    /* 아래 media에 정의한 크기를 제외하고는 font-size 고정 */
    font-size: 3.6rem;
}

div h2 {

}

@media (min-width: 500px) and (max-width: 1024px) {
    body {
        background: lightblue;
    }

    div {
        font-size: calc(2.4rem + 1vw); 
    }

    html {
        font-size: 50%
    }
}
```