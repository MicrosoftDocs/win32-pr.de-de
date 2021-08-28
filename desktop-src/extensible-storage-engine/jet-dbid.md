---
description: 'Weitere Informationen finden Sie unter: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c576734a3e2da71f041509e5b7d7d9244427dbb8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986693"
---
# <a name="jet_dbid"></a>JET_DBID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_dbid"></a>JET_DBID

Der **JET_DBID-Datentyp** enthält das Handle für die Datenbank. Ein Datenbankhand handle wird verwendet, um das Schema einer Datenbank zu verwalten. Sie kann auch verwendet werden, um die Tabellen innerhalb dieser Datenbank zu verwalten.

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>Datentypen

JET_DBID

Handle für die Datenbank.

Der Wert JET_dbidNil gibt an, dass das Handle ungültig ist.

### <a name="remarks"></a>Bemerkungen

Ein Datenbankhandl wird durch einen Aufruf von [JetCreateDatabase](./jetcreatedatabase-function.md) oder [JetOpenDatabase erstellt.](./jetopendatabase-function.md)

Ein Datenbankhand handle kann explizit durch [JetCloseDatabase](./jetclosedatabase-function.md) oder implizit durch [JetEndSession](./jetendsession-function.md) oder [JetTerm geschlossen werden.](./jetterm-function.md)

Ein Datenbankhand handle kann nur innerhalb der Sitzung verwendet werden, in der es erstellt wurde. Das Vorhandensein eines Datenbankhandpunkts entspricht dem logischen Öffnen einer Datenbank. Ein logisches Öffnen ist anders als das physische Öffnen einer Datenbank, was geschieht, wenn eine Datenbank an das System angefügt wird.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetEndSession](./jetendsession-function.md)
