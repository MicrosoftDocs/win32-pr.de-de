---
description: Weitere Informationen finden Sie in der jeto ssnapshotfreeze-Funktion
title: JetOSSnapshotFreeze-Funktion
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217235"
---
# <a name="jetossnapshotfreeze-function"></a>JetOSSnapshotFreeze-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotfreeze-function"></a>JetOSSnapshotFreeze-Funktion

Die **jeesssnapshotfreeze** -Funktion startet eine Momentaufnahme. Während der Momentaufnahme kann keine Aktivität zum Schreiben von Datenträgern durch die Engine durchgeführt werden.

**Windows XP:**  **jedessnapshotfreeze** wurde in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapid*

Der Bezeichner der Momentaufnahme Sitzung.

*pcinstanceingefo*

Die Anzahl der Instanzen, die zurzeit in der-Engine ausgeführt werden und Teil der Momentaufnahme Sitzung sind.

*painstanceingefo*

Ein Array von-Strukturen, eines für jede laufende Instanz, die Teil der Momentaufnahme Sitzung ist, und beschreibt die Instanz und die Datenbanken, die Teil davon sind.

*grbit*

Die Optionen für diesen-Befehl. Dieser Parameter ist für die zukünftige Verwendung reserviert, und der einzige gültige Wert ist 0.

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
<td><p>Die Zeiger, die für die Ausgabeparameter bereitgestellt werden, sind NULL, die Momentaufnahme Sitzung ist ungültig, oder der <em>grbit</em> -Parameter ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Die Momentaufnahme Sitzung befindet sich nicht im entsprechenden Zustand, um ein Einfrieren zu starten (z. b. ist ein vorheriger Einfrieren für diese Sitzung zuvor fehlgeschlagen).</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed</p></td>
<td><p>Die Engine befindet sich nicht in einem Zustand, in dem eine Momentaufnahme ausgeführt werden kann. Mindestens eine Streamingsicherung wird bereits ausgeführt, oder eine oder mehrere Instanzen durchlaufen Wiederherstellungsschritte oder beenden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Die Funktion konnte aufgrund einer nicht genügend Arbeitsspeicher Bedingung nicht ausgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads</p></td>
<td><p>Die Funktion ist fehlgeschlagen, da ein neuer Thread, der die Sperrung durchgeführt hat, nicht gestartet</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, werden keine Schreibvorgänge für die Datenbankdateien oder die Protokolldateien ausgeführt, die Bestandteil der fixierten Instanzen sind. Außerdem werden die Instanzinformationen ordnungsgemäß ausgefüllt und müssen später freigegeben werden, indem [jetfrebuffer](./jetfreebuffer-function.md) mit dem Zeiger auf das zurückgegebene instanzinformationsarray aufgerufen wird.

Wenn diese Funktion fehlschlägt, wird die Engine weiterhin normal ausgeführt, und die IOS-Funktion wird wie gewohnt ausgeführt. Wenn das Einfrieren fehlschlägt, muss [jedessnapshotthaw](./jetossnapshotthaw-function.md) aufgerufen werden. Außerdem werden die Instanzinformationen nicht aufgefüllt, sodass es nicht erforderlich ist, diese Ressource freizugeben.

#### <a name="remarks"></a>Bemerkungen

Während des Sperr Zeitraums werden keinerlei Schreib-e/a-Vorgänge für die angefügten Datenbanken oder die Transaktionsprotokolle ausgegeben, es kann jedoch sein, dass für die temporären Datenbanken oder Streamingdateien Schreibvorgänge für IOS ausgegeben werden.

Der Zustand, in dem sich die Datenbanken und die Protokolldateien während des Fixierens befinden (der Zustand, in dem sich die Dateien in einem Volumesnapshot-Image befinden) so, dass eine normale Wiederherstellung möglich ist, wenn diese Dateien später wieder hergestellt werden.

Da während des Sperr Zeitraums keine Schreibvorgänge vorhanden sind, können normale API-Aufrufe in der Engine für dieses Intervall angehalten werden. Die Client Anwendung muss in der Lage sein, API-Aufrufe zu verarbeiten, die möglicherweise länger dauern, wenn ein Einfrieren auftritt.

Aufgrund der oben beschriebenen möglichen Auswirkungen gibt es einen internen Timeout, nach dem die Momentaufnahme Sitzung die Freeze-Phase beendet, auch wenn die APIs, die den reaktivieren oder Abbruch durchgeführt haben, nicht aufgerufen wurden. Der Wert des Timeouts kann mit dem [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) System-Parameter geändert werden. Beachten Sie, dass sich das typische Sperr Intervall im Bereich von 10 Sekunden mit dem Standard Timeout von ungefähr 60 Sekunden befindet.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jeumssnapshotfrezew</strong> (Unicode) und <strong>jeto ssnapshotfrezea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[Jejessnapshotabort](./jetossnapshotabort-function.md)  
[Jejessnapshotprepare](./jetossnapshotprepare-function.md)  
[Jejessnapshotprepareingestance](./jetossnapshotprepareinstance-function.md)  
[Jejessnapshotthaw](./jetossnapshotthaw-function.md)
