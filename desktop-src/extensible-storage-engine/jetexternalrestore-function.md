---
description: 'Weitere Informationen finden Sie hier: jetexternalrestore-Funktion'
title: Jetexternalrestore-Funktion
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
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106373551"
---
# <a name="jetexternalrestore-function"></a>Jetexternalrestore-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetexternalrestore-function"></a>Jetexternalrestore-Funktion

Die **jetexternalrestore** -Funktion stellt eine externe Sicherung wieder her, die mit den externen Backup-APIs erstellt wurde, und gibt einen Bereich von Protokoll Dateinummern an, die während der Wiedergabe wiedergegeben werden. Dies wird als "feste Wiederherstellung" bezeichnet. Dies ähnelt der von der [jetinit](./jetinit-function.md) -Funktion ausgeführten Soft-Wiederherstellung.

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

*szcheckpointfilepath*

Der Pfad für die Prüf Punkt Datei, die während der Wiederherstellung verwendet werden soll, wenn *sztargetinstancecheckpointpath* nicht angegeben ist oder bereits über eine aktive oder ausgeführte Instanz verfügt.

*szlogpath*

Der Pfad oder das Verzeichnis für die Protokolle für die letzte Phase (rückgängig) der Wiederherstellung und möglicherweise für die Roll Forward-Protokolle. Dieser Pfad kann mit dem *szbackuplogpath* identisch sein.

*rgrstmap*

Dies ist ein Array von [JET_RSTMAP](./jet-rstmap-structure.md) Strukturen. Dabei handelt es sich um eine Zuordnung von alten und neuen Daten Bank Pfaden oder Dateinamen. Dies wird verwendet, da die Datenbanken möglicherweise an einem anderen Speicherort als dem Speicherort wieder hergestellt werden müssen, von dem aus Sie gesichert wurden. Wenn mehrere Datenbanken an einen einzelnen protokolliersatz angefügt werden, kann die Restore Map eine Teilmenge der wiederherzustellenden Datenbanken angeben.

*crstfilemap*

Die Anzahl der Einträge im *rgrstmap* -Array Parameter.

*szbackuplogpath*

Der Pfad zu dem Verzeichnis, in dem die Protokolldateien wieder hergestellt werden. Dabei handelt es sich um die Protokolle, die während der externen Sicherungs Sequenz gelesen wurden. Dieser Pfad kann mit dem szlogpath identisch sein.

*genlow*

Die niedrigste Protokolldatei Nummer, die von *szbackuplogpath* wiedergegeben werden soll. Die vollständige Genauigkeit eines langen Zeichens ohne Vorzeichen sollte beibehalten werden, aber in den aktuellen Versionen der Engine ist diese Zahl eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF. Dies kann sich in zukünftigen Versionen ändern.

*genhoch*

Die höchste Protokoll dateizahl, die von *szbackuplogpath* wiedergegeben werden soll. Die vollständige Genauigkeit eines langen Zeichens ohne Vorzeichen sollte beibehalten werden, aber in den aktuellen Versionen der Engine ist diese Zahl eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF. Dies kann sich in zukünftigen Versionen ändern.

*PFN*

Der Status Rückruf, um den Fortschritt der Wiederherstellung zu melden.

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dies kann bei <strong>jetexternalrestore</strong>der Fall sein, wenn " <em>sztargetcheckpointpath</em> " und " <em>sztargetinstancelogpath</em> " nicht beide angegeben oder nicht angegeben sind. Das heißt, Sie müssen abgeglichen werden und beide angegeben oder nicht angegeben werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Dies weist darauf hin, dass die Datenbank beschädigt wurde, oder eine unbekannte Datei.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die angeforderte Datei nicht geöffnet werden konnte, da Sie im angegebenen Pfad nicht gefunden wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da der angegebene Pfad nicht gefunden wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn es sich bei der während der Wiederherstellung angegebenen Datenbankdatei nicht um eine Datenbank handelt, die mit externer Sicherung gesichert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn eine der Protokolldateien im <em>szbackuplogpath</em>eine Protokoll Generierung unterhalb der von <em>genlow</em> oder <em>ploginfo. ulgenlow</em>angegebenen Protokolldateien aufweist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn eine der Protokolldateien im <em>szbackuplogpath</em>die Protokolldateien enthält, die über eine in <em>genhigh</em> oder <em>ploginfo. ulgenhigh</em>angegebene Protokoll Generierung verfügen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>Der angegebene <em>sztargetinstancelogpath</em> gehört nicht zu einer initialisierten Instanz. Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Die Datenbank-Engine kann eine externe Wiederherstellung oder eine feste Wiederherstellung nicht im Single Instance-Modus ausführen. Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg werden alle Datenbanken aus der *rgrstmap* vollständig wieder hergestellt und sind in einem sauberen oder konsistenten Zustand. An diesem Punkt kann die Datenbank erneut an eine vorhandene Instanz bereitgestellt werden.

Bei einem Fehler konnte die Engine die Datenbank nicht wiederherstellen. Die Datenbank befindet sich in einem ungültigen Status. um eine Wiederherstellung zu versuchen, muss die gesamte Datenbank wieder hergestellt werden. In der Regel handelt es sich bei einer solchen Situation um eine Datenträger-oder Protokoll Beschädigung oder eine andere Form der Protokoll Misswirtschaft oder um einen nicht kontinuierlichen Protokoll Satz.

#### <a name="remarks"></a>Bemerkungen

Um zu verstehen, wie eine "harte" Wiederherstellung funktioniert, müssen Sie verstehen, dass es drei Phasen der Wiederherstellung gibt und die zweite Phase zwei Teile haben kann. In Phase I sind Protokolle erforderlich, um eine gesicherte Datenbank in Konsistenz zu bringen (oder es kann ein ursprünglicher Satz inkrementeller Protokolle verwendet werden). In Phase II werden alle verfügbaren zusätzlichen Roll Forward-Protokolle genutzt, um die Datenbank konsistent zu machen. Außerdem gibt es eine Wiedergabe der zusätzlichen rollforwardprotokolle. Phase III ist die Roll Back Phase der Wiederherstellung.

Phase I: die Wiedergabe des Satzes von Protokollen, die wieder hergestellt werden müssen, damit die Datenbank in einen konsistenten Status (oder einen anfänglichen Satz von Protokolldateien) gebracht wird. Im Grunde handelt es sich hierbei um die Wiedergabe des Satzes von Protokolldateien, die für die wiederherzustellenden Datenbanken nicht optional sind. Wenn in diesem Bereich von Protokollen fehlende Protokolle vorhanden sind, tritt bei der Wiederherstellung ein Fehler auf. Diese Protokolle sollten in dem Verzeichnis abgelegt werden, das im Parameter " *szbackuplogpath* " angegeben ist.

Phase II: Optional können Protokolldateien, die aus inkrementellen oder differenziellen Sicherungen und aus den Protokolldateien einer aktiven Instanz stammen, über eine Reihe von Protokolldateien verfügen. Im Fall von Protokolldateien aus inkrementellen oder differenziellen Sicherungen können die Protokolldateien in den Verzeichnissen abgelegt werden, die entweder in den Parametern *szbackuplogpath* oder *sztargetinstancelogpath* angegeben sind, wobei das erste das empfohlene Verzeichnis ist. Die Protokolle, die für die Rollforwardphase (Phase II) verwendet werden, sollten aus derselben Reihe von Protokollen stammen, die während der Phase i abgespielt wurden, und sollten die Protokoll Nummern kontinuierlich erhöhen, ohne dass Lücken aus der Phase i protokolliert werden. Um eine Datenbank vollständig auf dem neuesten Stand zu halten, um die Protokolldateien zu verwenden, die derzeit von einer aktiven Instanz verwendet werden, müssen die Parameter *sztargetinstancelogpath* und *sztargetinstancecheckpointpath* angegeben werden. Dies ist auch dann möglich, wenn andere Datenbanken an diesen Protokoll Satz angefügt sind.

Phase III: in der letzten Wiederherstellungs Phase wird für alle Transaktionen, für die kein Commit ausgeführt wurde, ein Rollback ausgeführt. hierfür müssen neue Protokolldateien erstellt und die Prüf Punkt Datei aktualisiert werden. Diese Phase wird manchmal als "Rückgängig" bezeichnet. Der in dieser Phase zu verwendende Pfad der Prüf Punkt Datei ist der Pfad analog zum Protokoll Speicherort in Phase III, d. h., wenn *szlogpath* für Phase III verwendet wird, wird *szcheckpointfilepath* verwendet, wenn " *sztargetinstancelogpath* " für Phase III der Wiederherstellungs Sitzung " *sztargetinstancecheckpointpath* " verwendet wird.

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
<td><p>Implementiert als <strong>jetexternalrestorew</strong> (Unicode) und <strong>jetexternalrestorea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[Jetbeginexternalbackup](./jetbeginexternalbackup-function.md)  
[JetInit](./jetinit-function.md)
