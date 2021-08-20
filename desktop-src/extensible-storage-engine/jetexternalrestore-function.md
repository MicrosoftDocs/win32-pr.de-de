---
description: Weitere Informationen finden Sie unter JetExternalRestore-Funktion.
title: JetExternalRestore-Funktion
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4844c14d6b60e5825b3b09f58b0d756e83b0f41c4e743684a29607a814d4f16f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118072823"
---
# <a name="jetexternalrestore-function"></a>JetExternalRestore-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetexternalrestore-function"></a>JetExternalRestore-Funktion

Die **JetExternalRestore-Funktion** stellt eine externe Sicherung wieder her, die mit den externen Sicherungs-APIs erstellt wurde, und gibt einen Bereich von Protokolldateinummern an, die während des Wiederherstellungsvorgangs wiedergegeben werden. Dies wird als harte Wiederherstellung bezeichnet, die ähnlich wie die von der JetInit-Funktion durchgeführte wie die weiche [Wiederherstellung ist.](./jetinit-function.md)

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a>Parameter

*szCheckpointFilePath*

Der Pfad für die Prüfpunktdatei, die während der Wiederherstellung verwendet werden soll, wenn *szTargetInstanceCheckpointPath* nicht angegeben ist oder bereits über eine aktive oder ausgeführte Instanz verfügt.

*szLogPath*

Der Pfad oder das Verzeichnis für die Protokolle für die letzte Phase (Rückgängig) der Wiederherstellung und möglicherweise für die Roll forward-Protokolle. Dieser Pfad kann mit dem *szBackupLogPath identisch sein.*

*rgrstmap*

Dies ist ein Array [JET_RSTMAP](./jet-rstmap-structure.md) Strukturen. Dies ist eine Zuordnung alter und neuer Datenbankpfade oder Dateinamen. Dies wird verwendet, da die Datenbanken möglicherweise an einem anderen Speicherort als dem Speicherort wiederhergestellt werden müssen, von dem sie gespeichert wurden. Wenn mehrere Datenbanken an einen einzelnen Protokollierungssatz angefügt sind, kann die Wiederherstellungszuordnung eine Teilmenge der wiederherzustellenden Datenbanken angeben.

*crstfilemap*

Die Anzahl der Einträge im *rgrstmap-Arrayparameter.*

*szBackupLogPath*

Der Pfad zu dem Verzeichnis, in dem die Protokolldateien wiederhergestellt werden. Dies sind die Protokolle, die während der externen Sicherungssequenz ausgelesen wurden. Dieser Pfad kann mit dem szLogPath identisch sein.

*genLow*

Die niedrigste Protokolldateinummer, die von *szBackupLogPath wiedergegeben werden soll.* Die vollständige Genauigkeit eines long-Werts ohne Vorzeichen sollte beibehalten werden, aber in aktuellen Versionen der Engine ist diese Zahl eine Hexadezimalzahl im Bereich von 0x00000 bis 0xFFFFF. Dies kann sich in zukünftigen Versionen ändern.

*genHigh*

Die höchste Protokolldateinummer, die von *szBackupLogPath* wiedergegeben werden soll. Die vollständige Genauigkeit eines long-Werts ohne Vorzeichen sollte beibehalten werden, aber in aktuellen Versionen der Engine ist diese Zahl eine Hexadezimalzahl im Bereich von 0x00000 bis 0xFFFFF. Dies kann sich in zukünftigen Versionen ändern.

*pfn*

Der Statusrückruf, um den Fortschritt der Wiederherstellung zu melden.

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>Fehler beim Vorgang, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abschließen zu können.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetExternalRestore</strong>und so weiter geschehen, wenn <em>szTargetCheckpointPath</em> und <em>szTargetInstanceLogPath</em> entweder nicht beide angegeben sind oder nicht beide nicht angegeben sind. Das heißt, sie müssen übereinstimmen und sowohl angegeben als auch beide nicht angegeben sein.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Dies weist darauf hin, dass die Datenbank beschädigt oder eine unbekannte Datei war.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Fehler beim Vorgang, da die angeforderte Datei nicht geöffnet werden konnte, weil sie unter dem angegebenen Pfad nicht gefunden wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>Fehler beim Vorgang, weil der angegebene Pfad nicht gefunden werden konnte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn die während der Wiederherstellung angegebene Datenbankdatei keine Datenbank ist, die mit einer externen Sicherung gesichert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn eine der Protokolldateien in <em>szBackupLogPath</em>eine Protokollgenerierung unter der von <em>genLow</em> oder <em>pLogInfo.ulGenLow</em>angegebenen hat.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn eine für die Protokolldateien in <em>szBackupLogPath</em>eine Protokollgenerierung über der in <em>genHigh</em> oder <em>pLogInfo.ulGenHigh angegebenen hat.</em></p></td>
</tr>
<tr class="even">
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>Der <em>angegebene szTargetInstanceLogPath</em> gehört nicht zu einer initialisierten Instanz. Dieser Fehler wird nur in xp Windows und höher zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Die Datenbank-Engine kann keine externe Wiederherstellung oder harte Wiederherstellung im Einzelinstanzmodus ausführen. Dieser Fehler wird nur in xp Windows und höher zurückgegeben.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg werden alle Datenbanken aus *der rgrstmap* vollständig wiederhergestellt und befinden sich in einem sauberen oder konsistenten Zustand. An diesem Punkt kann die Datenbank erneut in eine vorhandene Instanz bereitgestellt werden.

Bei einem Fehler konnte die Engine die Datenbank nicht wiederherstellen. Die Datenbank befindet sich in einem ungültigen Zustand, und um die wiederherzustellende Wiederherstellung zu wiederholen, muss die gesamte Datenbank erneut wiederhergestellt werden. In der Regel ist die Ursache einer solchen Situation eine Beschädigung des Datenträgers oder Protokolls, eine andere Form der Protokollfehlverwaltung oder ein nicht kontinuierlicher Protokollsatz.

#### <a name="remarks"></a>Hinweise

Um zu verstehen, wie eine "harte" Wiederherstellung funktioniert, müssen Sie verstehen, dass es drei Phasen der Wiederherstellung gibt und die zweite Phase aus zwei Teilen besteht. In Phase I sind Protokolle erforderlich, um eine datenbanksicherungskonsistente Datenbank zu gewährleisten (oder ein erster Satz inkrementeller Protokolle kann verwendet werden). In Phase II werden alle verfügbaren zusätzlichen Roll forward-Protokolle verwendet, um die Datenbank konsistent zu machen. Es gibt auch eine Wiedergabe der zusätzlichen Roll forward-Protokolle. Phase III ist die Rückgängig-Phase der Wiederherstellung.

Phase I: Die Wiedergabe der Protokolle, die wiederhergestellt werden müssen, damit die Datenbank in einen konsistenten Zustand (oder einen anfänglichen Satz von Protokolldateien) gebracht werden kann, wird ausgeführt. Im Grunde ist dies die Wiedergabe der Protokolldateien, die für die wiederherzustellenden Datenbanken nicht optional sind. Wenn Protokolle aus diesem Protokollbereich fehlen, kann die Wiederherstellung nicht wiederhergestellt werden. Diese Protokolle sollten in dem Verzeichnis gespeichert werden, das im *szBackupLogPath-Parameter angegeben* ist.

Phase II: Optional gibt es einige Protokolldateien, bei denen es sich um Rollfor forward-Protokolldateien handelt, die aus inkrementellen oder differenziellen Sicherungen und aus den Protokolldateien einer aktiven Instanz stammen. Im Fall von Protokolldateien aus inkrementellen oder differenziellen Sicherungen können die Protokolldateien in den Verzeichnissen platziert werden, die entweder in den *SzBackupLogPath-* oder *szTargetInstanceLogPath-Parametern* angegeben sind, während ersteres das empfohlene Verzeichnis ist. Die protokolle, die für die Roll forward-Phase (Phase II) verwendet werden, sollten aus derselben Reihe von Protokollen stammen, die in Phase I abgespielt wurden, und sollten kontinuierlich inkrementierende Protokollnummern ohne Lücken aus den Phase-I-Protokollen aufweisen. Damit eine Datenbank mit den Protokolldateien, die derzeit von einer aktiven Instanz verwendet werden, vollständig auf dem neuesten Stand ist, müssen die Parameter *szTargetInstanceLogPath* und *szTargetInstanceCheckpointPath* angegeben werden. Dies kann auch dann erfolgen, wenn andere Datenbanken an diesen Protokollsatz angefügt sind.

Phase III: In der letzten Phase der Wiederherstellung wird für alle Transaktionen, für die keinComcommitted-Fehler erforderlich ist, ein Rollback für alle Transaktionen verwendet. Dazu müssen neue Protokolldateien generiert und die Prüfpunktdatei aktualisiert werden. Diese Phase wird manchmal als "Rückgängig" bezeichnet. Der prüfpunktdateipfad, der während dieser Phase verwendet werden soll, entspricht dem Protokollspeicherort der Phase III. Wenn *szLogPath* für Phase III verwendet wird, wird *szCheckpointFilePath* verwendet, wenn *szTargetInstanceLogPath* für Phase III der Wiederherstellung *szTargetInstanceCheckpointPath* verwendet wird.

Verwenden Sie dieses Flussdiagramm, um zu verstehen, wie die Pfade funktionieren:

![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JetExternalRestoreW</strong> (Unicode) und <strong>JetExternalRestoreA</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetInit](./jetinit-function.md)
