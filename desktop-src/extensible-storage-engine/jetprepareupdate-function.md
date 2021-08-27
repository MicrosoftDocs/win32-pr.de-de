---
description: Weitere Informationen finden Sie unter JetPrepareUpdate-Funktion.
title: JetPrepareUpdate-Funktion
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
ms.openlocfilehash: 98b14688b42c3e29bbbbab5b96466ad6c97f98e3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477546"
---
# <a name="jetprepareupdate-function"></a>JetPrepareUpdate-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetprepareupdate-function"></a>JetPrepareUpdate-Funktion

Die **JetPrepareUpdate-Funktion** ist der erste Vorgang bei der Durchführung eines Updates, um einen neuen Datensatz einzufügen oder einen vorhandenen Datensatz durch neue Werte zu ersetzen. Updates werden durchgeführt, indem **JetPrepareUpdate** aufgerufen wird, [jetSetColumn](./jetsetcolumn-function.md) oder [JetSetColumns](./jetsetcolumns-function.md) 0 oder mehr Mal aufgerufen wird und schließlich [JetUpdate](./jetupdate-function.md) aufgerufen wird, um den Vorgang abzuschließen. **JetPrepareUpdate** und [JetUpdate](./jetupdate-function.md) legen die Grenzen für einen Updatevorgang fest und sind wichtig, damit nur der endgültige Updatestatus eines Datensatzes in Indizes eingegeben wird. Dies ist effizienter, aber auch in Fällen erforderlich, in denen Daten mit einem gültigen Zustand übereinstimmen müssen, indem mehr als bei einem Set Column-Vorgang durchgeführt wird.

Es gibt einige verschiedene Optionen zum Einfügen oder Ersetzen von Datensätzen, die im Folgenden ausführlicher beschrieben werden.

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*Prep*

Die Optionen, die zur Vorbereitung auf ein Update verwendet werden können, einschließlich der folgenden.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_prepCancel</p> | <p>Dieses Flag bewirkt, dass <strong>JetPrepareUpdate</strong> das Update für diesen Cursor abbricht.</p> | 
| <p>JET_prepInsert</p> | <p>Dieses Flag bewirkt, dass der Cursor sich auf das Einfügen eines neuen Datensatzes vorbereitet. Alle Daten werden mit dem Standardzustand für den Datensatz initialisiert. Wenn die Tabelle über eine Spalte mit automatischer Inkrementierung verfügt, wird diesem Datensatz ein neuer Wert zugewiesen, unabhängig davon, ob das Update letztendlich erfolgreich ist, fehlschlägt oder abgebrochen wird.</p> | 
| <p>JET_prepInsertCopy</p> | <p>Dieses Flag bewirkt, dass der Cursor sich auf das Einfügen einer Kopie des vorhandenen Datensatzes vorbereitet. Wenn diese Option verwendet wird, muss ein aktueller Datensatz vorhanden sein. Der Anfangszustand des neuen Datensatzes wird aus dem aktuellen Datensatz kopiert. Lange Werte, die außerhalb des Datensatzes gespeichert werden, werden virtuell kopiert.</p> | 
| <p>JET_prepInsertCopyDeleteOriginal</p> | <p>Dieses Flag bewirkt, dass der Cursor sich auf ein Einfügen desselben Datensatzes und einen Lösch- oder ursprünglichen Datensatz vorbereitet. Sie wird in Fällen verwendet, in denen sich der Primärschlüssel geändert hat.</p> | 
| <p>JET_prepReplace</p> | <p>Dieses Flag bewirkt, dass der Cursor sich auf eine Ersetzung des aktuellen Datensatzes vorbereitet. Wenn die Tabelle über eine Versionsspalte verfügt, wird die Versionsspalte auf den nächsten Wert in ihrer Sequenz festgelegt. Wenn dieses Update nicht abgeschlossen ist, ist der Versionswert im Datensatz nicht betroffen. Es wird eine Updatesperre für den Datensatz eingerichtet, um zu verhindern, dass andere Sitzungen diesen Datensatz aktualisieren, bevor diese Sitzung abgeschlossen wird.</p> | 
| <p>JET_prepReplaceNoLock</p> | <p>Dieses Flag ähnelt JET_prepReplace, aber es wird keine Sperre eingerichtet, um zu verhindern, dass andere Sitzungen diesen Datensatz aktualisieren. Stattdessen erhält diese Sitzung möglicherweise JET_errWriteConflict, wenn <a href="gg269288(v=exchg.10).md">Sie JetUpdate</a> aufruft, um das Update abzuschließen.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errAlreadyPrepared</p> | <p><strong>JetPrepareUpdate</strong> wurde mit einem gültigen Flag für die Vorbereitung aufgerufen, aber nicht JET_prepCancel, und der Cursor befand sich bereits im vorbereiteten Zustand.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Das angegebene Vorbereitungsflag ist kein gültiges Flag.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errNotInTransaction</p> | <p><strong>JetPrepareUpdate</strong> wurde aufgerufen, um einen Datensatz mit SLV-Spalten zu ersetzen. SLV-Spalten. Beachten Sie, dass SLV-Spalten ein Feature sind, das nicht für die allgemeine Verwendung vorgesehen ist. Dieses Feature wird zur Unterstützung der Microsoft Exchange-Infrastruktur verwendet und ist nicht für die Verwendung in Ihrer Anwendung vorgesehen.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRollbackError</p> | <p><strong>JetPrepareUpdate</strong> wurde mit JET_prepCancel aufgerufen, konnte aber nicht alle Änderungen zurücksetzen, die an Spalten vom Typ JET_coltypLongText und/oder Spalten vom Typ JET_coltypLongBinary vorgenommen wurden.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieses Flag kann nicht mit derselben Sitzung von mehreren Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p><strong>JetPrepareUpdate</strong> wurde mit JET_prepCancel aufgerufen, aber der Cursor befand sich nicht im vorbereiteten Zustand.</p> | 



Bei Erfolg wird der Cursor für das gewünschte Update in den vorbereiteten Zustand geändert, oder im Fall von JET_prepCancel wird der Cursor in den nicht vorbereiteten Zustand zurückgesetzt, und alle Änderungen werden verworfen.

Bei einem Fehler bleibt der Cursorzustand unverändert. Wenn der Fehler JET_errRollbackError wurde, wird der Cursorzustand in den nicht vorbereiteten Zustand geändert, aber nicht alle Änderungen wurden zurückgesetzt.

#### <a name="remarks"></a>Hinweise

Das Einfügen einer Kopie eines Datensatzes ist eine wichtige Optimierung, wenn Datensätze Daten vom Typ JET_coltypLongText und/oder JET_coltypLongBinary gemeinsam nutzen. Diese Daten werden außerhalb des Datensatzes gespeichert, wenn sie groß sind, und es ist möglich, dass mehrere Datensätze dieselbe physische Darstellung der Daten gemeinsam nutzen. In diesem Fall können die Daten aus beiden Datensätzen aktualisiert werden. Dies führt jedoch dazu, dass die Daten so überhäuft werden, dass jeder Datensatz über eine eigene Kopie verfügt. Es ist nicht möglich, Daten in einem Datensatz durch eine Änderung eines anderen Datensatzes zu ändern. Außerdem ist es nicht möglich, ein Update eines Datensatzes durch ein Update eines anderen Datensatzes zu blockieren. Dies ist ein zentrales Feature für ESE und wird als Sperren auf Datensatzebene bezeichnet.

[JetUpdate-Vorgänge,](./jetupdate-function.md) bei denen ein Fehler vorschlägt, belassen den Cursor im zustand "Update vorbereitet". Dies ermöglicht die Korrektur einiger Fehler, z. B. eines falschen Spaltenwerts, ohne dass der Aktualisierungszustand neu erstellt werden muss. Dies bedeutet, dass in allen Fällen, in denen ein Cursor ein Update abbricht, **JetPrepareUpdate** explizit mit JET_prepCancel aufgerufen werden muss.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
