---
description: 'Weitere Informationen zu: JetExternalRestore2-Funktion'
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
ms.openlocfilehash: 6d2cbd4a13555d754cdbc1f9c02011b5891d6d6fcfae3fea822ddf6ad9953b78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719190"
---
# <a name="jetexternalrestore2-function"></a>JetExternalRestore2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetexternalrestore2-function"></a>JetExternalRestore2-Funktion

Die **JetExternalRestore2-Funktion** stellt eine externe Sicherung wieder her, die mit den externen Sicherungs-APIs erstellt wurde, und stellt Prüfpunkte bereit, die für zirkuläre Protokollierungsvorgänge verwendet werden können. Dies wird als harte Wiederherstellung bezeichnet, die ähnlich ist, sich jedoch von der soft recovery unterscheidet, die von der [JetInit-Funktion](./jetinit-function.md) durchgeführt wird.

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

*szCheckpointFilePath*

Der Pfad für die Prüfpunktdatei, die während der Wiederherstellung verwendet werden soll, wenn *szTargetInstanceCheckpointPath* nicht angegeben ist oder dieser Pfad über eine aktive oder ausgeführte Instanz verfügt.

*szLogPath*

Der Pfad oder das Verzeichnis für die Protokolle für die letzte Phase (Rückgängig) der Wiederherstellung und möglicherweise für die Roll forward-Protokolle. Dieser Pfad kann mit dem *szBackupLogPath* identisch sein.

*rgrstmap*

Dies ist ein Array von [JET_RSTMAP](./jet-rstmap-structure.md) Strukturen. Dies ist eine Zuordnung alter und neuer Datenbankpfade oder Dateinamen. Dies wird verwendet, da die Datenbanken möglicherweise an einem anderen Speicherort als dem Speicherort wiederhergestellt werden müssen, von dem sie gesichert wurden. Wenn mehrere Datenbanken an einen einzelnen Protokollierungssatz angefügt sind, kann die Wiederherstellungszuordnung eine Teilmenge der Wiederherstellungsdatenbanken angeben.

*crstfilemap*

Die Anzahl der Einträge im *rgrstmap-Arrayparameter.*

*szBackupLogPath*

Der Pfad zum Verzeichnis, in dem die Protokolldateien wiederhergestellt werden. Dies sind die Protokolle, die während der externen Sicherungssequenz ausgelesen wurden. Dieser Pfad kann mit dem *szLogPath* identisch sein.

*pLogInfo*

*pLogInfo* beschreibt mehrere Aspekte der Wiederherstellung von Sicherungsprotokollen. Mit diesem Parameter kann **JetExternalRestore2** die expliziten *GenLow-* und *genHigh-Parameter* von **JetExternalRestore2** sowie den Basisprotokollnamen anstelle eines angenommenen Protokollbasisnamens "edb" verwenden.

*szTargetInstanceName*

Dieser Parameter ist veraltet und kann nicht in Ihrer Anwendung verwendet werden.

*szTargetInstanceLogPath*

Der Pfad für die Roll forward-Protokolle, wenn sich der Speicherort der Protokolle, für die Sie einen Roll forward erstellen möchten, in einem aktiven Protokollierungssatz oder in einer aktiven Protokollierungsinstanz befindet. Dies sollte nicht angegeben werden, wenn die Zielinstanz die zirkuläre Protokollierung verwendet.

*szTargetInstanceCheckpointPath*

Der Pfad für den Prüfpunkt während der Wiederherstellung, wenn an diesem Ziel keine aktive Instanz ausgeführt wird. Dies sollte nicht angegeben werden, wenn die Zielinstanz die zirkuläre Protokollierung verwendet.

*pfn*

Der Statusrückruf, der den Fortschritt der Wiederherstellung meldet.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Der angegebene <em>szTargetInstanceLogPath</em> gehört nicht zu einer initialisierten Instanz. Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Dies weist darauf hin, dass die Datenbank beschädigt oder eine nicht erkannte Datei ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn eine für die Protokolldateien in <em>szBackupLogPath</em>eine Protokollgenerierung über der in <em>genHigh</em> oder <em>pLogInfo.ulGenHigh</em>angegebenen Protokollgenerierung aufweist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Fehler beim Vorgang, weil die angeforderte Datei nicht geöffnet werden konnte, weil sie nicht unter dem angegebenen Pfad gefunden werden konnte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>usw. passieren, wenn <em>szTargetCheckpointPath</em> und <em>szTargetInstanceLogPath</em> entweder nicht beide angegeben oder nicht beide nicht angegeben sind. Das heißt, sie müssen übereinstimmen und sowohl angegeben als auch nicht angegeben werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Fehler beim Vorgang, weil der angegebene Pfad nicht gefunden werden konnte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Fehler beim Vorgang, weil nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abzuschließen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn die während der Wiederherstellung angegebene Datenbankdatei keine Datenbank ist, die mit einer externen Sicherung gesichert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Die Datenbank-Engine kann keine externe Wiederherstellung oder eine harte Wiederherstellung im Einzelinstanzmodus ausführen. Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn eine der Protokolldateien in <em>szBackupLogPath</em>eine Protokollgenerierung unterhalb der durch <em>genLow</em> oder <em>pLogInfo.ulGenLow</em>angegebenen Protokollgenerierung aufweist.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg werden alle Datenbanken aus der *rgrstmap* vollständig wiederhergestellt und befinden sich in einem bereinigten oder konsistenten Zustand. An diesem Punkt kann die Datenbank einer vorhandenen Instanz erneut bereitgestellt werden.

Bei einem Fehler konnte die Engine die Datenbank nicht wiederherstellen. Die Datenbank befindet sich in einem ungültigen Zustand, und um die harte Wiederherstellung zu wiederholen, muss die gesamte Datenbank erneut wiederhergestellt werden. In der Regel ist die Ursache für eine solche Situation eine Datenträger- oder Protokollbeschädigung, eine andere Form der fehlerhaften Verwaltung von Protokollen oder ein nicht kontinuierlicher Protokollsatz.

#### <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter [JetExternalRestore.](./jetexternalrestore-function.md)

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
<td><p>Deklariert in Esent.h.</p></td>
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
<td><p>Wird als <strong>JetExternalRestore2W</strong> (Unicode) und <strong>JetExternalRestore2A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
