---
description: 'Weitere Informationen zu: JetGetTruncateLogInfoInstance-Funktion'
title: JetGetTruncateLogInfoInstance-Funktion
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36583267277f7c5254adc85047ce99631f6c03ef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479076"
---
# <a name="jetgettruncateloginfoinstance-function"></a>JetGetTruncateLogInfoInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgettruncateloginfoinstance-function"></a>JetGetTruncateLogInfoInstance-Funktion

Die **JetGetTruncateLogInfoInstance-Funktion** wird während einer Sicherung verwendet, die von [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) initiiert wird, um eine Instanz nach den Namen der Transaktionsprotokolldateien abzufragen, die nach erfolgreichem Abschluss der Sicherung sicher gelöscht werden können.

**Windows XP:****JetGetTruncateLogInfoInstance** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die -Instanz, die für diesen Aufruf verwendet werden soll.

*szz*

Der Ausgabepuffer, der die Liste der auf NULL endenden Zeichenfolgen empfängt, die den Satz von Transaktionsprotokolldateien beschreiben, die sicher gelöscht werden können, nachdem die Sicherung erfolgreich abgeschlossen wurde.

Die Liste der Zeichenfolgen, die in diesem Puffer zurückgegeben werden, hat das gleiche Format wie eine mehrfache Zeichenfolge, die von der Registrierung verwendet wird. Jede auf NULL endende Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Abschlusszeichen.

*cbMax*

Die maximale Größe des Ausgabepuffers in Bytes.

*actual*

Zeiger auf den Ausgabepuffer, der die tatsächliche Menge an Zeichenfolgendaten empfängt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte führte zu einem unerwarteten Ergebnis.</p><p><strong>Windows XP und höher:</strong>  Dies kann bei <strong>JetGetTruncateLogInfoInstance</strong> passieren, wenn das angegebene Instanzhandle ungültig ist.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>ausgeführt wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wurde in Windows XP eingeführt.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg294067(v=exchg.10).md">JetStopBackup</a>abgebrochen wurde.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wurde in Windows XP eingeführt.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Der Sicherungsvorgang ist fehlgeschlagen, weil er außerhalb der Sequenz aufgerufen wurde.</p> | 
| <p>JET_errNoBackup</p> | <p>Fehler beim Vorgang, weil keine externe Sicherung ausgeführt wird.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 
| <p><strong>JetGetTruncateLogInfoInstance</strong></p> | <p>Es gibt ausstehende Dateihandles, die mit <a href="gg269249(v=exchg.10).md">JetOpenFile</a> für die Instanz erstellt wurden.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, werden die angeforderten Informationen über den Satz von Transaktionsprotokolldateien, die nach erfolgreichem Abschluss der Sicherung sicher gelöscht werden können, in den Ausgabepuffern platziert, in denen sie bereitgestellt werden. Der Sicherungsstatuscomputer wird erweitert, sodass die Sicherung von Datenbankdateien nicht mehr zulässig ist. Nur Datenbankpatchdateien und Transaktionsprotokolldateien können für die Sicherung über diesen Punkt hinaus geöffnet werden.

Wenn diese Funktion fehlschlägt, ist der Status der Ausgabepuffer nicht definiert. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die Instanz.

#### <a name="remarks"></a>Hinweise

Diese API gibt keinen Fehler oder eine Warnung zurück, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Teil des Sicherungsdateisatzes sein sollten. Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und diese Informationen verwenden, um zu bestimmen, ob die Liste abgeschnitten wurde.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) und <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
