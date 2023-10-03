1.
b) they create tables and insert data
c) fixed by raising the block containing close to accomodate for secondary keys

2.
b)
ERROR:  (isbn10)=(0321197844) 키가 이미 있습니다.중복된 키 값이 "book_isbn10_key" 고유 제약 조건을 위반함 

오류:  중복된 키 값이 "book_isbn10_key" 고유 제약 조건을 위반함
SQL state: 23505
Detail: (isbn10)=(0321197844) 키가 이미 있습니다.

c)
INSERT 0 1

Query returned successfully in 24 msec.

2(d)
INSERT 0 1

Query returned successfully in 26 msec.

2e)
INSERT 0 1

Query returned successfully in 25 msec.

2f)
UPDATE 26

Query returned successfully in 24 msec.

2g)
Delete from student where department = 'chemistry'
deleted 0

2h)
ERROR:  (email)=(xiexin2011@gmail.com) 키가 "loan" 테이블에서 여전히 참조됩니다."student" 테이블의 자료 갱신, 삭제 작업이 "loan_borrower_fkey" 참조키(foreign key) 제약 조건 - "loan" 테이블 - 을 위반했습니다 

오류:  "student" 테이블의 자료 갱신, 삭제 작업이 "loan_borrower_fkey" 참조키(foreign key) 제약 조건 - "loan" 테이블 - 을 위반했습니다
SQL state: 23503
Detail: (email)=(xiexin2011@gmail.com) 키가 "loan" 테이블에서 여전히 참조됩니다.

3a)
 "deferrable constraint" refers to a type of database constraint that can be deferred until the end of a transaction, allowing for more flexibility in enforcing data integrity rules.

3b)
ERROR:  (isbn13)=(978-0321197849) 키가 "copy" 테이블에서 여전히 참조됩니다."book" 테이블의 자료 갱신, 삭제 작업이 "copy_book_fkey" 참조키(foreign key) 제약 조건 - "copy" 테이블 - 을 위반했습니다 

오류:  "book" 테이블의 자료 갱신, 삭제 작업이 "copy_book_fkey" 참조키(foreign key) 제약 조건 - "copy" 테이블 - 을 위반했습니다
SQL state: 23503
Detail: (isbn13)=(978-0321197849) 키가 "copy" 테이블에서 여전히 참조됩니다.

First code that set constraints to immediate cannot be executed since the entries reference each other.

Second code that allows constraints to be deferred can delete the entry.

(a)
No. If the book is not currently borrowed, we can delete the copy entry.
alter table copy add column available boolean

(b)
If we need all students from a certain faculty, we can create a view with a union of different departments under that faculty.