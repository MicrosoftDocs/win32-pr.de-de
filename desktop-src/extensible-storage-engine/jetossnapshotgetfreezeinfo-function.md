---
description: 'Weitere Informationen finden Sie in den folgenden Informationen: jejessnapshotgetfrezeinfo-Funktion'
title: Jejessnapshotgetfrezeinfo-Funktion
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fbfd3fb31567ea73b8266b5aeba506d62be7714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352436"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a>Jejessnapshotgetfrezeinfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotgetfreezeinfo-function"></a>Jejessnapshotgetfrezeinfo-Funktion

Die **jedessnapshotgetfrezeinfo** -Funktion Ruft die Liste der Instanzen und Datenbanken ab, die zu einem beliebigen Zeitpunkt Teil der Momentaufnahme Sitzung sind.

**Windows Vista:**  **jedessnapshotgetfrezeinfo** wird in Windows Vista eingeführt.

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapid*

Der Bezeichner der Momentaufnahme Sitzung, die gestartet werden soll.

*pcinstanceingefo*

Die Anzahl der Instanzen, die zurzeit ausgeführt werden und Teil der Momentaufnahme Sitzung sind.

*painstanceingefo*

Ein Array von-Strukturen, eines für jede laufende Instanz, das die Instanz und die darin vorhandenen Datenbanken beschreibt.

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>Die Funktion konnte aufgrund einer nicht genügend Arbeitsspeicher Bedingung nicht ausgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p><em>pcinstanceingefo</em> oder <em>painstanceingefo</em> ist <strong>null</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Eine Momentaufnahme Sitzung wird nicht ausgeführt.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, werden die Instanzinformationen ordnungsgemäß ausgefüllt und müssen später freigegeben werden, indem [jetfrebuffer](./jetfreebuffer-function.md) mit dem Zeiger auf das zurückgegebene instanzinformationsarray aufgerufen wird.

Wenn diese Funktion fehlschlägt, erfolgt keine Änderung des Engine-Zustands.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jeumssnapshotgetfrezeinfow</strong> (Unicode) und <strong>jeto ssnapshotgetfrezeinfoa</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Fehler Behandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Speicher-Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[Jetfrebuffer](./jetfreebuffer-function.md)  
[Jejessnapshotabort](./jetossnapshotabort-function.md)  
[Jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md)  
[Jejessnapshotthaw](./jetossnapshotthaw-function.md)
