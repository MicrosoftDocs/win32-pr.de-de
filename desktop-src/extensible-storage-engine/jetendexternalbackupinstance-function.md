---
description: 'Weitere Informationen zu: JetEndExternalBackupInstance-Funktion'
title: JetEndExternalBackupInstance-Funktion
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f82af0be3185db36498d9a5888da190e92314184
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479176"
---
# <a name="jetendexternalbackupinstance-function"></a>JetEndExternalBackupInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetendexternalbackupinstance-function"></a>JetEndExternalBackupInstance-Funktion

Die **JetEndExternalBackupInstance-Funktion** beendet eine externe Sicherungssitzung. Diese API ist die letzte API in einer Reihe von APIs, die aufgerufen werden muss, um eine erfolgreiche Onlinesicherung (nicht VSS-basiert) auszuführen.

**Windows XP: JetEndExternalBackupInstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die -Instanz, die für diesen Aufruf verwendet werden soll.

**Windows 2000:** Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. Die Verwendung dieser globalen Instanz wird in diesem Fall impliziert.

**Windows XP:** Für Windows XP und höhere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacymodus befindet (Windows Kompatibilitätsmodus 2000), in dem nur eine Instanz unterstützt wird. Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupAbortByCaller</p> | <p><strong>Windows XP:</strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p><p>Der Aufrufer hat eine Sicherung in der Mitte der Sicherungssequenz beendet, ohne die Absicht mit <a href="gg294067(v=exchg.10).md">JetStopBackup zu signalisieren.</a> Dieser Fehler ist das Ergebnis eines Fehlers im Sicherungsclient in Windows Server 2003 und höher. Bei Windows XP wird dieser Fehler für eine absichtliche Beendigung der externen Sicherungssequenz zurückgegeben.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p><strong>Windows Server 2003:</strong> Dieser Rückgabewert wird in Windows Server 2003 eingeführt.</p><p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg294067(v=exchg.10).md">JetStopBackup</a>abgebrochen wurde.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>beendet wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p><strong>Windows XP:</strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p><p>Der Vorgang kann nicht abgeschlossen werden, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p> | 
| <p>JET_errNoBackup</p> | <p>Fehler beim Vorgang, weil keine externe Sicherung ausgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, wobei nur eine Instanz unterstützt wird, obwohl tatsächlich bereits mehrere Instanzen vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 



Wenn die Funktion erfolgreich war, war die externe Sicherung erfolgreich. Erfolg gibt an, dass alle Dateien (z. B. Datenbanken und Protokolle), die für den Sicherungstyp geeignet sind (angegeben in [JetBeginExternalBackup),](./jetbeginexternalbackup-function.md)von der Sicherungs-Engine abgerufen wurden. Die gesicherten Dateien können mit harter Wiederherstellung wiederhergestellt werden ([JetExternalRestore](./jetexternalrestore-function.md)).

Wenn diese Funktion fehlschlägt, wird die externe Sicherung in der Regel beendet. Fehler bedeutet, dass die Sicherung aufgrund eines Client- oder Anwendungsverwendungsfehlers ungültig ist. Es ist wichtig, den Rückgabecode für diese API zu überprüfen, um sicherzustellen, dass die Sicherungssequenz erfolgreich war.

#### <a name="remarks"></a>Hinweise

Wenn die Engine zum Protokollieren von Ereignissen konfiguriert ist, wird ein Ereignis protokolliert, um die Auflösung der externen Sicherung anzugeben.

Wenn die Sicherungssequenz nicht in der angegebenen Reihenfolge und mit einem erfolgreichen Aufruf von [JetEndExternalBackup](./jetendexternalbackup-function.md)abgeschlossen wird, enthalten nachfolgende inkrementelle Sicherungen möglicherweise mehr Daten als von der Anwendung erwartet.

Weitere Informationen zur API-Sequenz für externe Sicherungen finden Sie unter [JetBeginExternalBackup.](./jetbeginexternalbackup-function.md)

Wenn die Protokollkürzung vor Windows Vista nicht durchgeführt wurde, hat die Engine davon ausgegangen, dass es sich bei der Sicherung um eine Kopiersicherung handelt. Die Sicherung kann jedoch eine normale Sicherung sein, für die keine Kürzung durchgeführt wurde (z. B. wenn getrennte Datenbanken vorhanden sind). Die option JET_bitBackupTruncateDone kann verwendet werden, um die Engine darüber zu informieren und ordnungsgemäße Änderungen des Datenbankheaders zuzulassen.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Storage-Engine-Fehler](./extensible-storage-engine-errors.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JET_ERR](./jet-err.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
