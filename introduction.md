
# 1. 소개

```
이 챕터에서는 그래프 데이터베이스의 개념 및 Neo4j의 주요 특징에 대해 다룹니다.
```

## 1.1. Neo4j 주요특징

연결된 데이터는 주변에서 흔히볼 수 있습니다. Neo4j는 풍부한 데이터 커넥션을 활용하고 빠르게 성장하는 그래프 기반 시스템을 지원합니다.


**그래프 데이터베이스** : Neo4j는 처음부터 그래프 데이터베이스로 설계되었습니다. 이 아키텍처는 노드와 관계의 빠른 관리와 저장 및 변환을 최적화하도록 설계되었습니다. Neo4j에서 관계는 엔터티 간의 사전 구체화 된 연결을 나타내는 일급 객체입니다. 관계형 데이터베이스는 릴레이션(relational) 수에 따라 기하 급수적으로 성능이 저하되는 조인입니다. 이것의 성능은 선형이며 한 노드에서 다른 노드를 탐색하는 Neo4j에 의해 수행됩니다.

엔터티 간의 연결 저장 및 쿼리의 접근 방식은 초당 최대 4 백만 홉(hop)과 코어를 순회하는 기능을 제공합니다. 대부분 그래프 검색은 더 큰 인접 지역 노드에 국한되므로, 데이터베이스에 저장된 데이터는 작업 런타임에 영향을 주지 않습니다. 전용 메모리 관리, 뛰어난 확장성 및 효율적인 메모리 작업이 이점입니다.


**화이트보드 친화성** : 속성 그래프 방식을 사용하면 모든 도메인 및 사용 사례의 개념, 설계, 구현, 저장 및 시각화 전반에 걸쳐 동일한 모델을 일관되게 사용할 수 있습니다. 이를 통해 모든 비즈니스 이해 관계자가 개발 전과정에 참여할 수 있습니다. 스키마 옵션 모델을 사용하면 요구 사항이 변경 될 때 고비용 스키마 변경 및 마이그레이션에 대한 패널티없이 도메인 모델을 계속 발전시킬 수 있습니다.

선언 그래프 쿼리 언어인 Cypher는 노드와 관계 그래프 패턴을 시각적으로 나타내도록 설계되었습니다. 유용하고 쉽게 읽을 수 있는 쿼리 언어는 특정 도메인 개념이나 질문을 표현하는 패턴을 중심으로합니다. Cypher는 특정 사례 최적화를 위해 확장될 수도 있습니다.


**신속한 개발 지원** : Neo4j는 그래프 기반 시스템의 빠른 개발을 지원합니다. Neo4j 개발은 관련성이 높은 정보의 실시간 쿼리를 위해 필요합니다. 이것은 다른 데이터베이스가 제공할 수 없는 기능입니다. 이런 Neo4j 고유 기능을 사용하면 가동성 및 확장성이 뛰어난 응용 프로그램을 빠르게 개발할 수 있습니다. 


**ACID트랜잭션을 이용한 데이터 안전성 제공** : Neo4j는 트랜잭션을 사용하여 하드웨어 오류 및 시스템 장애 발생시 데이터가 유지되도록 합니다.
 
 
**중요한 업무 및 고성능 운영을 위한 설계** : Neo4j 클러스터링은 중대한 비즈니스 및 고성능 어플리케이션을 지원하도록 설계되었습니다. 이러한 설계는 작은 스토리지에 영향을 받는 동안 상상가능한 가장 큰 데이터 세트를 위해 수백 조 개 이상의 엔터티를 저장할 수 있습니다. Neo4j는 확장 가능한 fault-tolerant cluster로 배치할 수 있습니다. 높은 확장성으로 인해 Neo4j 클러스터는 수백 개 또는 수천 개가 아닌 수십 대의 장비만 필요하므로 비용과 운영상의 복잡성이 줄어듭니다. 생산 어플리케이션의 다른 기능으로는 최신백업 및 광범위한 모니터링이 있습니다.

**Neo4j의 어플리케이션의 한계는 당신의 상상력에 제한됩니다.**