---
title: Java로 if-else문을 사용하여 String을 사용해보자
date: 2024-09-12 11:49:33 +09:00
categories: [Java]
tags:
    [
        Java,
        간단
    ]
---

# 서론
Java에서 객체의 메서드를 호출하기 위해서는 **객체.메서드** 형식으로 사용할 수 있다.  

**String**으로 값을 받아 입력된 첫 번째 값이 **소문자**인지, **대문자**인지, **숫자**인지, **기타**인지 확인 하는 코드를 짜 보자.  

**String**의 첫 번째 값을 읽기 위해서는 **charAt(0)** 을 사용하면 된다.  

## 코드
~~~java
import java.util.Scanner;

public class StringObject {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("키를 입력하시오: ");
        String st = sc.next();

        char ch = st.charAt(0);

        if('0' <= ch && ch <= '9'){
            System.out.print("숫자입니다.");
        }else if('a' <= ch && ch <= 'z'){
            System.out.print("소문자입니다.");
        }else if('A' <= ch && ch <= 'Z'){
            System.out.print("대문자입니다.");
        }else{
            System.out.print("기타");
        }
        sc.close();
    }
}
~~~  

## 결과 
~~~
키를 입력하시오: 89
숫자입니다.
~~~  
~~~
키를 입력하시오: hello
소문자입니다.
~~~  
~~~
키를 입력하시오: Hello
대문자입니다.
~~~  
~~~
키를 입력하시오: ^^
기타
~~~  

# 결론
이렇게 입력값이 숫자라 하더라도 String으로 처리할 수 있다.  

객체 생성과 사용은 다음에 알아보도록 하자.