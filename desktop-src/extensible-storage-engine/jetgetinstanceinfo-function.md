---
description: 'Weitere Informationen finden Sie unter: jetgetinstancinput Info-Funktion'
title: Jetgetinstancinput Info-Funktion
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866824"
---
# <a name="jetgetinstanceinfo-function"></a>Jetgetinstancinput Info-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetinstanceinfo-function"></a>Jetgetinstancinput Info-Funktion

Die **jetgetinstanceinfo** -Funktion Ruft Informationen zu den Instanzen ab, die ausgeführt werden.

**Windows XP: jetgetinstanceinfo** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>Parameter

*pcinstanceingefo*

Ein Zeiger auf einen Puffer, der die Anzahl der in " *painstanceinfo*" gespeicherten Elemente empfängt.

*painstanceingefo*

Ein Zeiger auf einen Puffer, der die Adresse des ersten Elements eines Arrays von-Strukturen empfängt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dieser Fehler wird von <strong>jetgetinstanceingefo</strong> zurückgegeben, wenn Folgendes gilt:</p>
<ul>
<li><p><em>pcinstanceingefo</em> oder <em>painstanceingefo</em> ist NULL.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Es ist nicht genügend Arbeitsspeicher vorhanden, um die Anforderung zu verarbeiten.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Die Datenbank-Engine weist ein Array von [JET_INSTANCE_INFO](./jet-instance-info-structure.md) Strukturen zu. Der Aufrufer ist dafür verantwortlich, diesen Arbeitsspeicher mit [jetfrebuffer](./jetfreebuffer-function.md)freizugeben.

Wenn keine aktiven Instanzen vorhanden sind, gibt **jetgetinstanceinfo** JET_errSuccess zurück, und *pcinstanceinfo* erhält den Wert 0.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetgetinstancin Fow</strong> (Unicode) und <strong>jetgetinstanceingefoa</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[Jetfrebuffer](./jetfreebuffer-function.md)
