---
description: 'Weitere Informationen: jetgetsecondaryindexbookmark-Funktion'
title: Jetgetsecondaryindexbookmark-Funktion
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d86b875037982a18ebb9d488c3a05b3123002b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358509"
---
# <a name="jetgetsecondaryindexbookmark-function"></a>Jetgetsecondaryindexbookmark-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetsecondaryindexbookmark-function"></a>Jetgetsecondaryindexbookmark-Funktion

Die **jetgetsecondaryindexbookmark** -Funktion Ruft ein spezielles Lesezeichen für den sekundären Index Eintrag an der aktuellen Position eines Cursors ab. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von [jetgoysecondaryindexbookmark](./jetgotosecondaryindexbookmark-function.md)effizient wieder in denselben Index Eintrag zu positionieren. Dies ist besonders nützlich, wenn Sie einen sekundären Index neu positionieren, der doppelte Schlüssel enthält oder mehrere Indexeinträge für denselben Datensatz enthält.

**Windows XP: jetgetsecondaryindexbookmark** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*pvsecondarykey*

Der Ausgabepuffer, der den sekundären Schlüssel empfängt.

*cbsecondarykeymax*

Die maximale Größe (in Bytes) des Ausgabepuffers für den sekundären Schlüssel.

*pcbsecondarykeyactual*

Empfängt die tatsächliche Größe des sekundären Schlüssels in Bytes.

Wenn dieser Parameter NULL ist, wird die tatsächliche Größe des sekundären Schlüssels nicht zurückgegeben.

Wenn der Ausgabepuffer zu klein ist, wird die tatsächliche Größe des sekundären Schlüssels weiterhin zurückgegeben. Dies bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.

*pvprimarybookmark*

Der Ausgabepuffer, der das Primärschlüssel-Lesezeichen empfängt.

*cbprimarybookmarkmax*

Die maximale Größe (in Bytes) des Ausgabepuffers für das Primärschlüssel-Lesezeichen.

*pcbprimarykeyactual*

Empfängt die tatsächliche Größe (in Bytes) des Primärschlüssel-Lesezeichens.

Wenn dieser Parameter NULL ist, wird die tatsächliche Größe des Primärschlüssel-Lesezeichens nicht zurückgegeben.

Wenn der Ausgabepuffer zu klein ist, wird die tatsächliche Größe des Primärschlüssel-Lesezeichens weiterhin zurückgegeben. Dies bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.

*grbit*

Für die zukünftige Verwendung reserviert.

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
<td><p>Der Vorgang wurde erfolgreich abgeschlossen, aber einer der Ausgabepuffer war zu klein, um die angeforderten Daten zu empfangen.</p>
<p>Der Ausgabepuffer wurde mit dem Umfang des Lesezeichens aufgefüllt, das passt. Die tatsächliche Größe des Lesezeichens wurde auch zurückgegeben, wenn dies angefordert wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>Der Cursor befindet sich derzeit nicht auf einem sekundären Index.</p>
<p>Das Abrufen eines sekundären Index Lesezeichens ist nicht sinnvoll, wenn der Cursor aktuell keinen sekundären Index verwendet. <a href="gg269221(v=exchg.10).md">Jetgetbookmark</a> sollte verwendet werden, wenn sich der Cursor nicht auf einem sekundären Index befindet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor ist nicht in einem Datensatz positioniert.</p>
<p>Dafür sind viele verschiedene Gründe möglich. Dies ist beispielsweise der Fall, wenn der Cursor aktuell nach dem letzten Datensatz im aktuellen Index positioniert ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird das sekundäre Index Lesezeichen für den Index Eintrag an der aktuellen Position eines Cursors in den Ausgabe Puffern zurückgegeben. Es erfolgt keine Änderung des Daten Bank Status.

Bei einem Fehler wird der Zustand der Ausgabepuffer und die tatsächliche Größe des sekundären Index Lesezeichens nur dann definiert, wenn JET_errBufferTooSmall zurückgegeben wurde. Wenn JET_errBufferTooSmall zurückgegeben wird, enthalten die Ausgabepuffer so viel von dem sekundären Index Lesezeichen, das in den bereitgestellten Speicherplatz passt, und die tatsächliche Größe des sekundären Index Lesezeichens ist genau. In jedem Fall erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Lesezeichen sollten im Allgemeinen als nicht transparente Datenblöcke behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Allerdings können die folgenden Eigenschaften für alle ESENT-Lesezeichen bekannt sein:

  - Ein Lesezeichen identifiziert eindeutig einen Datensatz in einer bestimmten Tabelle.

  - Das Lesezeichen eines Datensatzes ändert sich nicht für die Lebensdauer dieses Datensatzes.

  - Das Lesezeichen eines Datensatzes entspricht dem Schlüssel dieses Datensatzes auf dem primären Index für die Tabelle, die diesen Datensatz enthält. Wenn kein primärer Index für diese Tabelle definiert ist, erstellt die Datenbank-Engine ein eigenes Lesezeichen für den Datensatz.

  - Lesezeichen können mithilfe von [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) miteinander verglichen werden, um ihre relative Reihenfolge im primären Index für die Tabelle der Quelldaten Sätze festzulegen. Wenn kein primärer Index für diese Tabelle definiert ist, ist die relative Reihenfolge von Lesezeichen aus dieser Tabelle nicht sinnvoll.

  - Es ist bedeutungslos, Lesezeichen von Datensätzen aus unterschiedlichen Tabellen miteinander zu vergleichen.

  - Ein Lesezeichen ist immer kleiner oder gleich JET_cbBookmarkMost (256) Bytes in der Länge vor Windows Vista. In Windows Vista und späteren Versionen können Lesezeichen größer sein. Die maximale Größe eines Lesezeichens ist gleich dem aktuellen Wert von JET_paramKeyMost + 1.

Schlüssel sollten im Allgemeinen als nicht transparente Datenblöcke behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Allerdings können die folgenden Eigenschaften für alle ESENT-Schlüssel bekannt sein:

  - Schlüssel können mit [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) miteinander verglichen werden, um ihre relative Reihenfolge im Ursprungs Index für die Tabelle der Quell Indexeinträge festzulegen.

  - Es ist bedeutungslos, Schlüssel von Indexeinträgen aus verschiedenen Indizes miteinander zu vergleichen.

  - Ein Schlüssel ist immer kleiner oder gleich JET_cbKeyMost (255) Bytes in der Länge vor Windows Vista. Unter Windows Vista und späteren Versionen können Schlüssel größer sein. Die maximale Größe eines Schlüssels ist gleich dem aktuellen Wert JET_paramKeyMost.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetgetbookmark](./jetgetbookmark-function.md)  
[Jetgoysecondaryindexbookmark](./jetgotosecondaryindexbookmark-function.md)  
[Jetretrievekey](./jetretrievekey-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
