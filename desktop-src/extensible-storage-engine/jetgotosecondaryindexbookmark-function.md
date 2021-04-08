---
description: Weitere Informationen finden Sie in der jetgoto secondaryindexbookmark-Funktion
title: Jetgoto secondaryindexbookmark-Funktion
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893833fd1770fe3d972033a4d10f9047b0f61dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959899"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>Jetgoto secondaryindexbookmark-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgotosecondaryindexbookmark-function"></a>Jetgoto secondaryindexbookmark-Funktion

Die **jetgoto secondaryindexbookmark** -Funktion positioniert einen Cursor auf einen Index Eintrag, der dem angegebenen sekundären Index Lesezeichen zugeordnet ist. Das sekundäre Index Lesezeichen muss mit demselben Index für dieselbe Tabelle verwendet werden, aus der es ursprünglich abgerufen wurde. Das sekundäre Index Lesezeichen für einen Index Eintrag kann mithilfe von **jetgoysecondaryindexbookmark** abgerufen werden.

**Windows XP:**  **jetgodesecondaryindexbookmark** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*pvsecondarykey*

Der Puffer, der den sekundären Schlüssel enthält, der zum Positionieren des Cursors verwendet werden soll.

*cbsecondarykey*

Die Größe des sekundären Schlüssels im Puffer.

*pvprimarybookmark*

Der Puffer, der das Primärschlüssel-Lesezeichen enthält, das zum Positionieren des Cursors verwendet werden soll.

*cbprimarybookmark*

Die Größe des Primärschlüssel-Lesezeichens im Puffer.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.

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
<td><p>JET_bitBookmarkPermitVirtualCurrency</p></td>
<td><p>Wenn der Index Eintrag nicht mehr gefunden werden kann, wird der Cursor positioniert, wo der Index Eintrag bereits gefunden wurde. Der Vorgang schlägt weiterhin mit JET_errRecordDeleted fehl. Es ist jedoch möglich, zum nächsten oder vorherigen Index Eintrag relativ zum Index Eintrag zu wechseln, der jetzt fehlt.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht durchgeführt werden, weil die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>Das angegebene sekundäre Index Textzeichen ist ungültig. Dieser Fehler ist möglicherweise aufgetreten, weil der sekundäre Schlüssel NULL ist oder der Sekundär Schlüsselpuffer Zeiger <strong>null</strong>ist. Dieser Fehler tritt auf, weil</p>
<ul>
<li><p>Der aktuelle sekundäre Index verfügt nicht über eine Unique-Einschränkung, und die Größe des bereitgestellten Lesezeichens ist 0 (null).</p></li>
<li><p>Der Lesezeichen-Puffer Zeiger ist <strong>null</strong>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>Der Cursor befindet sich derzeit nicht auf einem sekundären Index. Es ist nicht sinnvoll, zu einem sekundären Index Lesezeichen zu wechseln, wenn der Cursor aktuell keinen sekundären Index verwendet. <a href="gg294053(v=exchg.10).md">Jetgojebookmark</a> sollte verwendet werden, wenn sich der Cursor nicht auf einem sekundären Index befindet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Der Index Eintrag, der dem sekundären Index Lesezeichen zugeordnet ist, wurde nicht gefunden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird der Cursor an einem Index Eintrag positioniert, der dem angegebenen sekundären Index Lesezeichen zugeordnet ist. Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen. Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht. Es erfolgt keine Änderung des Daten Bank Status.

Wenn diese Funktion fehlschlägt, bleibt die Position des Cursors unverändert, es sei denn, JET_errRecordDeleted zurückgegeben und JET_bitBookmarkPermitVirtualCurrency angegeben wird. In diesem Fall wird der Cursor positioniert, wo der Index Eintrag, der dem angegebenen sekundären Index Textzeichen zugeordnet ist, wäre. Der Cursor kann relativ zu dieser Position verschoben werden, befindet sich jedoch noch nicht in einem gültigen Index Eintrag.

Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen. Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht. In jedem Fall erfolgt keine Änderung des Daten Bank Status.

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
[Jetgetsecondaryindexbookmark](./jetgetsecondaryindexbookmark-function.md)  
[Jetgojebookmark](./jetgotobookmark-function.md)  
[Jetstopservice](./jetstopservice-function.md)
