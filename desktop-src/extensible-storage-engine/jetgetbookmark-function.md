---
description: 'Weitere Informationen: jetgetbookmark-Funktion'
title: Jetgetbookmark-Funktion
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131961"
---
# <a name="jetgetbookmark-function"></a>Jetgetbookmark-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetbookmark-function"></a>Jetgetbookmark-Funktion

Die **jetgetbookmark** -Funktion Ruft das Lesezeichen für den Datensatz ab, der mit dem Index Eintrag an der aktuellen Position eines Cursors verknüpft ist. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von [jetgobackbookmark](./jetgotobookmark-function.md)wieder in denselben Datensatz zu positionieren.

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*pvbookmark*

Der Ausgabepuffer, der das Lesezeichen empfängt.

*cbmax*

Die maximale Größe des Ausgabepuffers in Bytes.

*pcbactual*

Die tatsächliche Größe (in Bytes) des Lesezeichens.

Wenn dieser Parameter **null** ist, wird die tatsächliche Größe des Lesezeichens nicht zurückgegeben.

Wenn der Ausgabepuffer zu klein ist, wird die tatsächliche Größe des Lesezeichens weiterhin zurückgegeben. Dies bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.

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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um das ganze Lesezeichen zu erhalten. Der Ausgabepuffer wurde mit dem Umfang des Lesezeichens aufgefüllt, das passt. Die tatsächliche Größe des Lesezeichens wurde auch zurückgegeben, wenn dies angefordert wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</p>
<p><strong>Windows XP:  </strong> Diese Rückgabewerte werden in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor ist nicht in einem Datensatz positioniert. Dafür sind viele verschiedene Gründe möglich. Dies ist beispielsweise der Fall, wenn der Cursor nach dem letzten Datensatz im aktuellen Index positioniert wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird das Lesezeichen für den Datensatz, der dem Index Eintrag an der aktuellen Position eines Cursors zugeordnet ist, im Ausgabepuffer zurückgegeben. Es erfolgt keine Änderung des Daten Bank Status.

Wenn diese Funktion fehlschlägt, werden der Status des Ausgabepuffers und die tatsächliche Größe des Lesezeichens nur dann definiert, wenn JET_errBufferTooSmall zurückgegeben wurde. Wenn JET_errBufferTooSmall zurückgegeben wird, enthält der Ausgabepuffer den Teil des Lesezeichens, der in den bereitgestellten Bereich passt, und die tatsächliche Größe des Lesezeichens ist genau. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Lesezeichen sollten im Allgemeinen als nicht transparente Datenblöcke behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Allerdings gelten für alle ESENT-Lesezeichen die folgenden Bedingungen:

  - Ein Lesezeichen identifiziert eindeutig einen Datensatz in einer bestimmten Tabelle.

  - Das Lesezeichen eines Datensatzes ändert sich nicht für die Lebensdauer dieses Datensatzes.

  - Das Lesezeichen eines Datensatzes entspricht dem Schlüssel dieses Datensatzes auf dem primären Index für die Tabelle, die diesen Datensatz enthält. Wenn kein primärer Index für diese Tabelle definiert wird, erstellt die Datenbank-Engine ein eigenes Lesezeichen für den Datensatz.

  - Lesezeichen können miteinander verglichen werden, indem die [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) -Funktion verwendet wird, um ihre relative Reihenfolge im primären Index für die Tabelle der Quelldaten Sätze festzulegen. Wenn kein primärer Index für diese Tabelle definiert ist, ist es nicht sinnvoll, die relative Reihenfolge von Lesezeichen aus dieser Tabelle zu verwenden.

  - Es ist bedeutungslos, Lesezeichen von Datensätzen aus unterschiedlichen Tabellen miteinander zu vergleichen.

  - Ein Lesezeichen ist vor Windows Vista immer kleiner oder gleich JET_cbBookmarkMost (256) Bytes.
    
**Windows Vista:** In Windows Vista und späteren Versionen können Lesezeichen größer als JET_cbBookmarkMost (256) Bytes sein. Die maximale Größe eines Lesezeichens ist gleich dem aktuellen Wert von JET_paramKeyMost + 1.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetgojebookmark](./jetgotobookmark-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
