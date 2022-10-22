redis zip 다운로드: https://github.com/microsoftarchive/redis/releases

redis-server 시작
redis-cli 접속

//현재 키값 확인
keys *

// 키 저장
set mykey ""Hello""
set [key] [value]

//여러개 키값 저장
MSET key1 ""Hello"" key2 ""World""
MSET [key1] [value1] [key2] [value2]

//소멸 시간 지정해서 저장하기
setex mykey 10 ""Hello""
setex [key] [time] [value]

//키 값 불러오기
get [key]

//여러개 키 값 불러오기
mget [key1] [key2]

//키 삭제하기
del [key]

//키 남은시간 확인하기
ttl [key]

//키 검색하기
key *[검색어]*

//키 이름 바꾸기
rename [기존키] [바꿀키]

// 바꿀 이름이 존재하지 않는 이름일 경우만 키 이름 바꾸기 (결과: 성공:!, 실패:0)
renamenx [기존키] [바꿀키]

//모든 키 값 삭제하기
flushall

//hash 형태 저장하기
hmset [key] [컬럼1] [내용1] [컬럼2] [내용2]

//hash 컬럼 get하기
hmget [key] [컬럼]

// hash 모든 데이터 get하기
hgetall [key]

//list 데이터 한개씩 추가
lpush [key] ""{\""Age\"":20, \""Name\"":\""Mary\""}""
rpush [key] ""{\""Age\"":20, \""Name\"":\""Mary\""}""

// 특정 인덱스로 list get 하기
lrang [key] 0-1

//맨 처음 해당하는 요소 삭제 후 반환
lpop [key]
