---
description: Weitere Informationen finden Sie unter JetOSSnapshotAbort-Funktion.
title: JetOSSnapshotAbort-Funktion
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
ms.openlocfilehash: 70f4a7cc3db5b5c6ef90c59de05cd9c0acea9d1dfb4ac1eeeba119ded5e89c14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559810"
---
# <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort-Funktion

Die **JetOSSnapshotAbort-Funktion** benachrichtigt die Engine, dass sie normale E/A-Vorgänge fortsetzen kann, nachdem ein Einfrierenzeitraum mit einer fehlerhaften Momentaufnahme beendet wurde.

**Windows Server 2003:****JetOSSnapshotAbort** wird in Windows Server 2003 eingeführt.  

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapId*

Der Bezeichner der Momentaufnahmesitzung.

*grbit*

Die Optionen für diesen Aufruf. Dieser Parameter ist für die zukünftige Verwendung reserviert, und der einzige unterstützte gültige Wert ist 0 (null).

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
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Die Momentaufnahmesitzung ist ungültig, oder der grbit-Parameter ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Der Bezeichner für die Momentaufnahmesitzung ist ungültig.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ist, wird die Momentaufnahmesitzung beendet, und das normale Engine-Verhalten wird fortgesetzt. Eine neue Momentaufnahmesitzung kann zu einem späteren Zeitpunkt gestartet werden.

Wenn diese Funktion fehlschlägt, wird die Momentaufnahmesitzung nicht abgebrochen.

#### <a name="remarks"></a>Hinweise

Diese Funktion sollte anstelle von [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) aufgerufen werden, um die Engine darüber zu informieren, dass die Momentaufnahme aus Gründen abgebrochen wurde, die sich nicht auf die Engine beziehen. Diese Informationen können später verwendet werden, um Ereignisprotokollmeldungen zur Momentaufnahmesitzung ausausgaben oder andere geeignete Aktionen zu bestimmen.

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
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
