---
description: 'Weitere Informationen zu: jetprepareupdate-Funktion'
title: Jetprepareupdate-Funktion
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369086"
---
# <a name="jetprepareupdate-function"></a>Jetprepareupdate-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetprepareupdate-function"></a>Jetprepareupdate-Funktion

Die **jetprepareupdate** -Funktion ist der erste Vorgang, bei dem ein Update durchgeführt wird, um einen neuen Datensatz einzufügen oder einen vorhandenen Datensatz durch neue Werte zu ersetzen. Updates werden durch Aufrufen von **jetprepareupdate** und anschließendes Aufrufen von [jetsetcolumn](./jetsetcolumn-function.md) oder [jetsetcolumns](./jetsetcolumns-function.md) (null oder mehrmals) und schließlich durch Aufrufen von [jetupdate](./jetupdate-function.md) zum Durchführen des Vorgangs durchgeführt. **Jetprepareupdate** und [jetupdate](./jetupdate-function.md) legen die Grenzen für einen Aktualisierungs Vorgang fest und sind wichtig, wenn nur der endgültige Aktualisierungs Status eines Datensatzes in Indizes eingegeben werden soll. Dies ist sowohl effizienter als auch bei Fällen erforderlich, in denen Daten mit einem gültigen Zustand über mehr als den Vorgang zum Festlegen von Spalten verglichen werden müssen.

Es gibt verschiedene Optionen zum Einfügen oder Austauschen von Datensätzen. Diese werden im folgenden ausführlicher beschrieben.

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*vorzubereiten*

Die Optionen, die verwendet werden können, um ein Update vorzubereiten, einschließlich der folgenden.

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
<td><p>JET_prepCancel</p></td>
<td><p>Dieses Flag bewirkt, dass <strong>jetprepareupdate</strong> das Update für diesen Cursor abbricht.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepInsert</p></td>
<td><p>Dieses Flag bewirkt, dass der Cursor eine Einfügung eines neuen Datensatzes vorbereitet. Alle Daten werden auf den Standardstatus für den Datensatz initialisiert. Wenn die Tabelle eine automatische Inkrement-Spalte aufweist, wird diesem Datensatz ein neuer Wert zugewiesen, unabhängig davon, ob das Update letztendlich erfolgreich ist, fehlschlägt oder abgebrochen wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_prepInsertCopy</p></td>
<td><p>Dieses Flag bewirkt, dass der Cursor eine Einfügung einer Kopie des vorhandenen Datensatzes vorbereitet. Wenn diese Option verwendet wird, muss ein aktueller Datensatz vorhanden sein. Der ursprüngliche Zustand des neuen Datensatzes wird aus dem aktuellen Datensatz kopiert. Lange Werte, die außerhalb des Datensatzes gespeichert werden, werden virtuell kopiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepInsertCopyDeleteOriginal</p></td>
<td><p>Dieses Flag bewirkt, dass der Cursor eine Einfügung desselben Datensatzes und einen Löschvorgang oder den ursprünglichen Datensatz vorbereitet. Sie wird in Fällen verwendet, in denen sich der Primärschlüssel geändert hat.</p></td>
</tr>
<tr class="odd">
<td><p>JET_prepReplace</p></td>
<td><p>Dieses Flag bewirkt, dass der Cursor eine Ersetzung des aktuellen Datensatzes vorbereitet. Wenn die Tabelle eine Versions Spalte aufweist, wird die Versions Spalte auf den nächsten Wert in der zugehörigen Reihenfolge festgelegt. Wenn dieses Update nicht vollständig ausgeführt wird, ist der Versions Wert im Datensatz nicht betroffen. Es wird eine Update Sperre für den Datensatz erstellt, um zu verhindern, dass dieser Datensatz von anderen Sitzungen aktualisiert wird, bevor diese Sitzung abgeschlossen ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepReplaceNoLock</p></td>
<td><p>Dieses Flag ähnelt JET_prepReplace, es wird jedoch keine Sperre erstellt, um zu verhindern, dass andere Sitzungen diesen Datensatz aktualisieren. Stattdessen erhält diese Sitzung möglicherweise JET_errWriteConflict, wenn <a href="gg269288(v=exchg.10).md">jetupdate</a> aufgerufen wird, um das Update abzuschließen.</p></td>
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
<td><p>JET_errAlreadyPrepared</p></td>
<td><p><strong>Jetprepareupdate</strong> wurde mit einem gültigen Flag für prep aufgerufen, aber nicht JET_prepCancel, und der Cursor war bereits im vorbereiteten Zustand.</p></td>
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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Das angegebene prep-Flag ist kein gültiges Flag.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction</p></td>
<td><p><strong>Jetprepareupdate</strong> wurde aufgerufen, um einen Datensatz zu ersetzen, der über SLV-Spalten verfügte. SLV-Spalten. Beachten Sie, dass SLV-Spalten ein Feature sind, das nicht für die allgemeine Verwendung vorgesehen ist. Diese Funktion wird zur Unterstützung der Microsoft Exchange-Infrastruktur verwendet und ist nicht für die Verwendung in Ihrer Anwendung vorgesehen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError</p></td>
<td><p><strong>Jetprepareupdate</strong> wurde mit JET_prepCancel aufgerufen, konnte aber nicht alle Änderungen zurücksetzen, die an Spalten vom Typ JET_coltypLongText und/oder Spalten vom Typ JET_coltypLongBinary vorgenommen wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieses Flag kann nicht mit derselben Sitzung von mehreren Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p><strong>Jetprepareupdate</strong> wurde mit JET_prepCancel aufgerufen, aber der Cursor befand sich nicht im vorbereiteten Zustand.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wechselt der Cursor zum Zweck der gewünschten Aktualisierung in den vorbereiteten Zustand, oder im Fall von JET_prepCancel wird der Cursor in den Zustand "nicht vorbereitet" versetzt, und alle Änderungen werden verworfen.

Bei einem Fehler bleibt der Cursor Zustand unverändert. Wenn der Fehler JET_errRollbackError wurde, wird der Cursor Zustand in den Zustand "nicht vorbereitet" geändert, aber nicht alle Änderungen wurden zurückgesetzt.

#### <a name="remarks"></a>Bemerkungen

Das Einfügen einer Kopie eines Datensatzes ist eine wichtige Optimierung, wenn Datensätze Daten vom Typ JET_coltypLongText und/oder JET_coltypLongBinary gemeinsam verwenden. Diese Daten werden bei großen Datensätzen außerhalb des Datensatzes gespeichert, und es ist möglich, dass mehrere Datensätze dieselbe physische Darstellung der Daten gemeinsam nutzen. In diesem Fall können die Daten von jedem Datensatz aus aktualisiert werden. Dies führt jedoch dazu, dass die Daten so Burst werden, dass jeder Datensatz über eine eigene Kopie verfügt. Es ist nicht möglich, Daten in einem Datensatz durch eine Änderung eines anderen Datensatzes zu ändern. Außerdem ist es nicht möglich, ein Update eines einzelnen Datensatzes durch Aktualisieren eines anderen Datensatzes zu blockieren. Dies ist ein zentrales Feature von ESE und wird als Sperren auf Datensatzebene bezeichnet.

Bei [jetupdate](./jetupdate-function.md) -Vorgängen, bei denen der Cursor nicht erfolgreich ist Dadurch können einige Fehler korrigiert werden, z. b. ein falscher Spaltenwert, ohne dass der Aktualisierungs Status neu erstellt werden muss. Dies bedeutet, dass in allen Fällen, in denen ein Cursor ein Update abbricht, " **jetprepareupdate** " explizit mit JET_prepCancel aufgerufen werden muss.

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
[Jetretrievecolumschlag](./jetretrievecolumn-function.md)  
[Jetsetcolumn](./jetsetcolumn-function.md)  
[Jetupdate](./jetupdate-function.md)
