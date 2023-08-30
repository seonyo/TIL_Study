## 제네릭 
<hr>

### 제네릭이란
- 제네릭 : 객체를 수집, 관리하는 컬렉션을 이용할 때 반드시 사용 됨
- 제네릭을 사용하면 데이터를 저장하는 시점에 어떤 데이터를 저장할 것인지 명시할 수 있음
- 데이터의 사용 여부를 컴파일 시점에 확인 할 수 있음


``` java
public class Box<T>{
    private T item;

    public Box (T item){
        this.item = item;
    }
    public T getItem(){
        return item;
    }
}

public static void main (String args[]){
    Box <Apple> box = new Box(new Apple(10));
    Apple apple = box.getItem();
    System.out.println(apple.getSugarContent());
}
```

이렇게 타입파라미터로 명시해주면, Apple 클래스만 넘어간다 <br>
레이블과 같이 생각하기!