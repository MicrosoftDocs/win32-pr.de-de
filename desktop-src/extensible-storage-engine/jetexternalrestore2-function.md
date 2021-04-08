---
description: 'Weitere Informationen finden Sie hier: JetExternalRestore2-Funktion'
title: JetExternalRestore2-Funktion
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96314e401a81271f5a71bc056faa95fc1ae0dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960197"
---
# <a name="jetexternalrestore2-function"></a>JetExternalRestore2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetexternalrestore2-function"></a>JetExternalRestore2-Funktion

Die **JetExternalRestore2** -Funktion stellt eine externe Sicherung wieder her, die mit den externen Backup-APIs erstellt wurde, und stellt Prüfpunkte für zirkuläre Protokollierungs Vorgänge bereit. Dies wird als harte Wiederherstellung bezeichnet, die ähnlich, aber von der Soft-Wiederherstellung abweicht, wie von der [jetinit](./jetinit-function.md) -Funktion ausgeführt wird.

**Windows XP: JetExternalRestore2** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parameter

*szcheckpointfilepath*

Der Pfad für die Prüf Punkt Datei, die während der Wiederherstellung verwendet werden soll, wenn *sztargetinstancecheckpointpath* nicht angegeben ist oder der Pfad eine aktive oder ausgeführte Instanz aufweist.

*szlogpath*

Der Pfad oder das Verzeichnis für die Protokolle für die letzte Phase (rückgängig) der Wiederherstellung und möglicherweise für die Roll Forward-Protokolle. Dieser Pfad kann mit dem *szbackuplogpath* identisch sein.

*rgrstmap*

Dies ist ein Array von [JET_RSTMAP](./jet-rstmap-structure.md) Strukturen. Dabei handelt es sich um eine Zuordnung von alten und neuen Daten Bank Pfaden oder Dateinamen. Dies wird verwendet, da die Datenbanken möglicherweise an einem anderen Speicherort als dem Speicherort wieder hergestellt werden müssen, von dem aus Sie gesichert wurden. Wenn mehrere Datenbanken an einen einzelnen protokolliersatz angefügt werden, kann die Restore Map eine Teilmenge der wiederherzustellenden Datenbanken angeben.

*crstfilemap*

Die Anzahl der Einträge im *rgrstmap* -Array Parameter.

*szbackuplogpath*

Der Pfad zu dem Verzeichnis, in dem die Protokolldateien wieder hergestellt werden. Dabei handelt es sich um die Protokolle, die während der externen Sicherungs Sequenz gelesen wurden. Dieser Pfad kann mit dem *szlogpath* identisch sein.

*ploginfo*

*Ploginfo* beschreibt verschiedene Aspekte der Sicherungs Protokolle für die Wiederherstellung. dieser Parameter ermöglicht es **JetExternalRestore2** , die expliziten *genlow* -und *genhigh* -Parameter, die **JetExternalRestore2** haben, sowie den Basisprotokoll Namen anstelle eines vermuteten Protokoll Basis namens "edb" zu verwenden.

*sztargetinstancename*

Dieser Parameter ist veraltet und kann nicht in der Anwendung verwendet werden.

*sztargetinstancelogpath*

Der Pfad für die rollforwardprotokolle, wenn sich der Speicherort der Protokolle, für die Sie ein Roll Forward ausführen möchten, in einem aktiven Protokollierungs Satz oder einer Instanz befindet. Dieser Wert sollte nicht angegeben werden, wenn die Ziel Instanz die zirkuläre Protokollierung verwendet.

*sztargetinstancecheckpointpath*

Der Pfad für den Prüfpunkt während der Wiederherstellung, wenn keine aktive Instanz an diesem Ziel ausgeführt wird. Dieser Wert sollte nicht angegeben werden, wenn die Ziel Instanz die zirkuläre Protokollierung verwendet.

*PFN*

Der Status Rückruf, der den Fortschritt der Wiederherstellung meldet.

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
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>Der angegebene <em>sztargetinstancelogpath</em> gehört nicht zu einer initialisierten Instanz. Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Dies weist darauf hin, dass die Datenbank beschädigt wurde, oder eine unbekannte Datei.</p></td>
</tr>
<tr class="even">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn für die Protokolldateien im <em>szbackuplogpath</em>eine Protokoll Generierung oberhalb der in <em>genhigh</em> oder <em>ploginfo. ulgenhigh</em>angegebenen Protokolldateien vorliegt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die angeforderte Datei nicht geöffnet werden konnte, da Sie im angegebenen Pfad nicht gefunden wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dies kann bei <a href="gg294088(v=exchg.10).md">jetexternalrestore</a>der Fall sein, wenn " <em>sztargetcheckpointpath</em> " und " <em>sztargetinstancelogpath</em> " nicht beide angegeben oder nicht angegeben sind. Das heißt, Sie müssen abgeglichen werden und beide angegeben oder nicht angegeben werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da der angegebene Pfad nicht gefunden wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn es sich bei der während der Wiederherstellung angegebenen Datenbankdatei nicht um eine Datenbank handelt, die mit externer Sicherung gesichert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Die Datenbank-Engine kann eine externe Wiederherstellung oder eine feste Wiederherstellung nicht im Single Instance-Modus ausführen. Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn eine der Protokolldateien im <em>szbackuplogpath</em>eine Protokoll Generierung unterhalb der von <em>genlow</em> oder <em>ploginfo. ulgenlow</em>angegebenen Protokolldateien aufweist.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg werden alle Datenbanken aus der *rgrstmap* vollständig wieder hergestellt und sind in einem sauberen oder konsistenten Zustand. An diesem Punkt kann die Datenbank erneut an eine vorhandene Instanz bereitgestellt werden.

Bei einem Fehler konnte die Engine die Datenbank nicht wiederherstellen. Die Datenbank befindet sich in einem ungültigen Status. um eine Wiederherstellung zu versuchen, muss die gesamte Datenbank wieder hergestellt werden. In der Regel handelt es sich bei einer solchen Situation um eine Datenträger-oder Protokoll Beschädigung oder eine andere Form der Protokoll Misswirtschaft oder um einen nicht kontinuierlichen Protokoll Satz.

#### <a name="remarks"></a>Bemerkungen

Siehe [jetexternalrestore](./jetexternalrestore-function.md).

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
<td><p>Implementiert als <strong>JetExternalRestore2W</strong> (Unicode) und <strong>JetExternalRestore2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[Jetbeginexternalbackup](./jetbeginexternalbackup-function.md)  
[Jetexternalrestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
