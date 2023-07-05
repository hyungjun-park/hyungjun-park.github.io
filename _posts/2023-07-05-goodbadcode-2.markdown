---
layout: post
title:  "[도서] Good Code, Bad Code - 2. 추상화 계층"
date:   2023-07-05 22:00:25 +0900
categories: book
---

# 2. 추상화 계층
**주요 내용**
- 깔끔한 추상화 계층을 통해 문제를 하위 문제로 세분화하는 방법
- 추상화 계층이 코드 품질의 요소를 달성하는 데 어떻게 도움이 되는지
- API 및 구현 세부 사항
- 함수, 클래스 및 인터페이스를 사용해 코드를 추상화 계층으로 나누는 방법

코드를 구성하는 방법은 코드 품질의 기본적인 측면 중 하나이며, 코드를 잘 구성한다는 것은 간결한 추상화 계층을 만드는 것으로 귀결될 때가 많다.
잘 추상화된 코드는 가독성, 모듈성, 재사용성, 일반화성 및 테스트 용이성이 크게 개선된다.

## 2.1 널값 및 의사코드 규약
> 해당 장의 예제 코드에서 어떻게 널값을 다루는지 설명하는 내용이다.

프로그래밍 언어에는 값이 없다는 개념을 표현하기 위해 널값을 사용한다. 이 널값은 유용하면서도 문제가 많다.
- 값이 제공되지 않거나 함수가 원하는 결과를 반환할 수 없는 경우가 자주 발생하기 때문에 '값이 없다' 또는 '부재한다'는 재념은 유용하다.
- 값이 널일 수 있거나 혹은 널이면 안 되는 경우가 항상 명백한 것은 아니라서 문제가 발생한다. 개발자들은 변수에 액세스하기 전에 널값인지 확인하는 것을 자주 잊어버린다. (NullPointException)

널 안전성(null safety) 혹은 보이드 안전성(void safety)에 대한 생각이 점점 더 많은 추진력을 얻고 있다. 이렇게 하면 널값이 가능할 경우 그에 맞게 표시해야 하고 컴파일러는 반드시 널값 여부 확인을 할 수밖에 없도록 만든다.
 사용 중인 언어가 널 안전성을 지원한다면 사용하는 것이 좋다.
``` java
Optional<Element> getFifthElement(List<Element> elements) {
    if (elements.size() < 5) {
        return Optional.empty(); // Optional.empty() 가 널값 대신 반환된다.
    }
    return Optional.of(elements[4]);
}
```

## 2.2 왜 추상화 계층을 만드는가?

## 2.3 코드의 계층

## 2.4 마이크로서비스는 어떤가?

