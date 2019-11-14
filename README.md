## 데이터센터프로그래밍 3차 과제

아래 포스팅 글의 서비스를 Dockerization 하였습니다.

https://velopert.com/594

2차 과제에서 Dockerization했던 내용을
docker-swarm 이용하여 docker-machine 2개에서 각각의 작업이 정보를 주고 받도록 하였습니다.

### 실행
```
$ docker stack deploy -c docker-compose-dockerswarm.yml bookstack
```

### API 목록
| ROUTE                     | METHOD | DESCRIPTION               |
|---------------------------|--------|---------------------------|
| /api/books                | GET    | 모든 book 데이터 조회     |
| /api/books/:book_id       | GET    | _id 값으로 데이터 조회    |
| /api/books/author/:author | GET    | author 값으로 데이터 조회 |
| /api/books                | POST   | book 데이터 생성          |
| /api/books/:book_id       | PUT    | book 데이터 수정          |
| /api/books/:book_id       | DELETE | book 데이터 제거          |
