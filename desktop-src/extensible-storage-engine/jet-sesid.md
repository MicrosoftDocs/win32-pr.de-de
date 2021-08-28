---
description: 'Weitere Informationen zu: JET_SESID'
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
ms.openlocfilehash: da7acc706017c0346e5a701144d60bcbbfd7cf40
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983793"
---
# <a name="jet_sesid"></a>JET_SESID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_sesid"></a>JET_SESID

Der **JET_SESID-Datentyp** enthält ein Handle für die Sitzung, das für einen Aufruf der JET-API verwendet werden soll.

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>Datentypen

JET_SESID

Entweder **NULL** oder [JET_sesidNil](./invalid-handle-constants.md) können verwendet werden, um ein ungültiges Sitzungshandle anzugeben.

### <a name="remarks"></a>Bemerkungen

Eine Sitzung ist der Transaktionskontext der Datenbank-Engine. Sie kann verwendet werden, um Transaktionen zu starten, zu committen oder abzubricht, die sich auf die Sichtbarkeit und Dauerhaftigkeit von Änderungen auswirken, die von dieser oder anderen Sitzungen vorgenommen werden.

Eine Transaktion kann mit [JetBeginTransaction](./jetbegintransaction-function.md)gestartet werden. Eine Sitzung kann mit [JetBeginSession](./jetbeginsession-function.md)erstellt werden. Die maximale Anzahl von Sitzungen, die gleichzeitig erstellt werden können, wird durch [JET_paramMaxSessions](./resource-parameters.md)gesteuert, die mit [jetSetSystemParameter](./jetsetsystemparameter-function.md)konfiguriert werden kann.

Eine Sitzung wird explizit durch einen Aufruf von [JetEndSession](./jetendsession-function.md) oder implizit durch einen Aufruf von [JetTerm](./jetterm-function.md)beendet.

Jede Sitzung kann jeweils nur von einem Thread verwendet werden. Darüber hinaus besteht das Standardverhalten der Engine darin, die Verwendung einer Sitzung auf denselben Thread von dem Zeitpunkt des ersten Aufrufs von [JetBeginTransaction](./jetbegintransaction-function.md) bis zum Zeitpunkt des übereinstimmenden Aufrufs von [JetCommitTransaction](./jetcommittransaction-function.md) oder [JetRollback](./jetrollback-function.md) einzuschränken. Dieses Verhalten kann geändert werden, um diese zweite Einschränkung durch Festlegen eines benutzerdefinierten Sitzungskontexts mit [JetSetSessionContext](./jetsetsessioncontext-function.md) und [JetResetSessionContext](./jetresetsessioncontext-function.md)zu entfernen.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



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
