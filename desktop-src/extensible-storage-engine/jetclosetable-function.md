---
description: Weitere Informationen finden Sie unter JetCloseTable-Funktion.
title: JetCloseTable-Funktion
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84dbd573db443d09f4ece9271db5307beb17b56071679c15a8873f9ffbe08b32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119361190"
---
# <a name="jetclosetable-function"></a>JetCloseTable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetclosetable-function"></a>JetCloseTable-Funktion

Die **JetCloseTable-Funktion** schließt eine geöffnete Tabelle in einer Datenbank. Die Tabelle kann eine temporäre Tabelle oder eine normale Tabelle sein.

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a>Parameter

*sesid*

Identifiziert den Datenbanksitzungskontext, der für den API-Aufruf verwendet wird.

*tableid*

Identifiziert die zu schließende Tabelle.

Legen *Sie tableid* auf JET_tableidNil, um Arbeitsspeicher frei zu geben.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
</tbody>
</table>


#### <a name="remarks"></a>Hinweise

Diese Funktion muss für alle Tabellen aufgerufen werden, die mit [JetOpenTable geöffnet wurden.](./jetopentable-function.md)

Die Ausnahme von dieser Regel tritt auf, wenn [JetOpenTable](./jetopentable-function.md) in einer Transaktion aufgerufen wird und für die Transaktion ein Rollback ausgeführt wird (mit [JetRollback](./jetrollback-function.md)). Beim Roll back einer Transaktion wird die Tabelle automatisch geschlossen. In diesem Fall ist es ein Fehler, die Tabelle mit **JetCloseTable zu schließen.**

#### <a name="requirements"></a>Anforderungen

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
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetRollback](./jetrollback-function.md)
