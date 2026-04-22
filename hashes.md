# 1. Аудит хэшей пользователей

```text
Исходные данные:
user:a87db2423196431c88a1bdfc21d224b9faf9de74cadb7a578930bed9d5e86382
admin:367c8a75d581c986d352b9ae050ade399506b706d8ddf1b24016b07da1ec307e
web_admin:6578b8835074692df5249b17f18de5559fec0b0aa8c4272679156bcee45c6c52
root:7244957cda5cb2e115aebf8e30c5bd7e539d250f03c1d80fde0c535348e94b4a
db_user:3b95ecea8aca178ebfbaac1b46f2b0bde7e8b4b2353ffffeea74c5092e3a7159
```

Все значения содержат **64 шестнадцатеричных символа**, что соответствует алгоритму:

```text
Все значения содержат **64 шестнадцатеричных символа**, что соответствует алгоритму:
SHA-256
-m 1400
```

| Пользователь | Пароль         |
| ------------ | -------------- |
| user         | MILO2008       |
| admin        | hxtour         |
| web_admin    | t061584        |
| root         | washington1776 |
| db_user      | mmr431723      |



## 2. Оптимальный подбор PIN-кода

```text
Исходные данные:
75d25e48a3d92c398bb6a7873d6a22281f6bdd50f78956f666f717135190127cbbeec3fd35b9fb03925d6bf595baa022d10d247104cced3a0a8f4a6656c4bf6a 
684a71e209bad7d9c3a802386150a24b31be323e7e42624bbe787e381cfe0796820fb1aeabb45ec966c6e427babb5ece40824297dac97c37f2e41be6958ea324 
8f2090b09018f7431d25a92da885c6f3e80ea538778639072aa15b7484b44d92ecb6cae59350f3bd1846ab492e8604f8d3b25f0e5842c2335b0b03bae5e690c0 
7765080f31bffe1d14ff17db9316b538db5761ea5592454f3d7a71961567af39e91c1c60898bda23f0c6514b0c6ff8e3c830a22846fe1af94b2d6023c89449a1 
7c3a635c9bbedd8f74ddb9cdcea921368e728b6f65cdae7a6eec537748cf8831e57a8706494220b9caf695b4cb79aa655c7c6b635b49c1fdc318ea410c0ae49f
```

```text
Все значения содержат **64 шестнадцатеричных символа**, что соответствует алгоритму:
SHA-512
-m 1700
```

| Хэш         | PIN-код |
| ----------- | ------- |
| 75d25e48... | 5472    |
| 7c3a635c... | 17456   |
| 8f2090b0... | 11082   |
| 7765080f... | 4653    |

## 3. Атака с учётом соли

```text
Исходные данные:
user:1337:70ab6e15b42f3e8addef4be9651f8c6f872dc8ac5a36d2b6160493bcc3d4f987 
admin:9117:6c39425f74db54f7d99cbfb1a12816421b1a1db02003bfbe3270ec0113726b25 
web_admin:2560:433a276d5c258c089d803c77b76e7367f772f6c4c34fc524c70cda9bc5e3828d 
root:6766:ef62c8bbf7e8bb6e57ca5d8153c7e11864c0ce4cb0be51ee50ebff4e42750dee 
db_user:3780:44ca6adee541830e8c69ced64b361a51f3be10acb7286af94922449e4b164fd5
```


```text
Все значения содержат **64 шестнадцатеричных символа**, что соответствует алгоритму:
SHA-256
-m 1410
```

| Логин     | Salt | Пароль    |
| --------- | ---- | --------- |
| user      | 1337 | 54cami9   |
| admin     | 9117 | 428248h   |
| web_admin | 2560 | 656800    |
| root      | 6766 | rubenkus  |
| db_user   | 3780 | cup+preds |

## 4. MD5 через радужные таблицы

```text
Исходные данные:
d1e576b71ccef5978d221fadf4f0e289 
22d7fe8c185003c98f97e5d6ced420c7 
8a24367a1f46c141048752f2d5bbd14b 
8344711654700fe530f0d2ac74599a48 
a67e565b11cd18f7a922b58f5476b569
```
