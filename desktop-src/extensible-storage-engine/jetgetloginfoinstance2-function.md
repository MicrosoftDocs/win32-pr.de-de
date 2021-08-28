---
description: Weitere Informationen finden Sie unter JetGetLogInfoInstance2-Funktion.
title: JetGetLogInfoInstance2-Funktion
TOCTitle: JetGetLogInfoInstance2 Function
ms:assetid: 50fdae92-611c-4dbf-846e-86cc836a23db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269247(v=EXCHG.10)
ms:contentKeyID: 32765549
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance2W
- JetGetLogInfoInstance2
- JetGetLogInfoInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec8bf0a4cee4e89f8252e53ed0ffbeb3aed4bcdf
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982533"
---
# <a name="jetgetloginfoinstance2-function"></a>JetGetLogInfoInstance2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetloginfoinstance2-function"></a>JetGetLogInfoInstance2-Funktion

Die **JetGetLogInfoInstance2-Funktion** wird während einer von [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) initiierten Sicherung verwendet, um eine Instanz nach den Namen von Datenbankpatchdateien und Transaktionsprotokolldateien abfragt, die Teil des Sicherungsdateisets werden sollen. Diese Dateien können anschließend mit [JetOpenFile geöffnet](./jetopenfile-function.md) und mit [JetReadFile gelesen werden.](./jetreadfile-function.md)

**Windows XP: JetGetLogInfoInstance2** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetGetLogInfoInstance2(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in_out_opt  JET_LOGINFO* pLogInfo
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die -Instanz, die für diesen Aufruf verwendet werden soll.

Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. Die Verwendung dieser einen globalen Instanz wird in diesem Fall impliziert.

Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird. Andernfalls wird der Vorgang mit einem JET_errRunningInMultiInstanceMode.

*szz*

Der Ausgabepuffer, der die Liste der auf NULL beendeten Zeichenfolgen erhält, die den Satz von Datenbankpatchdateien und Transaktionsprotokolldateien beschreiben, die Teil des Sicherungsdateisets sein sollen.

Die Liste der in diesem Puffer zurückgegebenen Zeichenfolgen hat das gleiche Format wie eine mehrzeichenfolge, die von der Registrierung verwendet wird. Jede auf NULL endende Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Abschlusszeichen.

*cbMax*

Die maximale Größe des Ausgabepuffers in Bytes.

*–actual*

Empfängt die tatsächliche Menge der im Ausgabepuffer empfangenen Zeichenfolgendaten.

*pLogInfo*

Empfängt strukturierte Informationen zu den Transaktionsprotokolldateien, die Teil des Sicherungsdateisets sein sollen.

Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass sein Wert NULL ist.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg294067(v=exchg.10).md">JetStopBackup abgebrochen wurde.</a> Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Fehler beim Sicherungsvorgang, weil er nicht sequenziert aufgerufen wurde. <a href="gg294055(v=exchg.10).md">JetGetLogInfo gibt</a> diesen Fehler zurück, wenn ausstehende Dateihandles mit <a href="gg269249(v=exchg.10).md">JetOpenFile</a> für die Instanz erstellt wurden.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <a href="gg294055(v=exchg.10).md">JetGetLogInfo passieren,</a> wenn das angegebene Instanzhandy ungültig ist (Windows XP und spätere Versionen).</p> | 
| <p>JET_errNoBackup</p> | <p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, bei dem nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg werden die angeforderten Informationen zum Satz von Datenbankpatchdateien und Transaktionsprotokolldateien, die Teil des Sicherungsdateisets sein sollten, in den Ausgabepuffern platziert, sofern angegeben. Der Sicherungsstatuscomputer wird so erweitert, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist. Nur Datenbankpatchdateien und Transaktionsprotokolldateien dürfen für die Sicherung über diesen Punkt hinaus geöffnet werden.

Bei einem Fehler ist der Zustand der Ausgabepuffer nicht definiert. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die Instanz.

#### <a name="remarks"></a>Bemerkungen

Beachten Sie, dass diese API keinen Fehler oder eine Warnung zurück gibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Teil des Sicherungsdateisets sein sollten. Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und diese Informationen verwenden, um zu bestimmen, ob die Liste abgeschnitten wurde.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetGetLogInfoInstance2W</strong> (Unicode) und <strong>JetGetLogInfoInstance2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)
