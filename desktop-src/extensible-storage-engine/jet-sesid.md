---
description: 'Weitere Informationen finden Sie hier: JET_SESID'
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
ms.openlocfilehash: 542802c806bbea55aafb4fc1a0241a92b2842878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862208"
---
# <a name="jet_sesid"></a>JET_SESID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_sesid"></a>JET_SESID

Der **JET_SESID** -Datentyp enthält ein Handle für die Sitzung, die für einen aufzurufenden Jet-API-Befehl verwendet werden soll.

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>Datentypen

JET_SESID

Entweder **null** oder [JET_sesidNil](./invalid-handle-constants.md) kann verwendet werden, um ein ungültiges Sitzungs handle anzugeben.

### <a name="remarks"></a>Bemerkungen

Eine Sitzung ist der Transaktionskontext der Datenbank-Engine. Sie kann verwendet werden, um Transaktionen zu starten, zu übertragen oder abzubrechen, die die Sichtbarkeit und Dauerhaftigkeit von Änderungen, die von dieser oder anderen Sitzungen vorgenommen werden, beeinflussen.

Eine Transaktion kann mithilfe von [jetbegintransaction](./jetbegintransaction-function.md)gestartet werden. Eine Sitzung kann mithilfe von [jetbeginsession](./jetbeginsession-function.md)erstellt werden. Die maximale Anzahl von Sitzungen, die zu einem beliebigen Zeitpunkt erstellt werden können, wird durch [JET_paramMaxSessions](./resource-parameters.md)gesteuert, der mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md)konfiguriert werden kann.

Eine Sitzung wird explizit durch einen " [jetendsession](./jetendsession-function.md) "-Rückruf beendet oder durch einen " [jetterm](./jetterm-function.md)"-Befehl implizit beendet.

Jede Sitzung kann nur von einem Thread gleichzeitig verwendet werden. Außerdem besteht das Standardverhalten der-Engine darin, die Verwendung einer Sitzung auf denselben Thread ab dem Zeitpunkt zu beschränken, zu dem der erste Aufruf von [jetbegintransaction](./jetbegintransaction-function.md) bis zu dem Zeitpunkt erfolgt, zu dem der Aufruf von [jetcommittransaction](./jetcommittransaction-function.md) oder [jetrollback](./jetrollback-function.md) durchgeführt wird. Dieses Verhalten kann geändert werden, um diese zweite Einschränkung zu entfernen, indem ein benutzerdefinierter Sitzungs Kontext mithilfe von [jetsetessioncontext](./jetsetsessioncontext-function.md) und [jetresetessioncontext](./jetresetsessioncontext-function.md)festgelegt wird.

### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_paramMaxSessions](./resource-parameters.md)  
[Jetbeginsession](./jetbeginsession-function.md)  
[Jetbegintransaction](./jetbegintransaction-function.md)  
[Jetcommittransaction](./jetcommittransaction-function.md)  
[Jetendsession](./jetendsession-function.md)  
[Jetresessioncontext](./jetresetsessioncontext-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetabessioncontext](./jetsetsessioncontext-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[Jetterm](./jetterm-function.md)
