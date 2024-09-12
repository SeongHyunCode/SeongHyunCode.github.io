---
title: Java의 switch문을 사용해보자
date: 2024-09-12 11:10:33 +09:00
categories: [Java]
tags:
    [
        Java,
        간단
    ]
---

# 서론

**switch** 문은 Java에서 조건에 따라 여러 코드들 중 하나를 선택하여 실행하는 제어 흐름 문이다.  

**switch** 문은 **if - else** 문과 비슷하게 동작하지만, 여러 값 중 하나를 선택할 때 더 간결하고 읽기 쉽게 작성할 수 있다.  

다음은 **switch** 문의 기본적인 구조이다.  
~~~java
switch (제어문) {
    case 1:
        // code
        break;
    case 2:
        // code
        break;
    // 여러 개의 case 추가 가능
    default:
        // code
}
~~~  

**case 1** 부터 찾기 시작하여 원하는 값을 찾을 때 까지 다음으로 넘어가며 원하는 값을 찾으면 **break** 가 실행되어 **switch** 문을 빠져나온다.  

만약 모든 **case** 에 찾는 값이 없다면 **default:** 가 실행된다.  

정수형 변수 num이 30이라고 가정하고 나머지연산을 해서 나머지가 0이면 3의 배수일 것이고, 아니면 3의 배수가 아닐 것이다.

## 코드

~~~java
public class SwitchMultiple {
    public static void main(String[] args){
        int num = 30;

        switch(num % 3){
            case 0: System.out.println("3의 배수입니다.");
                break;
            case 1:
            case 2: System.out.println("3의 배수가 아닙니다.");
                break;
            default: System.out.println("3의 배수가 아닙니다.");
        }
    }
}
~~~  

여기서 default는 필요없는 코드이지만 **default** 예시를 위해 작성하였다.  

## 결과

~~~
3의 배수입니다.
~~~  

# 결론

Java의 **switch** 문은 간단하게 원하는 값을 찾을 수 있기에 많이 사용된다. 더욱 열심히 하자.