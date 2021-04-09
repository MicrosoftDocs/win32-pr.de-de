---
description: 'Weitere Informationen zu: jethssnapshotthaw-Funktion'
title: Jejessnapshotthaw-Funktion
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da7d5037cfc6b9a5f001dede57581127e4de60b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868940"
---
# <a name="jetossnapshotthaw-function"></a>Jejessnapshotthaw-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotthaw-function"></a>Jejessnapshotthaw-Funktion

Die **jedessnapshotthaw** -Funktion benachrichtigt die Engine, dass Sie normale e/a-Vorgänge nach einem Sperr Zeitraum und einer erfolgreichen Momentaufnahme wieder aufnehmen kann.

**Windows XP:**  **jedessnapshotthaw** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapid*

Der Bezeichner der Momentaufnahme Sitzung.

*grbit*

Dieser Parameter ist für die zukünftige Verwendung reserviert, und der einzige gültige Wert ist 0.

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
<td><p>Die Momentaufnahme Sitzung ist ungültig, oder der <em>grbit</em> -Parameter ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut</p></td>
<td><p>In der Momentaufnahme Sitzung war vor dem Auftreten dieses Aufrufes ein internes Timeout aufgetreten. Folglich werden e/a-Vorgänge vor dem Ausführen dieses Aufrufes normal zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird eine Momentaufnahme Sitzung beendet, und das normale Engine-Verhalten wird fortgesetzt. Eine neue Momentaufnahme Sitzung kann später gestartet werden.

Wenn diese Funktion fehlschlägt, wird die aktuelle Momentaufnahme Sitzung beendet, aber das Einfrieren von IOS während des Momentaufnahme Zeitraums wurde intern nicht berücksichtigt.

#### <a name="remarks"></a>Bemerkungen

Ereignisprotokoll Einträge werden für die verschiedenen Schritte der Momentaufnahme generiert.

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
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[Jejessnapshotabort](./jetossnapshotabort-function.md)  
[Jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md)  
[Jejessnapshotprepare](./jetossnapshotprepare-function.md)
