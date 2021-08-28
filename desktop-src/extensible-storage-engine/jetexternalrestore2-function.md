---
description: Weitere Informationen finden Sie unter JetExternalRestore2-Funktion.
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
ms.openlocfilehash: adceb414fdea434f84178a6e4f0b8b33838e954d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987433"
---
# <a name="jetexternalrestore2-function"></a>JetExternalRestore2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetexternalrestore2-function"></a>JetExternalRestore2-Funktion

Die **JetExternalRestore2-Funktion** stellt eine externe Sicherung wieder her, die mit den externen Sicherungs-APIs erstellt wurde, und stellt Prüfpunkte für zirkuläre Protokollierungsvorgänge zur Verfügung. Dies wird als harte Wiederherstellung bezeichnet, die ähnlich ist, sich aber von der soft-Wiederherstellung abschneiden kann, wie sie von der [JetInit-Funktion ausgeführt](./jetinit-function.md) wird.

**Windows XP: JetExternalRestore2** wird in xp Windows eingeführt.

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

Der Pfad für die Prüfpunktdatei, der während der Wiederherstellung verwendet werden soll, wenn *szTargetInstanceCheckpointPath* nicht angegeben ist oder dieser Pfad über eine aktive oder ausgeführte Instanz verfügt.

*szLogPath*

Der Pfad oder das Verzeichnis für die Protokolle für die letzte Phase (Rückgängig) der Wiederherstellung und möglicherweise für die Roll forward-Protokolle. Dieser Pfad kann mit dem *szBackupLogPath identisch sein.*

*rgrstmap*

Dies ist ein Array von [JET_RSTMAP](./jet-rstmap-structure.md) Strukturen. Dies ist eine Zuordnung alter und neuer Datenbankpfade oder Dateinamen. Dies wird verwendet, da die Datenbanken möglicherweise an einem anderen Speicherort als dem Speicherort wiederhergestellt werden müssen, von dem sie gespeichert wurden. Wenn mehrere Datenbanken an einen einzelnen Protokollierungssatz angefügt sind, kann die Wiederherstellungszuordnung eine Teilmenge der wiederherzustellenden Datenbanken angeben.

*crstfilemap*

Die Anzahl der Einträge im *rgrstmap-Arrayparameter.*

*szBackupLogPath*

Der Pfad zu dem Verzeichnis, in dem die Protokolldateien wiederhergestellt werden. Dies sind die Protokolle, die während der externen Sicherungssequenz ausgelesen wurden. Dieser Pfad kann mit dem *szLogPath* identisch sein.

*pLogInfo*

*pLogInfo* beschreibt mehrere Aspekte der Sicherungsprotokolle für die Wiederherstellung. Mit diesem Parameter kann **JetExternalRestore2** die expliziten Parameter *genLow* und *genHigh* von **JetExternalRestore2** sowie den Basisprotokollnamen anstelle des vermuteten Protokollbasisnamens "edb" verwenden.

*szTargetInstanceName*

Dieser Parameter ist veraltet und kann nicht in Ihrer Anwendung verwendet werden.

*szTargetInstanceLogPath*

Der Pfad für die Roll forward-Protokolle, wenn sich der Speicherort der Protokolle, für die Sie einen Rollover erstellen möchten, in einem aktiven Protokollierungssatz oder einer aktiven Instanz befindet. Dies sollte nicht angegeben werden, wenn die Zielinstanz zirkuläre Protokollierung verwendet.

*szTargetInstanceCheckpointPath*

Der Pfad für den Prüfpunkt während der Wiederherstellung, wenn auf diesem Ziel keine aktive Instanz ausgeführt wird. Dies sollte nicht angegeben werden, wenn die Zielinstanz zirkuläre Protokollierung verwendet.

*pfn*

Der Statusrückruf, der den Fortschritt der Wiederherstellung meldet.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBadRestoreTargetInstance</p> | <p>Der <em>angegebene szTargetInstanceLogPath</em> gehört nicht zu einer initialisierten Instanz. Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</p> | 
| <p>JET_errDatabaseCorrupted</p> | <p>Dies weist darauf hin, dass die Datenbank beschädigt oder eine unbekannte Datei war.</p> | 
| <p>JET_errEndingRestoreLogTooLow</p> | <p>Dieser Fehler wird zurückgegeben, wenn eine Protokollgenerierung für die Protokolldateien in <em>szBackupLogPath</em>über der in <em>genHigh</em> oder <em>pLogInfo.ulGenHigh angegebenen Protokollgenerierung verfügt.</em></p> | 
| <p>JET_errFileNotFound</p> | <p>Fehler beim Vorgang, da die angeforderte Datei nicht geöffnet werden konnte, weil sie unter dem angegebenen Pfad nicht gefunden wurde.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>und so weiter geschehen, wenn <em>szTargetCheckpointPath</em> und <em>szTargetInstanceLogPath</em> entweder nicht beide angegeben sind oder nicht beide nicht angegeben sind. Das heißt, sie müssen übereinstimmen und sowohl angegeben als auch beide nicht angegeben sein.</p> | 
| <p>JET_errInvalidPath</p> | <p>Fehler beim Vorgang, weil der angegebene Pfad nicht gefunden werden konnte.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abschließen zu können.</p> | 
| <p>JET_errRestoreOfNonBackupDatabase</p> | <p>Dieser Fehler wird zurückgegeben, wenn die während der Wiederherstellung angegebene Datenbankdatei keine Datenbank ist, die mit einer externen Sicherung gesichert wurde.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Die Datenbank-Engine kann keine externe Wiederherstellung oder harte Wiederherstellung im Einzelinstanzmodus ausführen. Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</p> | 
| <p>JET_errStartingRestoreLogTooHigh</p> | <p>Dieser Fehler wird zurückgegeben, wenn eine der Protokolldateien in <em>szBackupLogPath</em>eine Protokollgenerierung unter der von <em>genLow</em> oder <em>pLogInfo.ulGenLow</em>angegebenen hat.</p> | 



Bei Erfolg werden alle Datenbanken aus *der rgrstmap* vollständig wiederhergestellt und befinden sich in einem sauberen oder konsistenten Zustand. An diesem Punkt kann die Datenbank erneut in eine vorhandene Instanz bereitgestellt werden.

Bei einem Fehler konnte die Engine die Datenbank nicht wiederherstellen. Die Datenbank befindet sich in einem ungültigen Zustand, und um die wiederherzustellende Wiederherstellung zu wiederholen, muss die gesamte Datenbank erneut wiederhergestellt werden. In der Regel ist die Ursache einer solchen Situation eine Beschädigung des Datenträgers oder Protokolls, eine andere Form der Protokollfehlverwaltung oder ein nicht kontinuierlicher Protokollsatz.

#### <a name="remarks"></a>Bemerkungen

Weitere Informationen [finden Sie unter JetExternalRestore.](./jetexternalrestore-function.md)

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetExternalRestore2W</strong> (Unicode) und <strong>JetExternalRestore2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
