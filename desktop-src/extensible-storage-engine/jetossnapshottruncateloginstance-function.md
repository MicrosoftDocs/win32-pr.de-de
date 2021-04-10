---
description: 'Weitere Informationen finden Sie hier: jejessnapshottruneureloginstance-Funktion'
title: Jejessnapshottruneureloginstance-Funktion
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cef30d012c28c809bb35d59a82fd596ba69bd175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749704"
---
# <a name="jetossnapshottruncateloginstance-function"></a>Jejessnapshottruneureloginstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshottruncateloginstance-function"></a>Jejessnapshottruneureloginstance-Funktion

Die **jetossnapshottruneureloginstance** -Funktion verkürzt das Protokoll für eine angegebene Instanz während einer Momentaufnahme Sitzung.

**Windows Vista:**  **jedessnapshottruneureloginstance** wird in Windows Vista eingeführt.

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
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

Die Optionen für diesen-Befehl. Dieser Parameter kann eine Kombination der folgenden Werte aufweisen.

bei *grbit* kann es sich um einen der folgenden Werte handeln:

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
<li><p>Der-Vorgang wird abgeschlossen, nachdem die Momentaufnahme Sitzung abgelaufen ist.</p></li>
<li><p>Die Sitzung wurde als Kopier Momentaufnahme angegeben.</p></li>
</ul></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, werden die Protokolldateien für eine oder alle Instanzen, die Teil der Momentaufnahme Sitzung sind, nach Möglichkeit abgeschnitten.

#### <a name="remarks"></a>Bemerkungen

Diese Funktion sollte nur aufgerufen werden, wenn die Momentaufnahme mit der JET_bitContinueAfterThaw-Option erstellt wurde. Andernfalls wird die Momentaufnahme Sitzung nach dem Rückruf von [jedessnapshotthaw](./jetossnapshotthaw-function.md)beendet.

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
