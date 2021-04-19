---
description: 'Weitere Informationen zu: jetdelete-Funktion'
title: JetDelete-Funktion
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362840"
---
# <a name="jetdelete-function"></a>JetDelete-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdelete-function"></a>JetDelete-Funktion

Die **jetdelete** -Funktion löscht den aktuellen Datensatz in einer Datenbanktabelle.

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet wird.

*TableID*

Der Cursor in einer Datenbanktabelle. Die aktuelle Zeile wird gelöscht.

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
<td><p>JET_errCallbackFailed</p></td>
<td><p>Fehler bei der Rückruffunktion. Zugriffs Verletzungen in Rückruf Funktionen werden z. b. abgefangen und in JET_errCallbackFailed übersetzt. Dieser Fehler wird nur von Windows XP und höher zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation</p></td>
<td><p>Der von <em>TableID</em> angegebene Cursor unterstützt das Löschen nicht. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der von <em>TableID</em> angegebene Cursor befindet sich nicht in einem Datensatz.</p></td>
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
<td><p>JET_errPermissionDenied</p></td>
<td><p>Die Datenbank-Engine verfügt nicht über ausreichende Berechtigungen zum Löschen des Datensatzes. Dies kann vorkommen, wenn die Datenbankdatei mit Schreib geschütztem Zugriff geöffnet wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackError</p></td>
<td><p>Ein Update Puffer (siehe <a href="gg269339(v=exchg.10).md">jetprepareupdate</a>) ist vorhanden, aber nicht alle Änderungen, die an Spalten vom Typ JET_coltypLongText und/oder Spalten vom Typ JET_coltypLongBinary vorgenommen werden, können zurückgesetzt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Es ist nicht zulässig, dieselbe Sitzung von mehr als einem Thread gleichzeitig zu verwenden. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Bei der Transaktion handelt es sich um eine schreibgeschützte Transaktion, die Löschvorgänge nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher vorhanden ist, um transaktionale Informationen zum Update beizubehalten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Eine andere Sitzung hat den Datensatz bereits für das Update gesperrt. Das von dieser Sitzung versuchte Update schlägt fehl.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird die Währung direkt vor dem nächsten Datensatz verbleiben. Wenn der gelöschte Datensatz der letzte in der Tabelle war, bleibt die Währung am Ende der Tabelle (d. h. nach dem neuen letzten Datensatz). Wenn der gelöschte Datensatz der einzige Datensatz in der Tabelle war, wird die Währung auf den Anfang festgelegt.

Die entsprechenden Indizes werden automatisch aktualisiert.

Wenn ein Update vorbereitet wird (mithilfe von [jetprepareupdate](./jetprepareupdate-function.md)), wird es abgebrochen. Der Update Puffer wird zurückgesetzt.

Bei einem Fehler bleibt die Währung unverändert. Wenn ein Update vorbereitet wird (siehe [jetprepareupdate](./jetprepareupdate-function.md)), wird der Update Puffer möglicherweise zurückgesetzt.

#### <a name="remarks"></a>Bemerkungen

Nicht alle Tabellen unterstützen das Löschen von Zeilen. In einer temporären Tabelle wird das Löschen von Zeilen normalerweise nicht unterstützt. Das Löschen von Datensätzen kann für temporäre Tabellen aus vielen Gründen aktiviert werden. einige davon sind:

  - JET_bitTTUpdatable wurde während der Erstellung angegeben.

  - Große temporäre Tabellen können das Löschen unterstützen, wenn Sie mit JET_bitTTScrollable oder JET_bitTTIndexed erstellt wurden. Der Schwellenwert, bei dem eine temporäre Tabelle "Large" ist, beträgt derzeit 64 Kilobyte, kann jedoch in zukünftigen Versionen geändert werden.

Windows XP und höher. Rückruf Funktionen können von **jetdelete** aufgerufen werden, einschließlich JET_cbtypBeforeDelete und JET_cbtypAfterDelete.

Es ist wichtig, die Auswirkungen der Ausführung einer großen Anzahl von Aktualisierungs Vorgängen in einer einzelnen Transaktion zu verstehen. Jedes Update der Datenbank muss von der Datenbank-Engine im Versionsspeicher nachverfolgt werden. Der Versionsspeicher enthält einen Live Datensatz aller verschiedenen Versionen der einzelnen Datensatz-oder Indexeinträge in der Datenbank, die von allen aktiven Transaktionen angezeigt werden können. Diese Versionen werden zur Unterstützung der Parallelitäts Steuerung mit mehreren Versionsverwaltung verwendet, die von der Datenbank-Engine verwendet wird, um Transaktionen mithilfe der Momentaufnahme Isolation zu unterstützen. Sobald die Datenbank-Engine die Ressourcen erschöpft hat, die zum Speichern dieser Versionen verwendet werden, kann Sie keine weiteren Änderungen mehr akzeptieren, bis einige Transaktionen abgeschlossen sind, damit diese Ressourcen freigegeben werden können. Wenn sich die Engine in diesem Zustand befindet, schlagen alle Updates mit Jet_errVersionStoreOutOfMemory fehl. Die Ressourcen, die für die Datenbank-Engine zum Speichern dieser Versionen verfügbar sind, können mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit *JET_paramMaxVerPages* und *JET_paramGlobalMinVerPages* gesteuert werden.

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
[Jetopumtemptable](./jetopentemptable-function.md)  
[Jetprepareupdate](./jetprepareupdate-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
