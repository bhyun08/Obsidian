`@GeneratedValue` : JPA에서 사용되는 어노테이션으로, 엔티티의 기본 키(primary key) 값을 자동으로 생성해주는 전략을 정의할 때 사용한다. 이 어노테이션은 주로 `@Id` 어노테이션과 함께 사용되며, 엔티티의 식별자를 자동으로 생성하고 관리하는 방법을 지정한다.

### 주요 속성

`@GeneratedValue` 어노테이션은 몇 가지 속성을 통해 키 생성 전략을 정의할 수 있다.

1. **strategy**: 키 생성 전략을 지정합니다. 주로 사용되는 값은 다음과 같습니다:
    
    - **GenerationType.AUTO**: 기본 생성 전략을 사용합니다. 데이터베이스 벤더에 따라 적절한 전략을 자동으로 선택한다.
    - **GenerationType.IDENTITY**: 데이터베이스의 IDENTITY 컬럼을 사용하여 키를 자동으로 증가시킵니다.
    - **GenerationType.SEQUENCE**: 데이터베이스 시퀀스를 사용하여 키를 생성한다.
    - **GenerationType.TABLE**: 별도의 키 생성 테이블을 사용하여 키를 생성한다. 데이터베이스 독립적인 방식이다.
    
2. **generator**: 사용할 시퀀스 생성기 또는 테이블 생성기의 이름을 지정한다.