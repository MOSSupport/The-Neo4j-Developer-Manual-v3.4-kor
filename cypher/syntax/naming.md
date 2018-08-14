### 3.2.2. 명명 규칙 및 권장사항

명명 규칙 및 권장사항, 관계 유형 및 속성 이름과 [변수](./variables.md)에 대해 알아봅니다.


#### 3.2.2.1. 명명 규칙 

- 영문자로 시작해야 합니다. 
 
  - 이것은 `å`, `ä`, `ö`, `ü`와 같은 영어가 아닌 문자를 포함합니다. 
  - 영문자가 아닌 문자가 필요한 경우 이스케이프에 백틱을 사용하십시오. 예 : ``^ n``.

- 숫자를 포함할 수 있지만, 첫 번째 문자는 포함할 수 없습니다. 

  - ```first1```는 허용되지만, ```1first```는 허용되지 않습니다. 
  - 주요 숫자가 필요한 경우 이스케이프에 괄호를 사용하십시오. 예 : ``1first``.

- 기호를 포함할 수 없습니다. 

  - 밑줄을 사용한 예외처리는 다음과 같이 사용합니다. ```my_variable```
  -이 규칙에 대한 표면적인 예외는```$ myParam```에 주어진 [변수](./parameters.md)를 나타내는 첫번째 문자 ```$```를 사용합니다.
  - 주요 상징 문자가 필요한 경우 이스케이프에 괄호를 사용하십시오. 예 : ``$$ n``.
- Neo4j버전에 따라서 ```65535``` (```2^16 - 1```) 또는 ```65534``` 문자와 같이 길어질 수 있습니다. 
- 대/소문자를 구분합니다.

  - 따라서, ```:PERSON```, ```:Person``` 그리고 ```:person```는 다른 세가지 라벨이며, `n` 와 `N`는 다른 두 가지 변수 입니다.  
- 공백 문자:

  - 선행 및 후행 공백 문자는 자동으로 제거됩니다. 예를 들어서, ```MATCH ( a ) RETURN a```는 ```MATCH (a) RETURN a```와 같습니다. 
  - 만약 이름에 공백이 필요할 경우 이스케이프에 백틱(backtick)을 사용하십시오. 예 : ``변수에 공백이있다 .``

#### 3.2.2.2. 범위 지정 및 네임스페이스(namespace) 규칙

- 노드 라벨, 관계 유형 및 속성 명은 재사용할 수 있습니다. 
  - 레이블, 유형 및 특성 이름에 대해 ```a```가 있는 다음 조회는 유효합니다.
    ```CREATE (a:a {a: 'a'})-[r:a]→(b:a {a: 'a'})```.

- 노드 및 관계의 변수는 같은 쿼리 범위 내에서 이름을 재사용할 수 없습니다. 
  - 노드와 관계가 같은 이름을 가졌기에 아래 쿼리를 사용할 수 없습니다. 
     ```a```: ```CREATE (a)-[a]→(b)```. 
 

#### 3.2.2.3. 추천 

아래 명명 규칙을 권장합니다. 

| 노드 라벨 | 대문자로 시작하는 Camel 케이스    | `:vehice_owner` 보다 ```:VehicleOwner```사용   |
| --------- | --------------------------------- | ---------------------------------------------- |
| 관계 유형 | 대문자, 밑줄을 사용하여 단어 분리 | `:OWNS_VEHICLE` rather than `:ownsVehicle` etc |