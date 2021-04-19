---
description: 'Weitere Informationen zu: jeesssnapshottruneurelog-Funktion'
title: Jeto ssnapshottruneurelog-Funktion
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364152"
---
# <a name="jetossnapshottruncatelog-function"></a>Jeto ssnapshottruneurelog-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshottruncatelog-function"></a>Jeto ssnapshottruneurelog-Funktion

Die **jetossnapshottruneurelog** -Funktion ermöglicht das Abschneiden von Protokollen für alle Instanzen, die Teil der Momentaufnahme Sitzung sind.

**Windows Vista:**  **jedessnapshottruneurelog** wird in Windows Vista eingeführt.

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapid*

Der Bezeichner der Momentaufnahme Sitzung.

*grbit*

Die Optionen für diesen-Befehl. Dieser Parameter kann eine Kombination der folgenden Werte aufweisen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitAllDatabasesSnapshot</p></td>
<td><p>Alle Datenbanken werden angefügt, sodass die Speicher-Engine die Protokoll Verkürzung berechnen und durchführen kann.</p></td>
</tr>
<tr class="even">
<td><p>0 (null)</p></td>
<td><p>Es erfolgt kein abschneiden.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Der <em>grbit</em> -Parameter ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Die Momentaufnahme Sitzung befindet sich nicht in dem Status, in dem ein Abschneiden erfolgen kann. Mögliche Ursachen sind:</p>
<ul>
<li><p>der-Vorgang erfolgt nach dem Timeout der Momentaufnahme Sitzung.</p></li>
<li><p>die Sitzung wurde als Kopier Momentaufnahme angegeben.</p></li>
</ul></td>
</tr>
</tbody>
</table>


Bei Erfolg werden die Protokolldateien für eine oder alle Instanzen, die Teil der Momentaufnahme Sitzung sind, nach Möglichkeit abgeschnitten.

#### <a name="remarks"></a>Bemerkungen

Diese Funktion sollte nur aufgerufen werden, wenn die Momentaufnahme mit der JET_bitContinueAfterThaw-Option erstellt wurde. Andernfalls würde die Momentaufnahme Sitzung nach dem [jedessnapshotthaw](./jetossnapshotthaw-function.md) -Befehl beendet werden.

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
[Jeto ssnapshotend](./jetossnapshotend-function.md)  
[Jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md)  
[Jejessnapshotprepare](./jetossnapshotprepare-function.md)  
[Jejessnapshotthaw](./jetossnapshotthaw-function.md)
