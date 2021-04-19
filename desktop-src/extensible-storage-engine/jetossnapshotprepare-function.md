---
description: 'Weitere Informationen finden Sie hier: jejessnapshotprepare-Funktion'
title: JetOSSnapshotPrepare-Funktion
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364101"
---
# <a name="jetossnapshotprepare-function"></a>JetOSSnapshotPrepare-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotprepare-function"></a>JetOSSnapshotPrepare-Funktion

Die **jedessnapshotprepare** -Funktion beginnt die Vorbereitung für eine Momentaufnahme Sitzung. Eine Momentaufnahme Sitzung ist ein kurzes Zeitintervall, in dem die Engine keine Schreibvorgänge auf dem Datenträger ausgibt, sodass die Engine an einer volumemomentaufnahmensitzung teilnehmen kann (wenn Sie von einem Momentaufnahme-Writer gesteuert wird).

**Windows XP:**  **jedessnapshotprepare** wurde in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*psnapid*

Der Bezeichner der Momentaufnahme Sitzung, die gestartet werden soll.

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
<td><p>0</p></td>
<td><p>Normale Momentaufnahme.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIncrementalSnapshot</p></td>
<td><p>Es werden nur Protokolldateien erstellt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCopySnapshot</p></td>
<td><p>Eine Kopier Momentaufnahme (normal oder inkrementell) ohne Protokoll abkürzen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitContinueAfterThaw</p></td>
<td><p>Die Momentaufnahme Sitzung tritt nach <a href="gg269229(v=exchg.10).md">jeto ssnapshotthaw</a> auf und erfordert einen <a href="gg294136(v=exchg.10).md">jedessnapshotend</a> -Funktions Aufruf.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitExplicitPrepare</p></td>
<td><p>Standardmäßig werden keine Instanzen vorbereitet.</p>
<p><strong>Windows 7:</strong>  JET_bitExplicitPrepare wurde in Windows 7 eingeführt.</p></td>
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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Der Momentaufnahme-ID-Zeiger ist NULL, oder der <em>grbit</em> -Parameter ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Eine Momentaufnahme Sitzung wird bereits ausgeführt, und der Vorgang darf nicht mehr als eine Momentaufnahme Sitzung zu einem bestimmten Zeitpunkt aufweisen.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, kann eine Momentaufnahme Sitzung jederzeit mit der e/a-Sperr Phase gestartet werden. Der Bezeichner für die Sitzung wird zurückgegeben und muss in den nachfolgenden Aufrufen für die Momentaufnahme Sitzung verwendet werden.

Die laufenden Instanzen der Engine werden nun als Teil der Momentaufnahme Sitzung betrachtet.

**Windows Vista:**  Um eine andere Teilmenge von Instanzen anzugeben, kann die [jechanssnapshotprepareinstance](./jetossnapshotprepareinstance-function.md) aufgerufen werden.

Der reguläre API-Sequenz Aufruf lautet: **jedessnapshotprepare**, optional gefolgt von einem oder mehreren Aufrufen von [jedessnapshotprepareinstance](./jetossnapshotprepareinstance-function.md)und anschließendem [jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md). Nachdem das Einfrieren gestartet wurde, kann es mit [jeto ssnapshotthaw](./jetossnapshotthaw-function.md)beendet werden. Nach der Vorbereitung kann die Momentaufnahme Sitzung jederzeit mit [jedessnapshotabort](./jetossnapshotabort-function.md)beendet werden.

Wenn JET_bitContinueAfterThaw nach [jedessnapshotthaw](./jetossnapshotthaw-function.md)angegeben wird, bleibt die Momentaufnahme Sitzung erhalten (obwohl die e/a-Vorgänge fortgesetzt werden). Dadurch wird die Momentaufnahme überprüft, und bei Bedarf wird die Protokoll Verkürzung mithilfe von [jetossnapshottruneurelog](./jetossnapshottruncatelog-function.md) aktiviert, und es wird ein Anruf von [jetossnapshotend](./jetossnapshotend-function.md)benötigt.

Wenn diese Funktion fehlschlägt, erfolgt keine Änderung des Engine-Zustands.

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
[Jeto ssnapshotend](./jetossnapshotend-function.md)  
[Jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md)  
[Jejessnapshotprepareingestance](./jetossnapshotprepareinstance-function.md)  
[Jejessnapshotthaw](./jetossnapshotthaw-function.md)  
[Jeto ssnapshottruneurelog](./jetossnapshottruncatelog-function.md)
