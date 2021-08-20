---
description: 'Weitere Informationen finden Sie unter: JetOSSnapshotPrepareInstance-Funktion'
title: JetOSSnapshotPrepareInstance-Funktion
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfd4fc15f3ea7d4f6275f0d4dd31ed96729715b6089397fff7ee73fc7d0c6e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614934"
---
# <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance-Funktion

Die **JetOSSnapshotPrepareInstance-Funktion** wählt eine bestimmte Instanz aus, die Teil der Momentaufnahmesitzung sein soll.

**Windows Vista:** **JetOSSnapshotPrepareInstance** wurde in Windows Vista eingeführt.

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*snapId*

Der Bezeichner der Momentaufnahmesitzung.

*Instanz*

Die -Instanz, die für diesen Aufruf verwendet wird.

*grbit*

Die Optionen für diesen Aufruf. Dieser Parameter ist für die zukünftige Verwendung reserviert. Der einzige gültige Wert ist 0 (null).

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
<td><p>Der Momentaufnahme-ID-Zeiger <strong>ist NULL,</strong> oder der <em>grbit-Parameter</em> ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Eine Momentaufnahmesitzung wird bereits erstellt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Der Bezeichner für die Momentaufnahmesitzung ist ungültig.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ist, ist die angegebene Instanz Teil der Momentaufnahmesitzung.

Wenn diese Funktion fehlschlägt, erfolgt keine Änderung des Engine-Zustands.

#### <a name="remarks"></a>Hinweise

Der normale API-Sequenzaufruf [ist: JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), optional gefolgt von einem oder mehr Aufrufen von **JetOSSnapshotPrepareInstance**, gefolgt von [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Nachdem der Einfrieren gestartet wurde, kann er mit [JetOSSnapshotThaw beendet werden.](./jetossnapshotthaw-function.md) Nach der Vorbereitung kann die Momentaufnahmesitzung mit [JetOSSnapshotAbort](./jetossnapshotabort-function.md)jederzeit plötzlich beendet werden. Ereignisprotokolleinträge werden für die verschiedenen Schritte der Momentaufnahme generiert.

Wenn **JetOSSnapshotPrepareInstance** zwischen dem Start der Sitzung ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) und dem Fix-Moment ([JetOSSnapshotFreeze)](./jetossnapshotfreeze-function.md)nicht aufgerufen wird, frieren alle ausgeführten Instanzen in der Engine ein und werden Teil der Momentaufnahmesitzung. Dies hat zwei Gründe:

  - Sie vereinfacht den Code für Benutzer, die alle Instanzen wünschen.

  - Sie ermöglicht Abwärtskompatibilität für die Aufrufer der Momentaufnahme-APIs.

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
<td><p>Erfordert Windows Server 2008.</p></td>
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

[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Storage Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
