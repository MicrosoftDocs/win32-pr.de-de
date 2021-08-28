---
description: 'Weitere Informationen finden Sie unter: JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
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
ms.openlocfilehash: 60920995e72fdc1f45dcc6c083be7bcc1a91b3fa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466407"
---
# <a name="jet_sesid"></a>JET_SESID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_sesid"></a>JET_SESID

Der **JET_SESID** enthält ein Handle für die Sitzung, das für einen Aufruf der JET-API verwendet werden soll.

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>Datentypen

JET_SESID

Entweder **NULL** oder [JET_sesidNil](./invalid-handle-constants.md) kann verwendet werden, um ein ungültiges Sitzungshand handle anzugeben.

### <a name="remarks"></a>Hinweise

Eine Sitzung ist der Transaktionskontext der Datenbank-Engine. Sie kann zum Starten, Commit oder Abbrechen von Transaktionen verwendet werden, die sich auf die Sichtbarkeit und Dauerhaftigkeit von Änderungen auswirken, die von dieser oder anderen Sitzungen vorgenommen werden.

Eine Transaktion kann mit [JetBeginTransaction gestartet werden.](./jetbegintransaction-function.md) Eine Sitzung kann mit [JetBeginSession erstellt werden.](./jetbeginsession-function.md) Die maximale Anzahl von Sitzungen, die zu einem [](./resource-parameters.md)beliebigen Zeitpunkt erstellt werden können, wird durch JET_paramMaxSessions gesteuert, die mit [JetSetSystemParameter konfiguriert werden kann.](./jetsetsystemparameter-function.md)

Eine Sitzung wird explizit durch einen Aufruf von [JetEndSession](./jetendsession-function.md) oder implizit durch einen Aufruf von [JetTerm beendet.](./jetterm-function.md)

Jede Sitzung kann jeweils nur von einem Thread verwendet werden. Darüber hinaus besteht das Standardverhalten der Engine im Einschränken der Verwendung einer Sitzung auf denselben Thread ab dem Zeitpunkt, zu dem der erste Aufruf von [JetBeginTransaction](./jetbegintransaction-function.md) erfolgt, bis zu dem Zeitpunkt, zu dem der entsprechende Aufruf von [JetCommitTransaction](./jetcommittransaction-function.md) oder [JetRollback](./jetrollback-function.md) erfolgt. Dieses Verhalten kann geändert werden, um diese zweite Einschränkung zu entfernen, indem ein benutzerdefinierter Sitzungskontext mit [JetSetSessionContext](./jetsetsessioncontext-function.md) und [JetResetSessionContext gesetzt wird.](./jetresetsessioncontext-function.md)

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_paramMaxSessions](./resource-parameters.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
