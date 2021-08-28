---
description: 'Weitere Informationen zu: JetGetLogInfo-Funktion'
title: JetGetLogInfo-Funktion
TOCTitle: JetGetLogInfo Function
ms:assetid: a9d14830-d731-4d47-bdc2-c0660a08678e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294055(v=EXCHG.10)
ms:contentKeyID: 32765665
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoA
- JetGetLogInfoW
- JetGetLogInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 889e660254610441e56204c2585049e3c7e5ad38
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465827"
---
# <a name="jetgetloginfo-function"></a>JetGetLogInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetloginfo-function"></a>JetGetLogInfo-Funktion

Die **JetGetLogInfo-Funktion** wird während einer von [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) initiierten Sicherung verwendet, um eine Instanz nach den Namen von Datenbankpatchdateien und Transaktionsprotokolldateien abzufragen, die Teil des Sicherungsdateisatzes werden sollen. Diese Dateien können anschließend mit [JetOpenFile](./jetopenfile-function.md) geöffnet und mit [JetReadFile](./jetreadfile-function.md)gelesen werden.

```cpp
    JET_ERR JET_API JetGetLogInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parameter

*szz*

Der Ausgabepuffer, der die Liste der auf NULL endenden Zeichenfolgen empfängt, die den Satz von Datenbankpatchdateien und Transaktionsprotokolldateien beschreiben, die Teil des Sicherungsdateisatzes sein sollen.

Die Liste der in diesem Puffer zurückgegebenen Zeichenfolgen hat das gleiche Format wie eine von der Registrierung verwendete Mehrfachzeichenfolge. Jede auf NULL endende Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Abschlusszeichen.

*cbMax*

Die maximale Größe des Ausgabepuffers in Bytes.

*actual*

Empfängt die tatsächliche Menge an Zeichenfolgendaten, die im Ausgabepuffer empfangen werden.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg294067(v=exchg.10).md">JetStopBackup</a>abgebrochen wurde. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Der Sicherungsvorgang ist fehlgeschlagen, weil er außerhalb der Sequenz aufgerufen wurde. <strong>JetGetLogInfo</strong> gibt diesen Fehler zurück, wenn ausstehende Dateihandles vorhanden sind, die mit <a href="gg269249(v=exchg.10).md">JetOpenFile</a> für die Instanz erstellt wurden.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann bei <strong>JetGetLogInfo</strong> auftreten, wenn das angegebene Instanzhandle ungültig ist (Windows XP und höher).</p> | 
| <p>JET_errNoBackup</p> | <p>Fehler beim Vorgang, weil keine externe Sicherung ausgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Fehler beim Vorgang, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, wobei nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg werden die angeforderten Informationen zu den Datenbankpatchdateien und Transaktionsprotokolldateien, die Teil des Sicherungsdateisatzes sein sollen, in den Ausgabepuffern platziert, sofern angegeben. Der Sicherungsstatuscomputer wird erweitert, sodass die Sicherung von Datenbankdateien nicht mehr zulässig ist. Nur Datenbankpatchdateien und Transaktionsprotokolldateien dürfen für die Sicherung über diesen Punkt hinaus geöffnet werden.

Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die Instanz.

#### <a name="remarks"></a>Hinweise

Beachten Sie, dass diese API keinen Fehler oder keine Warnung zurückgibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Teil des Sicherungsdateisatzes sein sollten. Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und diese Informationen verwenden, um zu bestimmen, ob die Liste abgeschnitten wurde.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetGetLogInfoW</strong> (Unicode) und <strong>JetGetLogInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)
