---
description: Weitere Informationen finden Sie unter JetGotoBookmark-Funktion.
title: JetGotoBookmark-Funktion
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 56e94339a49cc80e8b7b416e89efc5c85079981e0430f325e29f1dd711eef63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978999"
---
# <a name="jetgotobookmark-function"></a>JetGotoBookmark-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgotobookmark-function"></a>JetGotoBookmark-Funktion

Die **JetGotoBookmark-Funktion** positioniert einen Cursor an einem Indexeintrag für den Datensatz, der dem angegebenen Lesezeichen zugeordnet ist. Das Lesezeichen kann mit jedem Index verwendet werden, der für eine Tabelle definiert ist. Das Lesezeichen für einen Datensatz kann mit [JetGetBookmark abgerufen werden.](./jetgetbookmark-function.md)

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*pvBookmark*

Der Puffer, der das Lesezeichen enthält, das zum Positionieren des Cursors verwendet werden soll.

*cbBookmark*

Die Größe des Lesezeichens im Puffer.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die -Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p>
<p><strong>Windows XP:</strong>   Dieser Rückgabewert wurde in xp Windows eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>Das bereitgestellte Lesezeichen ist ungültig. Dies kann aufgetreten sein, weil die Größe des Lesezeichens 0 (null) oder der Lesezeichenpufferzeiger <strong>NULL ist.</strong></p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor befindet sich auf einem sekundären Index, und für den Datensatz, der dem Lesezeichen zugeordnet ist, konnte kein Indexeintrag gefunden werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Der datensatz, der dem Lesezeichen zugeordnet ist, wurde nicht gefunden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p>
<p><strong>Windows XP:</strong>   Dieser Rückgabewert wurde in xp Windows eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ist, wird der Cursor an einem Indexeintrag für den Datensatz positioniert, der dem angegebenen Lesezeichen zugeordnet ist. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist, wird dieser Indexbereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird dieser Suchschlüssel gelöscht. Es erfolgt keine Änderung des Datenbankstatus.

Wenn diese Funktion fehlschlägt, bleibt die Position des Cursors unverändert. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist, wird dieser Indexbereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird dieser Suchschlüssel gelöscht. Es erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Hinweise

Es gibt zwei Möglichkeiten, ein Lesezeichen zu verwenden, um einen Cursor auf einem Index zu positionieren. Die erste besteht in der verwendung des Lesezeichens, um sich direkt auf dem Datensatz zu positionieren. Dies tritt auf, wenn der aktuelle Index des Cursors der primäre Index ist. Dieses Verfahren funktioniert, da ein ESENT-Lesezeichen mit dem Primärschlüssel des zugeordneten Datensatzes identisch ist.

Die zweite Möglichkeit, ein Lesezeichen zu verwenden, besteht in der Position auf einem Eintrag in einem sekundären Index, der dem Datensatz entspricht, der diesem Lesezeichen zugeordnet ist. Während dieses Vorgangs sucht die Engine den tatsächlichen Datensatz mithilfe des Lesezeichens für den primären Index. Anschließend werden die Datensatzdaten und die Definition des sekundären Indexes verwendet, um einen Schlüssel im sekundären Index zu berechnen, der auf den Datensatz verweist. Anschließend wird der Cursor auf dem Indexeintrag für diesen Schlüssel positioniert. Wenn sich der Cursor derzeit auf einem sekundären Index über einer oder mehreren Mehrwertschlüsselspalten befindet, wird der Cursor auf dem Indexeintrag positioniert, der dem ersten Mehrwert jeder dieser Schlüsselspalten entspricht.

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
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)
