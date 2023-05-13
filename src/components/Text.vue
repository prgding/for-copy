<script setup lang="ts">
import {ref} from "vue";

let seq_customerID = ref('seq_customerID')
let seq_savingID = ref('seq_savingID')
let path = ref('F:\\bank\\Tablespace_Bank.dat')
let userInfo_trigger = ref('userInfo_trigger')
let deposit_trigger = ref('deposit_trigger')
let name1 = ref('张三')
let name2 = ref('李四')
let name3 = ref('王五')
let name4 = ref('小明')
let name5 = ref('小刚')
let pid1 = ref('123451234512345123')
let pid2 = ref('123451234512345124')
let pid3 = ref('123451234512345125')
let pid4 = ref('123451234512345126')
let pid5 = ref('123451234512345127')
let phone1 = ref('12345678901')
let phone2 = ref('12345678902')
let phone3 = ref('12345678903')
let phone4 = ref('12345678904')
let phone5 = ref('12345678905')
let city1 = ref('江西')
let city2 = ref('南昌')
let city3 = ref('江西农业大学')
let city4 = ref('北京')
let city5 = ref('上海')
let card1 = ref('1010357612341234')
let card2 = ref('1010357612341235')
let card3 = ref('1010357612341236')
let card4 = ref('1010357612341237')
let card5 = ref('1010357612341238')
let wrong_pass = ref('密码不正确')
let success_in = ref('成功存入了')
let success_out = ref('成功取出了')
let no_balance = ref('余额不足了')
let wrong_type = ref('交易类型只能为存入/支取')
let rollback = ref('回滚了')


const activeNames = ref(['1'])
const handleChange = (val: string[]) => {
  console.log(val)
}

</script>

<template>
  <div class="container">

    <div class="left">
      <div style="text-align: left;">
        <h3>
          下列默认是我用过的, 最好改一下
        </h3>
        <h3>
          改完之后在右边复制
        </h3>
      </div>

      <el-form
          :label-position="'top'"
          style="max-width: 80%"
      >

        <el-form-item label="customerID序列名" spellcheck="false">
          <el-input v-model="seq_customerID"/>
        </el-form-item>
        <el-form-item label="savingID序列名" spellcheck="false">
          <el-input v-model="seq_savingID"/>
        </el-form-item>
        <el-form-item label="表空间存放位置" spellcheck="false">
          <el-input v-model="path"/>
        </el-form-item>
        <el-form-item label="userInfo触发器名称" spellcheck="false">
          <el-input v-model="userInfo_trigger"/>
        </el-form-item>
        <el-form-item label="deposit触发器名称" spellcheck="false">
          <el-input v-model="deposit_trigger"/>
        </el-form-item>
        <el-form-item label="测试用户1名称" spellcheck="false">
          <el-input v-model="name1"/>
        </el-form-item>
        <el-form-item label="测试用户2名称" spellcheck="false">
          <el-input v-model="name2"/>
        </el-form-item>
        <el-form-item label="测试用户3名称" spellcheck="false">
          <el-input v-model="name3"/>
        </el-form-item>
        <el-form-item label="测试用户4名称" spellcheck="false">
          <el-input v-model="name4"/>
        </el-form-item>
        <el-form-item label="测试用户5名称" spellcheck="false">
          <el-input v-model="name5"/>
        </el-form-item>
        <el-form-item label="身份证号1(必须18位)" spellcheck="false">
          <el-input v-model="pid1"/>
        </el-form-item>
        <el-form-item label="身份证号2(必须18位)" spellcheck="false">
          <el-input v-model="pid2"/>
        </el-form-item>
        <el-form-item label="身份证号3(必须18位)" spellcheck="false">
          <el-input v-model="pid3"/>
        </el-form-item>
        <el-form-item label="身份证号4(必须18位)" spellcheck="false">
          <el-input v-model="pid4"/>
        </el-form-item>
        <el-form-item label="身份证号5(必须18位)" spellcheck="false">
          <el-input v-model="pid5"/>
        </el-form-item>
        <el-form-item label="电话号码1(必须11位)" spellcheck="false">
          <el-input v-model="phone1"/>
        </el-form-item>
        <el-form-item label="电话号码2(必须11位)" spellcheck="false">
          <el-input v-model="phone2"/>
        </el-form-item>
        <el-form-item label="电话号码3(必须11位)" spellcheck="false">
          <el-input v-model="phone3"/>
        </el-form-item>
        <el-form-item label="电话号码4(必须11位)" spellcheck="false">
          <el-input v-model="phone4"/>
        </el-form-item>
        <el-form-item label="电话号码5(必须11位)" spellcheck="false">
          <el-input v-model="phone5"/>
        </el-form-item>
        <el-form-item label="位置1" spellcheck="false">
          <el-input v-model="city1"/>
        </el-form-item>
        <el-form-item label="位置2" spellcheck="false">
          <el-input v-model="city2"/>
        </el-form-item>
        <el-form-item label="位置3" spellcheck="false">
          <el-input v-model="city3"/>
        </el-form-item>
        <el-form-item label="位置4" spellcheck="false">
          <el-input v-model="city4"/>
        </el-form-item>
        <el-form-item label="位置5" spellcheck="false">
          <el-input v-model="city5"/>
        </el-form-item>
        <el-form-item label="卡号1(必须10103576开头+8位数字)" spellcheck="false">
          <el-input v-model="card1"/>
        </el-form-item>
        <el-form-item label="卡号2(必须10103576开头+8位数字)" spellcheck="false">
          <el-input v-model="card2"/>
        </el-form-item>
        <el-form-item label="卡号3(必须10103576开头+8位数字)" spellcheck="false">
          <el-input v-model="card3"/>
        </el-form-item>
        <el-form-item label="卡号4(必须10103576开头+8位数字)" spellcheck="false">
          <el-input v-model="card4"/>
        </el-form-item>
        <el-form-item label="卡号5(必须10103576开头+8位数字)" spellcheck="false">
          <el-input v-model="card5"/>
        </el-form-item>
        <el-form-item label="密码错误提示" spellcheck="false">
          <el-input v-model="wrong_pass"/>
        </el-form-item>
        <el-form-item label="成功存入提示" spellcheck="false">
          <el-input v-model="success_in"/>
        </el-form-item>
        <el-form-item label="成功取出提示" spellcheck="false">
          <el-input v-model="success_out"/>
        </el-form-item>
        <el-form-item label="余额不足提示" spellcheck="false">
          <el-input v-model="no_balance"/>
        </el-form-item>
        <el-form-item label="交易类型错误提示" spellcheck="false">
          <el-input v-model="wrong_type"/>
        </el-form-item>
        <el-form-item label="回滚提示" spellcheck="false">
          <el-input v-model="rollback"/>
        </el-form-item>

      </el-form>
    </div>

    <div class="right">
      <div class="demo-collapse" style="text-align: left;">
        <el-collapse v-model="activeNames" @change="handleChange">
          <el-collapse-item title="用例1" name="1">
            <pre>
--用例1: 建表空间、建表、建约束

--创建序列
CREATE SEQUENCE {{ seq_customerID }} START WITH 1;
CREATE SEQUENCE {{ seq_savingID }} START WITH 1;

--1.创建表空间 Tablespace_Bank
CREATE TABLESPACE Tablespace_Bank
    DATAFILE '{{ path }}'
    SIZE 100M
    AUTOEXTEND ON
    NEXT 256K
    MAXSIZE UNLIMITED;

--2.创建表
--2.1 userInfo 客户信息表
CREATE TABLE userInfo (
    customerID NUMBER,
    customerName VARCHAR2(100),
    PID VARCHAR2(18),
    telephone VARCHAR2(20),
    address VARCHAR2(200)
)TABLESPACE Tablespace_Bank;
CREATE OR REPLACE TRIGGER {{ userInfo_trigger }}
    BEFORE INSERT ON userInfo
    FOR EACH ROW
BEGIN
    :NEW.customerID := {{ seq_customerID }}.NEXTVAL;
END;

--2.2 cardInfo 银行卡信息表
CREATE TABLE cardInfo (
    cardID VARCHAR2(50),
    curType VARCHAR2(50),
    savingID VARCHAR2(50),
    openDate DATE,
    openMoney NUMBER,
    balance NUMBER,
    password VARCHAR2(6),
    IsReportLoss NUMBER,
    customerID NUMBER
)TABLESPACE Tablespace_Bank;

--2.3 tradeInfo 交易信息表
CREATE TABLE tradeInfo (
    transDate DATE,
    cardID VARCHAR2(50),
    transType VARCHAR2(20),
    transMoney NUMBER,
    remark VARCHAR2(255)
)TABLESPACE Tablespace_Bank;

--2.4 deposit 存款类型表
CREATE TABLE deposit (
    savingID VARCHAR2(50),
    savingType VARCHAR2(255),
    describe VARCHAR2(255)
)TABLESPACE Tablespace_Bank;
CREATE OR REPLACE TRIGGER {{ deposit_trigger }}
    BEFORE INSERT ON deposit
    FOR EACH ROW
BEGIN
    :NEW.savingID := {{ seq_savingID }}.NEXTVAL;
END;

--3.添加约束
--3.1 userInfo 表的约束
ALTER TABLE userInfo ADD CONSTRAINT PK_userInfo PRIMARY KEY (customerID);
ALTER TABLE userInfo MODIFY customerName NOT NULL;
ALTER TABLE userInfo MODIFY PID NOT NULL;
CREATE UNIQUE INDEX UQ_PID ON userInfo (PID);
ALTER TABLE userInfo ADD CONSTRAINT check_pid_format CHECK (LENGTH(PID) = 18);
ALTER TABLE userInfo MODIFY telephone NOT NULL;
ALTER TABLE userInfo ADD CONSTRAINT check_telephone_format CHECK (telephone LIKE '____-________' OR LENGTH(telephone) = 11);

--3.2 cardInfo 表的约束
ALTER TABLE cardInfo ADD CONSTRAINT PK_cardInfo PRIMARY KEY (cardID);
ALTER TABLE cardInfo MODIFY cardID NOT NULL;
ALTER TABLE cardInfo ADD CONSTRAINT ck_cardID_format CHECK (REGEXP_LIKE(cardID, '^10103576\d{8}$'));
ALTER TABLE cardInfo MODIFY curType DEFAULT 'RMB' NOT NULL;
ALTER TABLE cardInfo MODIFY savingID NOT NULL;
ALTER TABLE cardInfo MODIFY openDate DEFAULT SYSDATE NOT NULL;
ALTER TABLE cardInfo MODIFY openMoney NOT NULL CHECK (openMoney >= 1);
ALTER TABLE cardInfo MODIFY balance NOT NULL CHECK (balance >= 1);
ALTER TABLE cardInfo MODIFY password DEFAULT 888888 NOT NULL;
ALTER TABLE cardInfo ADD CONSTRAINT CHK_password CHECK (REGEXP_LIKE(password, '^\d{6}$'));
ALTER TABLE cardInfo MODIFY IsReportLoss DEFAULT 0 NOT NULL CHECK (IsReportLoss IN (0, 1));
ALTER TABLE cardInfo MODIFY customerID NOT NULL;
ALTER TABLE cardInfo ADD CONSTRAINT fk_customerID FOREIGN KEY (customerID) REFERENCES userInfo (customerID);

--3.3 tradeInfo 表的约束
ALTER TABLE tradeInfo MODIFY transDate DEFAULT SYSDATE NOT NULL;
ALTER TABLE tradeInfo MODIFY cardID NOT NULL;
ALTER TABLE tradeInfo ADD CONSTRAINT fk_cardID FOREIGN KEY (cardID) REFERENCES cardInfo (cardID);
ALTER TABLE tradeInfo MODIFY transType NOT NULL CHECK (transType IN ('存入', '支取'));
ALTER TABLE tradeInfo MODIFY transMoney NOT NULL CHECK (transMoney > 0);

--3.4 deposit 表的约束
ALTER TABLE deposit ADD CONSTRAINT PK_deposit PRIMARY KEY (savingID);
ALTER TABLE deposit MODIFY savingType NOT NULL;
ALTER TABLE deposit ADD CONSTRAINT ck_savingType CHECK (savingType IN ('活期', '定活两便', '定期'));
ALTER TABLE cardInfo ADD CONSTRAINT fk_savingID FOREIGN KEY (savingID) REFERENCES deposit (savingID);
            </pre>

          </el-collapse-item>
          <el-collapse-item title="用例2" name="2">
            <pre>
--用例2: 插入数据测试

INSERT INTO userInfo (customerID, customerName, PID, telephone, address)
VALUES ({{ seq_customerID }}.NEXTVAL, '{{ name1 }}', '{{ pid1 }}', '{{ phone1 }}', '{{ city1 }}');
INSERT INTO userInfo (customerID, customerName, PID, telephone, address)
VALUES ({{ seq_customerID }}.CURRVAL, '{{ name2 }}', '{{ pid2 }}', '{{ phone2 }}', '{{ city2 }}');
INSERT INTO userInfo (customerID, customerName, PID, telephone, address)
VALUES ({{ seq_customerID }}.CURRVAL, '{{ name3 }}', '{{ pid3 }}', '{{ phone3 }}', '{{ city3 }}');
INSERT INTO userInfo (customerID, customerName, PID, telephone, address)
VALUES ({{ seq_customerID }}.CURRVAL, '{{ name4 }}', '{{ pid4 }}', '{{ phone4 }}', '{{ city4 }}');
INSERT INTO userInfo (customerID, customerName, PID, telephone, address)
VALUES ({{ seq_customerID }}.CURRVAL, '{{ name5 }}', '{{ pid5 }}', '{{ phone5 }}', '{{ city5 }}');

INSERT INTO deposit (savingID, savingType, describe) VALUES ({{ seq_savingID }}.NEXTVAL, '活期', '活期存款');
INSERT INTO deposit (savingID, savingType, describe) VALUES ({{ seq_savingID }}.CURRVAL, '定活两便', '定活两便存款');
INSERT INTO deposit (savingID, savingType, describe) VALUES ({{ seq_savingID }}.CURRVAL, '定期', '定期存款');
INSERT INTO deposit (savingID, savingType, describe) VALUES ({{ seq_savingID }}.CURRVAL, '定期', '定期存款');
INSERT INTO deposit (savingID, savingType, describe) VALUES ({{ seq_savingID }}.CURRVAL, '活期', '活期存款');

INSERT INTO cardInfo (cardID, savingID, openDate, openMoney, balance, customerID)
VALUES ('{{ card1 }}', 3, TO_DATE('2023/05/08', 'YYYY/MM/DD'), 100, 100, 3);
INSERT INTO cardInfo (cardID, curType, savingID, openDate, openMoney, balance, customerID)
VALUES ('{{ card2 }}', 'RMB', 4, TO_DATE('2023/05/9', 'YYYY/MM/DD'), 50, 50, 4);
INSERT INTO cardInfo (cardID, curType, savingID, openDate, openMoney, balance, customerID)
VALUES ('{{ card3 }}', 'RMB', 5, TO_DATE('2023/05/10', 'YYYY/MM/DD'), 200, 200, 5);
INSERT INTO cardInfo (cardID, curType, savingID, openDate, openMoney, balance, password, customerID)
VALUES ('{{ card4 }}', 'RMB', 6, TO_DATE('2023/05/11', 'YYYY/MM/DD'), 150, 150, '111222', 6);
INSERT INTO cardInfo (cardID, curType, savingID, openDate, openMoney, balance, password, IsReportLoss, customerID)
VALUES ('{{ card5 }}', 'RMB', 7, SYSDATE, 1000, 1000, '333444', 0, 7);

INSERT INTO tradeInfo (cardID, transType, transMoney, remark)
VALUES ('{{ card1 }}', '存入', 50, '存款');
INSERT INTO tradeInfo (transDate, cardID, transType, transMoney, remark)
VALUES (SYSDATE, '{{ card2 }}', '支取', 20, '取款');
INSERT INTO tradeInfo (transDate, cardID, transType, transMoney, remark)
VALUES (SYSDATE, '{{ card3 }}', '存入', 100, '存款');
INSERT INTO tradeInfo (transDate, cardID, transType, transMoney, remark)
VALUES (SYSDATE, '{{ card4 }}', '存入', 30, '存款');
INSERT INTO tradeInfo (transDate, cardID, transType, transMoney, remark)
VALUES (SYSDATE, '{{ card5 }}', '支取', 40, '取款');

commit;
            </pre>
          </el-collapse-item>
          <el-collapse-item title="用例3" name="3">
            <pre>
-- 用例3: 模拟常规业务

--1. 修改客户密码
UPDATE cardInfo SET password = '112233' WHERE cardID = '{{ card1 }}';

--2. 办理银行卡挂失
UPDATE cardInfo SET IsReportLoss = 1 WHERE cardID = '{{ card1 }}';

--3. 统计银行资金流通余额和盈利结算
SELECT
    SUM(CASE WHEN transType = '存入' THEN transMoney ELSE 0 END) -
    SUM(CASE WHEN transType = '支取' THEN transMoney ELSE 0 END) AS "银行资金流通余额",
    SUM(CASE WHEN transType = '支取' THEN transMoney * 0.008 ELSE 0 END) -
    SUM(CASE WHEN transType = '存入' THEN transMoney * 0.003 ELSE 0 END) AS "盈利结算"
FROM tradeInfo;

--4. 查询本周开户的卡号，显示该卡相关信息
SELECT * FROM cardInfo
WHERE openDate BETWEEN trunc(sysdate, 'DAY') AND trunc(sysdate, 'DAY') + 6;

--5. 查询本月交易金额最高的卡号
SELECT DISTINCT cardID FROM tradeInfo
WHERE transMoney = (
  SELECT MAX(transMoney)
  FROM tradeInfo
  WHERE TO_CHAR(transDate, 'MM') = TO_CHAR(SYSDATE, 'MM')
);
            </pre>
          </el-collapse-item>
          <el-collapse-item title="用例4" name="4">
            <pre>
--用例4：利用视图实现数据查询

--1. 为客户提供以下3个视图供其查询该客户数据
CREATE VIEW vw_userInfo AS
SELECT customerID AS "客户编号", customerName AS "开户名", PID AS "身份证号", telephone AS "电话号码", address AS "居住地址"
FROM userInfo;

CREATE VIEW vw_cardInfo AS
SELECT cardID AS "卡号", customerID AS "客户编号", curType AS "货币种类", savingID AS "存款类型",
       openDate AS "开户日期", balance AS "余额", password AS "密码", IsReportLoss AS "是否挂失"
FROM cardInfo;

CREATE VIEW vw_tradeInfo AS
SELECT transDate AS "交易日期", transType AS "交易类型", cardID AS "卡号", transMoney AS "交易金额", remark AS "备注"
FROM tradeInfo;

--2. 调用创建的视图获得查询结果
SELECT * FROM vw_userInfo;
SELECT * FROM vw_cardInfo;
SELECT * FROM vw_tradeInfo;
            </pre>
          </el-collapse-item>
          <el-collapse-item title="用例5" name="5">
            <pre>
--用例5: 用存储过程实现业务处理

--1. 完成取款或存款业务

--1.1 创建存储过程
CREATE OR REPLACE PROCEDURE processTransaction(
  p_customerName IN userInfo.customerName%TYPE,
  p_cardID IN OUT cardInfo.cardID%TYPE,
  p_transType IN tradeInfo.transType%TYPE,
  p_transMoney IN tradeInfo.transMoney%TYPE,
  p_password IN cardInfo.password%TYPE DEFAULT NULL
)
IS
  v_customerID userInfo.customerID%TYPE;
  v_balance cardInfo.balance%TYPE;
  v_actualPassword cardInfo.password%TYPE;
BEGIN
  SELECT customerID INTO v_customerID
  FROM userInfo
  WHERE customerName = p_customerName;

  SELECT balance INTO v_balance
  FROM cardInfo
  WHERE cardID = p_cardID
  AND customerID = v_customerID;

  SELECT password INTO v_actualPassword
  FROM cardInfo
  WHERE cardID = p_cardID;

  IF p_transType = '支取' THEN
    IF p_password IS NULL OR p_password != v_actualPassword THEN
      DBMS_OUTPUT.PUT_LINE('{{ wrong_pass }}');
      RETURN;
    END IF;
  END IF;

  BEGIN
    IF p_transType = '存入' THEN
      UPDATE cardInfo
      SET balance = balance + p_transMoney
      WHERE cardID = p_cardID
      AND customerID = v_customerID;

      INSERT INTO tradeInfo (transDate, cardID, transType, transMoney, remark)
      VALUES (SYSDATE, p_cardID, p_transType, p_transMoney, '存入');

      DBMS_OUTPUT.PUT_LINE('{{ success_in }}');
    ELSIF p_transType = '支取' THEN
      IF p_transMoney > v_balance THEN
        DBMS_OUTPUT.PUT_LINE('{{ no_balance }}');
        RETURN;
      END IF;

      UPDATE cardInfo
      SET balance = balance - p_transMoney
      WHERE cardID = p_cardID
      AND customerID = v_customerID;

      INSERT INTO tradeInfo (transDate, cardID, transType, transMoney, remark)
      VALUES (SYSDATE, p_cardID, p_transType, p_transMoney, '支取');

      DBMS_OUTPUT.PUT_LINE('{{ success_out }}');
    ELSE
      DBMS_OUTPUT.PUT_LINE('{{ wrong_type }}');
      RETURN;
    END IF;

    COMMIT;
  EXCEPTION
    WHEN OTHERS THEN
      ROLLBACK;
      DBMS_OUTPUT.PUT_LINE('{{ rollback }}');
      RAISE;
  END;
END;

--1.2 调用存储过程
DECLARE
  v_cardID cardInfo.cardID%TYPE;
BEGIN
  SELECT cardID INTO v_cardID
  FROM cardInfo ci
  JOIN userInfo ui ON ci.customerID = ui.customerID
  WHERE ui.customerName = '{{ name1 }}';
  DBMS_OUTPUT.PUT_LINE('卡号为 ' || v_cardID);

  -- 存款业务
  processTransaction('{{ name1 }}', v_cardID, '存入', 3000);

  -- 取款业务
  processTransaction('{{ name1 }}', v_cardID, '支取', 2000, '112233');
END;


--2. 产生随机卡号
--2.1 创建存储过程
CREATE OR REPLACE PROCEDURE generateCardNumber(
  p_cardID IN OUT cardInfo.cardID%TYPE,
  p_generatedNumber OUT VARCHAR2
)
IS
BEGIN
  p_generatedNumber := '10103576' || TO_CHAR(ROUND(DBMS_RANDOM.VALUE(10000000, 99999999)));

  -- 更新卡号
  p_cardID := p_generatedNumber;
END;

--2.2 调用存储过程
DECLARE
  v_cardID cardInfo.cardID%TYPE := '10103576';
  v_generatedNumber VARCHAR2(20);
BEGIN
  generateCardNumber(v_cardID, v_generatedNumber);
  DBMS_OUTPUT.PUT_LINE('随机卡号为 ' || v_generatedNumber);
END;
            </pre>
          </el-collapse-item>
        </el-collapse>
      </div>
    </div>
  </div>

</template>

<style scoped>
.container {
  display: flex;
}

.left {
  width: 25%;
  padding-left: 30px;
}

.right {
  width: 65%;
}

</style>