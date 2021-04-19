---
description: 'Weitere Informationen zu: jetgojebookmark-Funktion'
title: Jetgoto Bookmark-Funktion
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
ms.openlocfilehash: 89dde261648b396bcfc9532911c0d4acd3c88828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364238"
---
# <a name="jetgotobookmark-function"></a>Jetgoto Bookmark-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgotobookmark-function"></a>Jetgoto Bookmark-Funktion

Die **jetgoatbookmark** -Funktion positioniert einen Cursor auf einen Index Eintrag für den Datensatz, der dem angegebenen Lesezeichen zugeordnet ist. Das Lesezeichen kann mit jedem für eine Tabelle definierten Index verwendet werden. Das Lesezeichen für einen Datensatz kann mit [jetgetbookmark](./jetgetbookmark-function.md)abgerufen werden.

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*pvbookmark*

Der Puffer, der das Lesezeichen enthält, das zum Positionieren des Cursors verwendet werden soll.

*cbbookmark*

Die Größe des Lesezeichens im Puffer.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da der-Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:</strong>   Dieser Rückgabewert wurde in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>Das angegebene Lesezeichen ist ungültig. Dieser Fehler ist möglicherweise aufgetreten, weil die Größe des Lesezeichens 0 (null) ist oder der Lesezeichen-Puffer Zeiger <strong>null</strong>ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor befindet sich auf einem sekundären Index, und für den Datensatz, der dem Lesezeichen zugeordnet ist, wurde kein Index Eintrag gefunden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Der Datensatz, der dem Lesezeichen zugeordnet ist, konnte nicht gefunden werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p><strong>Windows XP:</strong>   Dieser Rückgabewert wurde in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird der Cursor an einem Index Eintrag für den Datensatz positioniert, der dem angegebenen Lesezeichen zugeordnet ist. Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen. Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht. Es erfolgt keine Änderung des Daten Bank Status.

Wenn diese Funktion fehlschlägt, bleibt die Position des Cursors unverändert. Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen. Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Es gibt zwei Möglichkeiten, ein Lesezeichen zu verwenden, um einen Cursor auf einem Index zu positionieren. Der erste besteht darin, das Lesezeichen zu verwenden, um den Datensatz direkt zu positionieren. Dies tritt auf, wenn der aktuelle Index des Cursors der primäre Index ist. Diese Technik funktioniert, weil ein ESENT-Lesezeichen mit dem Primärschlüssel des zugehörigen Datensatzes identisch ist.

Die zweite Möglichkeit zur Verwendung eines Lesezeichens besteht darin, es in einem Eintrag in einem sekundären Index zu positionieren, der dem Datensatz entspricht, der diesem Lesezeichen zugeordnet ist. Während dieses Vorgangs sucht die Engine den tatsächlichen Datensatz mit dem Lesezeichen auf dem primären Index. Anschließend werden die Daten Satz Daten und die sekundäre Index Definition verwendet, um einen Schlüssel in den sekundären Index zu berechnen, der auf den Datensatz verweist. Anschließend positioniert Sie den Cursor auf dem Index Eintrag für diesen Schlüssel. Wenn sich der Cursor aktuell auf einem sekundären Index über eine oder mehrere mehrwertige Schlüssel Spalten befindet, wird der Cursor auf dem Index Eintrag positioniert, der dem ersten mehrwertigen Wert der einzelnen Schlüssel Spalten entspricht.

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
[Jetgetbookmark](./jetgetbookmark-function.md)
