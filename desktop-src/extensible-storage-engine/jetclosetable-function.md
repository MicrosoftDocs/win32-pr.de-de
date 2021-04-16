---
description: Weitere Informationen finden Sie in der jetclosetable-Funktion.
title: Jetclosetable-Funktion
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
ms.openlocfilehash: b38ba9b14c34d20b01b6530f2ed3406e55b3bc3f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531100"
---
# <a name="jetclosetable-function"></a>Jetclosetable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetclosetable-function"></a>Jetclosetable-Funktion

Die **jetclosetable** -Funktion schließt eine geöffnete Tabelle in einer Datenbank. Bei der Tabelle kann es sich um eine temporäre Tabelle oder eine normale Tabelle handeln.

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a>Parameter

*-sid*

Identifiziert den Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet wird.

*TableID*

Identifiziert die Tabelle, die geschlossen werden soll.

Legen Sie *TableID* auf JET_tableidNil, um Arbeitsspeicher freizugeben.

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
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Diese Funktion muss für alle mit [jetopentable](./jetopentable-function.md)geöffneten Tabellen aufgerufen werden.

Die Ausnahme von dieser Regel tritt auf, wenn [jetopentable](./jetopentable-function.md) in einer Transaktion aufgerufen wird und für die Transaktion ein Rollback ausgeführt wird (mit [jetrollback](./jetrollback-function.md)). Beim Rollback einer Transaktion wird die Tabelle automatisch geschlossen. In diesem Fall ist es ein Fehler, die Tabelle mit **jetclosetable** zu schließen.

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
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetopentable](./jetopentable-function.md)  
[Jetrollback](./jetrollback-function.md)
