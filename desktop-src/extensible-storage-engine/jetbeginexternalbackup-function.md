---
description: Weitere Informationen finden Sie unter JetBeginExternalBackup-Funktion.
title: JetBeginExternalBackup-Funktion
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
ms.openlocfilehash: 8d0e47a117c044899a8b078290be622cfecdae91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482906"
---
# <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup-Funktion

Die **JetBeginExternalBackup-Funktion** initiiert eine externe Sicherung, während die Engine und die Datenbank online und aktiv sind. **JetBeginExternalBackup** ist das erste in einer Reihe von Funktionen, die aufgerufen werden müssen, um eine erfolgreiche Onlinesicherung (nicht VSS-basiert) auszuführen.

Eine externe Sicherung kann verwendet werden, um vollständige, inkrementelle oder differenzielle Sicherungen zu implementieren.

Die Sicherung ist fuzzy, da die Sicherung mit einem einzelnen Zeitpunkt im Transaktionsverlauf konsistent ist, aber die Steuerung des genauen Zeitpunkts nicht möglich ist.

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angeben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Dieses Flag ist veraltet. Die Verwendung dieses Bit führt dazu, dass JET_errInvalidgrbit zurückgegeben wird.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Erstellt eine inkrementelle Sicherung im Gegensatz zu einer vollständigen Sicherung. Dies bedeutet, dass nur die Protokolldateien seit der letzten vollständigen oder inkrementellen Sicherung gesichert werden.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Für die zukünftige Verwendung reserviert. Definiert für Windows XP.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Wenn bereits eine externe Sicherung oder Momentaufnahmesicherung erstellt wird, wird dieser Fehler zurückgegeben, bis <strong>JetBeginExternalBackup</strong> (oder eine der Varianten davon) aufgerufen wird. ESE lässt immer nur eine Onlinesicherung zu.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>Die Instanz oder Datenbank-Engine befindet sich entweder in der Wiederherstellungsphase oder in einer Phase zum Herunterfahren oder Beenden.</p> | 
| <p>JET_errCheckpointCorrupt</p> | <p>Bei einer vollständigen Sicherung konnte die Prüfpunktdatei nicht gelesen werden, oder die Datei konnte nicht überprüft werden.</p> | 
| <p>JET_errCheckpointFileNotFound</p> | <p>Bei einer vollständigen Sicherung konnte die Prüfpunktdatei nicht gefunden werden.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die -Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong> Dieser Rückgabewert wird in xp Windows eingeführt.</p> | 
| <p>JET_errInvalidBackup</p> | <p>Die Zirkelprotokollierung ist aktiviert, und der angegebene Sicherungstyp JET_bitBackupIncremental. Informationen <a href="gg269235(v=exchg.10).md">zum Steuern der</a> zirkulären oder nicht zirkulären Protokollierung finden Sie unter JET_paramCircularLog in den Transaktionsprotokollfehlern. <strong></strong></p> | 
| <p>JET_errInvalidgrbit</p> | <p>Mindestens ein <em>Grbit-Member</em> war ungültig.</p> | 
| <p>JET_errLoggingDisabled</p> | <p>Wiederherstellung oder Protokollierung ist deaktiviert. Sie können keine Onlinesicherung durchführen, wenn die Protokollierung deaktiviert ist. Weitere Informationen zur Protokollierung und Wiederherstellung finden Sie unter <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</p> | 
| <p>JET_errLogWriteFail</p> | <p>Die Engine hat das Schreiben auf das Protokolllaufwerk beendet, weil das Protokoll voll ist oder Datenträger-E/A-Fehler aufgetreten sind.</p> | 
| <p>JET_errMissingFullBackup</p> | <p>Die inkrementelle Sicherung wurde angegeben (mit JET_bitBackupIncremental), und es wurde nie eine vollständige Sicherung für eine der angefügten Datenbanken für den Protokollierungssatz erstellt.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abschließen zu können.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, bei dem nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 



Wenn die Funktion erfolgreich ist, wird eine externe Sicherung initiiert und die Engine für den Sicherungsstatus initialisiert. Nachfolgende APIs können jetzt aufgerufen werden, um die externe Sicherungssequenz zu vervollständigen und die Datenbankdatei, die Datenbankpatchdatei (sofern unterstützt) und die Protokolldatei zu streamen oder daraus zu lesen. Ein Ereignis kann protokolliert werden, dass eine externe Sicherung begonnen hat.

Wenn die Funktion fehlschlägt, wird die Sicherungssitzung nicht initiiert. Wenn eine weitere Sicherungssitzung in Bearbeitung ist, wird sie nicht abgebrochen.

#### <a name="remarks"></a>Hinweise

Der externe Sicherungsprozess (wie von **JetBeginExternalBackup** gestartet) ist so konzipiert, dass eine Fuzzytransaktions-Onlinesicherung der gesamten Instanz auf einem Zielgerät als Stream möglich ist. Die Sicherung enthält alle Datenbankdateien, die mit [JetAttachDatabase](./jetattachdatabase-function.md) (für eine vollständige Sicherung), gefolgt von den zugehörigen Datenbankpatchdateien (sofern unterstützt) und schließlich den Transaktionsprotokolldateien, die während des Sicherungsprozesses generiert wurden, an die Instanz angefügt sind. Das Endergebnis ist ein Satz von Dateien, die aus dem Stream wiederhergestellt werden können, möglicherweise in Kombination mit vorhandenen Datenbank- und Protokolldateien, und schließlich in einem konsistenten Zustand wiederhergestellt werden können.

Die allgemeine Reihenfolge der Vorgänge für eine vollständige Sicherung besteht aus den folgenden Aufrufen. Zunächst wird **JetBeginExternalBackup** aufgerufen, um den Sicherungsprozess zu starten. Anschließend wird [JetGetAttachInfo aufgerufen,](./jetgetattachinfo-function.md) um die Liste der Datenbanken zu erhalten, die an die zu sichernde Instanz angefügt sind. Für jede dieser Datenbanken wird [JetOpenFile](./jetopenfile-function.md) aufgerufen, gefolgt von einer Reihe von [JetReadFile-Aufrufen](./jetreadfile-function.md) und dann einem Aufruf von [JetCloseFile.](./jetclosefile-function.md) Anschließend wird [JetGetLogInfo aufgerufen,](./jetgetloginfo-function.md) um eine Liste der zu sichernden Datenbankpatch- und Protokolldateien zu erhalten. Für jede dieser Dateien wird eine weitere Sequenz von [JetOpenFile-,](./jetopenfile-function.md) [JetReadFile-](./jetreadfile-function.md)und [JetCloseFile-Aufrufen](./jetclosefile-function.md) ausgeführt. Anschließend werden alle unerwünschten Transaktionsprotokolldateien mit [JetTruncateLog gelöscht.](./jettruncatelog-function.md) Schließlich wird die Sicherung durch einen Aufruf von [JetEndExternalBackup beendet.](./jetendexternalbackup-function.md)

Es ist auch möglich, diesen Satz von Schritten zu ändern, um eine inkrementelle Sicherung der Instanz durchzuführen. Bei einer inkrementellen Sicherung werden Protokolldateien aufzählt und gesichert. Inkrementelle Sicherungen sind nur möglich, wenn die zirkuläre Protokollierung nicht aktiviert ist.

Es ist auch möglich, diesen Satz von Schritten zu ändern, um nachfolgende differenzielle Sicherungen der Instanz zu ermöglichen. Um eine differenzielle Sicherung durchzuführen, rufen Sie [JetTruncateLog](./jettruncatelog-function.md) in der vorherigen vollständigen oder inkrementellen Sicherung nicht auf. Wenn Sie [JetTruncateLog](./jettruncatelog-function.md)nicht aufrufen, ermöglichen Sie nachfolgende Sicherungen differenziell in Bezug auf die letzte vollständige oder inkrementelle Sicherung. Differenzielle Sicherungen sind nur möglich, wenn die zirkuläre Protokollierung nicht aktiviert ist.

Die Datenbankpatchdatei ist eine spezielle Hilfsdatei, die zum Speichern von Datenbankseitenabbildern unter bestimmten Umständen während der Sicherung verwendet wird. Diese Datei muss sich während eines Wiederherstellungsvorgang am gleichen Speicherort wie die zugeordnete Datenbank befinden. Diese Datei wird nur in Windows 2000 verwendet. Daher muss jede Anwendung, die für die Arbeit mit Windows 2000 und anderen Releases geschrieben wurde, Datenbankpatchdateien unterstützen, sofern diese vorhanden sind, darf aber auch nicht fehlschlagen, wenn sie nicht vorhanden sind.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
