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
ms.openlocfilehash: ad8cad0cfc31c77b3cc8e960153bda14b4f431e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475816"
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


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBadRestoreTargetInstance</p> | <p>Der angegebene <em>szTargetInstanceLogPath</em> gehört nicht zu einer initialisierten Instanz. Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</p> | 
| <p>JET_errDatabaseCorrupted</p> | <p>Dies weist darauf hin, dass die Datenbank beschädigt oder eine nicht erkannte Datei ist.</p> | 
| <p>JET_errEndingRestoreLogTooLow</p> | <p>Dieser Fehler wird zurückgegeben, wenn eine für die Protokolldateien in <em>szBackupLogPath</em>eine Protokollgenerierung über der in <em>genHigh</em> oder <em>pLogInfo.ulGenHigh</em>angegebenen Protokollgenerierung aufweist.</p> | 
| <p>JET_errFileNotFound</p> | <p>Fehler beim Vorgang, weil die angeforderte Datei nicht geöffnet werden konnte, weil sie nicht unter dem angegebenen Pfad gefunden werden konnte.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>usw. passieren, wenn <em>szTargetCheckpointPath</em> und <em>szTargetInstanceLogPath</em> entweder nicht beide angegeben oder nicht beide nicht angegeben sind. Das heißt, sie müssen übereinstimmen und sowohl angegeben als auch nicht angegeben werden.</p> | 
| <p>JET_errInvalidPath</p> | <p>Fehler beim Vorgang, weil der angegebene Pfad nicht gefunden werden konnte.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, weil nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</p> | 
| <p>JET_errRestoreOfNonBackupDatabase</p> | <p>Dieser Fehler wird zurückgegeben, wenn die während der Wiederherstellung angegebene Datenbankdatei keine Datenbank ist, die mit einer externen Sicherung gesichert wurde.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Die Datenbank-Engine kann keine externe Wiederherstellung oder eine harte Wiederherstellung im Einzelinstanzmodus ausführen. Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</p> | 
| <p>JET_errStartingRestoreLogTooHigh</p> | <p>Dieser Fehler wird zurückgegeben, wenn eine der Protokolldateien in <em>szBackupLogPath</em>eine Protokollgenerierung unterhalb der durch <em>genLow</em> oder <em>pLogInfo.ulGenLow</em>angegebenen Protokollgenerierung aufweist.</p> | 



Bei Erfolg werden alle Datenbanken aus der *rgrstmap* vollständig wiederhergestellt und befinden sich in einem bereinigten oder konsistenten Zustand. An diesem Punkt kann die Datenbank einer vorhandenen Instanz erneut bereitgestellt werden.

Bei einem Fehler konnte die Engine die Datenbank nicht wiederherstellen. Die Datenbank befindet sich in einem ungültigen Zustand, und um die harte Wiederherstellung zu wiederholen, muss die gesamte Datenbank erneut wiederhergestellt werden. In der Regel ist die Ursache für eine solche Situation eine Datenträger- oder Protokollbeschädigung, eine andere Form der fehlerhaften Verwaltung von Protokollen oder ein nicht kontinuierlicher Protokollsatz.

#### <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter [JetExternalRestore.](./jetexternalrestore-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetExternalRestore2W</strong> (Unicode) und <strong>JetExternalRestore2A</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
