### 통계(SW활용현황) API를 위한 DB, Table 생성

![image](https://github.com/user-attachments/assets/0dc9fa5a-62e5-49ef-891b-088e91040116)
CREATE DATABASE statistic;
USE statistic;
CREATE TABLE requestInfo (
    requestID numeric NOT NULL PRIMARY KEY,
    requestCode varchar(5) NOT NULL,
    userID varchar(5),
    createDate varchar(10)
);

CREATE TABLE requestCode (
    requestCode varchar(5) NOT NULL PRIMARY KEY,
    code_explain varchar(50) NOT NULL
);

CREATE TABLE user (
    userID varchar(5) NOT NULL PRIMARY KEY,
    HR_ORGAN varchar(5) NOT NULL,
    USERNAME varchar(5) NOT NULL
);
INSERT INTO requestInfo(requestID, requestCode, userID, createDate)
VALUES 
(1, 'L', 'AAA', '200818'),
(2, 'O', 'DDD', '200404'),
(3, 'L', 'BBB', '200622'),
(4, 'L', 'CCC', '190622');

INSERT INTO requestCode(requestCode, code_explain)
VALUES 
('L', 'Request Type L'),
('O', 'Request Type O');

INSERT INTO user(userID, HR_ORGAN, USERNAME)
VALUES 
('AAA', 'HR1', 'User1'),
('DDD', 'HR2', 'User2'),
('BBB', 'HR1', 'User3'),
('CCC', 'HR3', 'User4');

SELECT * FROM requestInfo;
SELECT * FROM requestCode;
SELECT * FROM user;
