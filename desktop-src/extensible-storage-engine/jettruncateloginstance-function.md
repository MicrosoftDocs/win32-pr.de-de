---
description: 'Weitere Informationen zu: JetTruncateLogInstance-Funktion'
title: JetTruncateLogInstance-Funktion
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4fdf8f7c47baab70426ddf03cdbc666a13c08f3d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477856"
---
# <a name="jettruncateloginstance-function"></a>JetTruncateLogInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jettruncateloginstance-function"></a>JetTruncateLogInstance-Funktion

Die **JetTruncateLogInstance-Funktion** wird während einer von [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) initiierten Sicherung verwendet, um alle Transaktionsprotokolldateien zu löschen, die nach erfolgreichem Abschluss der aktuellen Sicherung nicht mehr benötigt werden.

**Windows XP:****JetTruncateLogInstance** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die -Instanz, die für diesen Aufruf verwendet werden soll.

Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. Die Verwendung dieser globalen Instanz wird in diesem Fall impliziert.

Für Windows XP und höhere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacymodus befindet (Windows Kompatibilitätsmodus 2000), in dem nur eine Instanz unterstützt wird. Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p><strong>Windows Server 2003:</strong>  Dieser Rückgabewert wird in Windows Server 2003 eingeführt.</p><p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg294067(v=exchg.10).md">JetStopBackup</a>abgebrochen wurde.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>beendet wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Der Sicherungsvorgang ist fehlgeschlagen, da er außerhalb der Sequenz aufgerufen wurde. <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> gibt diesen Fehler zurück, wenn ausstehende Dateihandles vorhanden sind, die mit <a href="gg269249(v=exchg.10).md">JetOpenFile</a> für die Instanz erstellt wurden.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameter führte zu einem unerwarteten Ergebnis. Dies kann für <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> auftreten, wenn das angegebene Instanzhandle ungültig ist.</p> | 
| <p>JET_errNoBackup</p> | <p>Fehler beim Vorgang, weil keine externe Sicherung ausgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Fehler beim Vorgang, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, wobei nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, werden die Transaktionsprotokolldateien gelöscht, die nach erfolgreichem Abschluss der aktuellen Sicherung nicht mehr benötigt werden. Der Sicherungsstatuscomputer wird erweitert, sodass die Sicherung von Datenbankdateien nicht mehr zulässig ist. Nur Datenbankpatchdateien und Transaktionsprotokolldateien dürfen für die Sicherung über diesen Punkt hinaus geöffnet werden.

Wenn diese Funktion fehlschlägt, kann der Sicherungsstatuscomputer erweitert werden, sodass die Sicherung von Datenbankdateien nicht mehr zulässig ist. Möglicherweise werden einige Transaktionsprotokolldateien gelöscht, die kleiner als die gewünschte Zahl sind, aber sie werden immer vom ältesten zum ersten Gelöschten gelöscht.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
