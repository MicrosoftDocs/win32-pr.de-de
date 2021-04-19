---
description: 'Weitere Informationen finden Sie hier: jejessnapshotabort-Funktion'
title: Jejessnapshotabort-Funktion
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349998"
---
# <a name="jetossnapshotabort-function"></a>Jejessnapshotabort-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotabort-function"></a>Jejessnapshotabort-Funktion

Die **jedessnapshotabort** -Funktion benachrichtigt die Engine, dass Sie normale e/a-Vorgänge fortsetzen kann, nachdem eine Sperrfrist mit einem fehlerhaften Snapshot erreicht wurde.

**Windows Server 2003:**  **jedessnapshotabort** wurde in Windows Server 2003 eingeführt.

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapid*

Der Bezeichner der Momentaufnahme Sitzung.

*grbit*

Die Optionen für diesen-Befehl. Dieser Parameter ist für die zukünftige Verwendung reserviert, und der einzige gültige Wert ist 0 (null).

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
<td><p>Die Momentaufnahme Sitzung ist ungültig, oder der grbit-Parameter ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird die Momentaufnahme Sitzung beendet, und das normale Engine-Verhalten wird fortgesetzt. Eine neue Momentaufnahme Sitzung kann zu einem späteren Zeitpunkt gestartet werden.

Wenn diese Funktion fehlschlägt, wird die Momentaufnahme Sitzung nicht abgebrochen.

#### <a name="remarks"></a>Bemerkungen

Diese Funktion sollte anstelle von [jedessnapshotthaw](./jetossnapshotthaw-function.md) aufgerufen werden, um die Engine darüber zu informieren, dass die Momentaufnahme aus Gründen, die nicht mit der Engine in Beziehung stehen, abgebrochen wurde. Diese Informationen können später verwendet werden, um Ereignisprotokoll Meldungen über die Momentaufnahme Sitzung auszugeben oder um andere geeignete Aktionen zu bestimmen.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[Jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md)  
[Jejessnapshotprepare](./jetossnapshotprepare-function.md)  
[Jejessnapshotthaw](./jetossnapshotthaw-function.md)
