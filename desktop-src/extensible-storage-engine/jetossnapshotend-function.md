---
description: Weitere Informationen finden Sie in der Funktion "jeto ssnapshotend".
title: Jeto ssnapshotend-Funktion
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128169"
---
# <a name="jetossnapshotend-function"></a>Jeto ssnapshotend-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotend-function"></a>Jeto ssnapshotend-Funktion

Die **jedessnapshotend** -Funktion benachrichtigt die Engine, dass die Momentaufnahme Sitzung abgeschlossen wurde.

**Windows Vista:**  **jedessnapshotend** wird in Windows Vista eingeführt:.

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
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
<td><p>0</p></td>
<td><p>Das erfolgreiche Ende der Momentaufnahme Sitzung.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitAbortSnapshot</p></td>
<td><p>Die Momentaufnahme Sitzung wurde abgebrochen.</p></td>
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
<td><p>Eine der angeforderten Optionen ist ungültig, wird falsch oder nicht implementiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Eine Momentaufnahme Sitzung wird bereits ausgeführt. Dies ist nicht zulässig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut</p></td>
<td><p>In der Momentaufnahme Sitzung war vor dem Auftreten dieses Aufrufes ein internes Timeout aufgetreten. Folglich werden die e/a-Vorgänge vor dem Auftreten dieses Aufrufes normal zurückgegeben.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird eine Momentaufnahme Sitzung abgeschlossen, und das normale Engine-Verhalten wird fortgesetzt. Eine neue Momentaufnahme Sitzung kann später gestartet werden.

Wenn diese Funktion fehlschlägt, gibt der JET_errOSSnapshotTimeOut Rückgabecode zurück, und die aktuelle Momentaufnahme Sitzung wird beendet, aber das Einfrieren von IOS während des Momentaufnahme Zeitraums wurde intern nicht berücksichtigt. Bei allen anderen Fehlern wird der Sitzungs Status der Momentaufnahme nicht geändert.

#### <a name="remarks"></a>Bemerkungen

Diese Funktion wird nur aufgerufen, wenn [jeto ssnapshotthaw](./jetossnapshotthaw-function.md) mit JET_bitContinueAfterThaw aufgerufen wurde.

Die Momentaufnahme Sitzung muss fertiggestellt werden, damit die Momentaufnahme Überprüfung und das Abschneiden des Protokolls stattfinden. Ereignisprotokoll Einträge werden für die verschiedenen Schritte der Momentaufnahme generiert.

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
[Jejessnapshotthaw](./jetossnapshotthaw-function.md)
