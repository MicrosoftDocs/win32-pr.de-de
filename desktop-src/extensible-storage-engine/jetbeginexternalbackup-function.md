---
description: Weitere Informationen finden Sie in der jetbeginexternalbackup-Funktion.
title: Jetbeginexternalbackup-Funktion
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d410adb592c3d56d2f9880ec809749396318258a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351076"
---
# <a name="jetbeginexternalbackup-function"></a>Jetbeginexternalbackup-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbeginexternalbackup-function"></a>Jetbeginexternalbackup-Funktion

Die **jetbeginexternalbackup** -Funktion initiiert eine externe Sicherung, während die Engine und die Datenbank online und aktiv sind. **Jetbeginexternalbackup** ist das erste in einer Reihe von Funktionen, die aufgerufen werden müssen, um eine erfolgreiche (nicht auf VSS basierende) Online Sicherung auszuführen.

Eine externe Sicherung kann zum Implementieren von vollständigen, inkrementellen oder differenziellen Sicherungen verwendet werden.

Bei der Sicherung handelt es sich um einen fuzzywert, da die Sicherung mit einem bestimmten Zeitpunkt im Transaktionsverlauf konsistent ist, aber das Steuern des genauen Zeitraums nicht möglich ist.

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angeben.

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
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Dieses Flag ist veraltet. Die Verwendung dieses Bits führt dazu, dass JET_errInvalidgrbit zurückgegeben wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Erstellt im Gegensatz zu einer vollständigen Sicherung eine inkrementelle Sicherung. Dies bedeutet, dass nur die Protokolldateien seit der letzten vollständigen oder inkrementellen Sicherung gesichert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Für die zukünftige Verwendung reserviert. Definiert für Windows XP.</p></td>
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
<td><p>JET_errBackupInProgress</p></td>
<td><p>Wenn bereits eine externe Sicherung oder Momentaufnahme Sicherung in Verarbeitung ist, wird dieser Fehler zurückgegeben, bis <strong>jetbeginexternalbackup</strong> (oder eine der Varianten davon) aufgerufen wird. ESE ermöglicht jeweils nur eine Online Sicherung.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>Die Instanz oder Datenbank-Engine befindet sich entweder in der Wiederherstellung oder in einer Beendigungs-oder Beendigungs Phase.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointCorrupt</p></td>
<td><p>Bei einer vollständigen Sicherung konnte die Prüf Punkt Datei nicht gelesen werden, oder die Datei konnte nicht überprüft werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCheckpointFileNotFound</p></td>
<td><p>Bei einer vollständigen Sicherung konnte die Prüf Punkt Datei nicht gefunden werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da der-Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>Die zirkuläre Protokollierung ist aktiviert, und der angegebene Sicherungstyp ist JET_bitBackupIncremental. Informationen dazu, wie Sie zirkuläre oder nicht zirkuläre Protokollierung steuern, finden Sie unter <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> in den <strong>Transaktionsprotokoll Fehlern</strong> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Mindestens ein <em>grbit</em> -Member war ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLoggingDisabled</p></td>
<td><p>Wiederherstellung oder Protokollierung ist deaktiviert. Wenn die Protokollierung deaktiviert ist, können Sie keine Online Sicherung durchführen. Weitere Informationen zur Protokollierung und Wiederherstellung finden Sie unter <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogWriteFail</p></td>
<td><p>Die Engine hat das Schreiben auf das Protokoll Laufwerk beendet, da die Protokolldatei voll ist oder die e/a-Fehler aufgetreten sind.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFullBackup</p></td>
<td><p>Die inkrementelle Sicherung wurde angegeben (mit JET_bitBackupIncremental), und nie war eine vollständige Sicherung für eine der angefügten Datenbanken für den Protokollierungs Satz.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn die Funktion erfolgreich ausgeführt wird, wird eine externe Sicherung initiiert, und die Sicherungs Zustands-Engine wird initialisiert. Nachfolgende APIs können jetzt aufgerufen werden, um die externe Sicherungs Sequenz und den Stream abzuschließen oder die Datenbankdatei, die Datenbank-Patchdatei (falls unterstützt) und die Protokolldatei auszulesen. Ein Ereignis kann protokolliert werden, dass eine externe Sicherung begonnen hat.

Wenn die Funktion fehlschlägt, wird die Sicherungs Sitzung nicht initiiert. Wenn eine andere Sicherungs Sitzung ausgeführt wird, wird Sie nicht abgebrochen.

#### <a name="remarks"></a>Bemerkungen

Der externe Sicherungsprozess (wie von **jetbeginexternalbackup** gestartet) ist so konzipiert, dass eine Fuzzy Transaction-Online Sicherung der gesamten Instanz auf einem Zielgerät als Stream zulässig ist. Die Sicherung enthält alle Datenbankdateien, die mithilfe von [jetattachdatabase](./jetattachdatabase-function.md) (für eine vollständige Sicherung) an die Instanz angefügt sind, gefolgt von den zugehörigen datenbankpatchdateien (falls unterstützt), und schließlich von den Transaktionsprotokoll Dateien, die während des Sicherungs Vorgangs generiert wurden. Das Endergebnis ist ein Satz von Dateien, der aus dem Stream wieder hergestellt werden kann, möglicherweise mit vorhandenen Datenbank-und Protokolldateien kombiniert und schließlich in einem konsistenten Zustand wieder hergestellt wird.

Die allgemeine Reihenfolge von Vorgängen für eine vollständige Sicherung besteht aus den folgenden aufrufen. Zuerst wird **jetbeginexternalbackup** aufgerufen, um den Sicherungsprozess zu starten. Anschließend wird [jetgetattachinfo](./jetgetattachinfo-function.md) aufgerufen, um die Liste der Datenbanken zu erhalten, die an die zu sichernde Instanz angefügt sind. Für jede dieser Datenbanken wird [jetopumfile](./jetopenfile-function.md) aufgerufen, gefolgt von einer Reihe von [jetreadfile](./jetreadfile-function.md) -aufrufen und dann durch einen Aufruf von [jetclosefile](./jetclosefile-function.md). Anschließend wird [jetgetloginfo](./jetgetloginfo-function.md) aufgerufen, um eine Liste der zu sichernden datenbankpatch-und-Protokolldateien zu erhalten. Für jede dieser Dateien wird eine weitere Abfolge von [jetopenfile](./jetopenfile-function.md)-, [jetreadfile](./jetreadfile-function.md)-und [jetclosefile](./jetclosefile-function.md) -aufrufen durchgeführt. Anschließend werden alle unerwünschten Transaktionsprotokoll Dateien mithilfe von [jettruneurelog](./jettruncatelog-function.md)gelöscht. Schließlich wird die Sicherung durch einen [calltendexternalbackup](./jetendexternalbackup-function.md)-Befehl beendet.

Es ist auch möglich, diesen Satz von Schritten zu ändern, um eine inkrementelle Sicherung der-Instanz auszuführen. Eine inkrementelle Sicherung listet Protokolldateien auf und sichert Sie. Inkrementelle Sicherungen sind nur möglich, wenn zirkuläre Protokollierung nicht aktiviert ist

Es ist auch möglich, diesen Satz von Schritten so zu ändern, dass nachfolgende differenzielle Sicherungen der Instanz ausgeführt werden können. Um eine differenzielle Sicherung auszuführen, nennen Sie [jettruneurelog](./jettruncatelog-function.md) nicht in der vorherigen vollständigen oder inkrementellen Sicherung. Durch das Aufrufen von [jettruneurelog](./jettruncatelog-function.md)können nachfolgende Sicherungen in Bezug auf die letzte vollständige oder inkrementelle Sicherung differenziell sein. Differenzielle Sicherungen sind nur möglich, wenn die zirkuläre Protokollierung nicht aktiviert ist.

Die Datenbank-Patchdatei ist eine spezielle Hilfsdatei, die zum Speichern von Datenbankseiten Images unter bestimmten Umständen während der Sicherung verwendet wird. Diese Datei muss bei einem Wiederherstellungs Vorgang am gleichen Speicherort wie die zugehörige Datenbank vorhanden sein. Diese Datei wird nur in Windows 2000 verwendet. Daher müssen alle Anwendungen, die für Windows 2000 und andere Releases geschrieben werden, Daten Bank Patchdateien unterstützen, wenn Sie vorhanden sind, aber auch nicht fehlschlagen dürfen, wenn Sie nicht vorhanden sind.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetattachdatabase](./jetattachdatabase-function.md)  
[Jetbeginexternalbackupinstance](./jetbeginexternalbackupinstance-function.md)  
[Jetclosefile](./jetclosefile-function.md)  
[Jetendexternalbackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[Jetgetattachinfo](./jetgetattachinfo-function.md)  
[Jetgetloginfo](./jetgetloginfo-function.md)  
[Jetopumfile](./jetopenfile-function.md)  
[Jetreadfile](./jetreadfile-function.md)  
[Jetstopbackup](./jetstopbackup-function.md)  
[Jettruneurelog](./jettruncatelog-function.md)
