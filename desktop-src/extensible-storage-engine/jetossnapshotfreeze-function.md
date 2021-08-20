---
description: 'Weitere Informationen finden Sie unter: JetOSSnapshotFreeze-Funktion'
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
ms.openlocfilehash: 2c524d9067441bb2d9077a9a1751f4910a47f031f4e28701fe204f70c9c5b3e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118072234"
---
# <a name="jetossnapshotfreeze-function"></a>JetOSSnapshotFreeze-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotfreeze-function"></a>JetOSSnapshotFreeze-Funktion

Die **JetOSSnapshotFreeze-Funktion** startet eine Momentaufnahme. Während die Momentaufnahme in Bearbeitung ist, kann keine Schreib-auf-Datenträger-Aktivität durch die Engine stattfinden.

**Windows XP:****JetOSSnapshotFreeze** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapId*

Der Bezeichner der Momentaufnahmesitzung.

*pcInstanceInfo*

Die Anzahl der derzeit in der Engine ausgeführten Instanzen, die Teil der Momentaufnahmesitzung sind.

*paInstanceInfo*

Ein Array von -Strukturen, eine für jede ausgeführte Instanz, die Teil der Momentaufnahmesitzung ist, die die Instanz und die Datenbanken beschreibt, die teil davon sind.

*grbit*

Die Optionen für diesen Aufruf. Dieser Parameter ist für die zukünftige Verwendung reserviert, und der einzige unterstützte gültige Wert ist 0.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Die für die Ausgabeparameter bereitgestellten Zeiger sind NULL, die Momentaufnahmesitzung ist ungültig, oder der <em>grbit-Parameter</em> ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Die Momentaufnahmesitzung befindet sich nicht im entsprechenden Zustand, um ein Einfrieren zu starten (z. B. ist bei dieser Sitzung zuvor ein vorheriger Einfrieren fehlgeschlagen).</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed</p></td>
<td><p>Die Engine befindet sich nicht in einem Zustand, in dem eine Momentaufnahme ausgeführt werden kann. Mindestens eine Streamingsicherung wird bereits ausgeführt, oder eine oder mehrere Instanzen werden wiederherstellungsschritte ausgeführt oder werden beendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Der Bezeichner für die Momentaufnahmesitzung ist ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Fehler bei der Funktion aufgrund einer nicht genügenden Arbeitsspeicherbedingung.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads</p></td>
<td><p>Fehler bei der Funktion, weil ein neuer Thread, der das Einfrieren durchfing, nicht gestartet werden konnte.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ist, werden keine Schreib-IOs für die Datenbankdateien oder die Protokolldateien ausgegeben, die Teil von instanzen sind, die fixiert sind. Außerdem werden die Instanzinformationen ordnungsgemäß ausgefüllt und müssen später durch Aufrufen von [JetFreeBuffer](./jetfreebuffer-function.md) mit dem Zeiger auf das zurückgegebene Instanzinformationsarray frei werden.

Wenn diese Funktion fehlschlägt, wird die Engine weiterhin normal ausgeführt, während die E/A-Vorgänge wie gewohnt ausgeführt werden. Es ist nicht notwendig, [JetOSSnapshotThaw aufrufen,](./jetossnapshotthaw-function.md) wenn beim Einfrieren ein Fehler auftritt. Außerdem werden die Instanzinformationen nicht ausgefüllt, sodass diese Ressource nicht frei werden muss.

#### <a name="remarks"></a>Hinweise

Während des Einfrierenzeitraums werden keine Schreib-E/A-Dateien für die angefügten Datenbanken oder Transaktionsprotokolle ausgegeben, obwohl möglicherweise Schreib-E/A-Dateien für die temporären Datenbanken oder Streamingdateien ausgegeben werden.

Der Zustand, in dem sich die Datenbanken und die Protokolldateien während des Einfrierens befinden (der Zustand, in dem sich die Dateien in einem Volumemomentaufnahme-Image befinden), ist so, dass eine normale Wiederherstellung möglich ist, wenn diese Dateien später wiederhergestellt werden.

Da während des Einfrierens keine Schreibvorgänge ausgeführt werden, werden normale API-Aufrufe an die Engine für dieses Intervall möglicherweise nicht mehr ausgeführt. Die Clientanwendung muss API-Aufrufe verarbeiten können, die möglicherweise länger dauern als normal, wenn ein Einfrieren auftritt.

Aufgrund der oben beschriebenen möglichen Auswirkungen gibt es ein internes Timeout, nach dem die Momentaufnahmesitzung die Einfrierenphase beendet, auch wenn die APIs, die das Aufsperren oder Abbrechen tun, nicht aufgerufen wurden. Der Wert des Timeouts kann mithilfe des JET_paramOSSnapshotTimeout [geändert](./backup-and-restore-parameters.md) werden. Beachten Sie, dass das typische Einfrierenintervall im Bereich von 10 Sekunden liegt und das Standardzeitüberschreitungsintervall ungefähr 60 Sekunden beträgt.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>JetOSSnapshotFreezeW</strong> (Unicode) und <strong>JetOSSnapshotFreezeA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
