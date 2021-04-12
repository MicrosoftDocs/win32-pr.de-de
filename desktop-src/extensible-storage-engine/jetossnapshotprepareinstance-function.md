---
description: 'Weitere Informationen finden Sie hier: jeum-Funktion'
title: Jeto ssnapshotprepareingestance-Funktion
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
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104394282"
---
# <a name="jetossnapshotprepareinstance-function"></a>Jeto ssnapshotprepareingestance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotprepareinstance-function"></a>Jeto ssnapshotprepareingestance-Funktion

Die **jedessnapshotprepareinstance** -Funktion wählt eine bestimmte Instanz aus, die Teil der Momentaufnahme Sitzung sein soll.

**Windows Vista:** **jedessnapshotprepareinstance** wurde in Windows Vista eingeführt.

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*snapid*

Der Bezeichner der Momentaufnahme Sitzung.

*lichen*

Die-Instanz, die für diesen-Befehl verwendet wird.

*grbit*

Die Optionen für diesen-Befehl. Dieser Parameter ist für die zukünftige Verwendung reserviert. Der einzige gültige Wert ist 0 (null).

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
<td><p>Der Momentaufnahme-ID-Zeiger ist <strong>null</strong> , oder der <em>grbit</em> -Parameter ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Eine Momentaufnahme Sitzung wird bereits ausgeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, ist die angegebene Instanz Teil der Momentaufnahme Sitzung.

Wenn diese Funktion fehlschlägt, erfolgt keine Änderung des Engine-Zustands.

#### <a name="remarks"></a>Bemerkungen

Der reguläre API-Sequenz Aufruf lautet: [jedessnapshotprepare](./jetossnapshotprepare-function.md), optional gefolgt von einem oder mehreren Aufrufen von **jedessnapshotprepareinstance** und anschließendem [jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md). Nachdem das Einfrieren gestartet wurde, kann es mit [jeto ssnapshotthaw](./jetossnapshotthaw-function.md)beendet werden. Nach der Vorbereitung kann die Momentaufnahme Sitzung jederzeit mit [jedessnapshotabort](./jetossnapshotabort-function.md)beendet werden. Ereignisprotokoll Einträge werden für die verschiedenen Schritte der Momentaufnahme generiert.

Wenn **jedessnapshotprepareinstance** zwischen dem Start der Sitzung ([jedessnapshotprepare](./jetossnapshotprepare-function.md)) und dem Freeze-Moment ([jedessnapshotfreeze](./jetossnapshotfreeze-function.md)) nicht aufgerufen wird, werden alle derzeit in der Engine laufenden Instanzen fixiert und in die Momentaufnahme Sitzung aufgenommen. Dies geschieht aus zwei Gründen:

  - Der Code für Benutzer, die alle Instanzen wünschen, wird vereinfacht.

  - Sie ermöglicht die Abwärtskompatibilität für die Aufrufer der Momentaufnahme-APIs.

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

[Fehler Behandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Speicher-Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[Jejessnapshotabort](./jetossnapshotabort-function.md)  
[Jeto ssnapshotend](./jetossnapshotend-function.md)  
[Jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md)  
[Jejessnapshotprepare](./jetossnapshotprepare-function.md)  
[Jejessnapshotthaw](./jetossnapshotthaw-function.md)
