---
description: Weitere Informationen finden Sie unter JetGetAttachInfoInstance-Funktion.
title: JetGetAttachInfoInstance-Funktion
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8bbfac13e1536c0a8261e3c63a4308a84a60cf09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474096"
---
# <a name="jetgetattachinfoinstance-function"></a>JetGetAttachInfoInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetattachinfoinstance-function"></a>JetGetAttachInfoInstance-Funktion

Die **JetGetAttachInfoInstance-Funktion** wird während einer Sicherung verwendet, die von [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) initiiert wird, um eine Instanz nach den Namen von Datenbankdateien abfragt, die Teil des Sicherungsdateisets werden sollen. Es werden nur Datenbanken berücksichtigt, die derzeit mit [JetAttachDatabase](./jetattachdatabase-function.md) an die Instanz angefügt sind. Diese Dateien können anschließend mit [JetOpenFileInstance geöffnet](./jetopenfileinstance-function.md) und mit [JetReadFileInstance gelesen werden.](./jetreadfileinstance-function.md)

**Windows XP: JetGetAttachInfoInstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die -Instanz, die für diesen Aufruf verwendet werden soll.

Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. Die Verwendung dieser einen globalen Instanz wird in diesem Fall impliziert.

Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird. Andernfalls kann der Vorgang nicht durchgeführt JET_errRunningInMultiInstanceMode.

*szz*

Der Ausgabepuffer, der die Liste der auf NULL beendeten Zeichenfolgen empfängt, die den Satz von Datenbankdateien beschreiben, die Teil des Sicherungsdateisets sein sollen. Die Liste der in diesem Puffer zurückgegebenen Zeichenfolgen hat das gleiche Format wie eine mehrzeichenfolge, die von der Registrierung verwendet wird. Jede auf NULL endende Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Abschlusszeichen.

*cbMax*

Die maximale Größe des Ausgabepuffers in Bytes.

*–actual*

Zeiger auf den Ausgabepuffer, der die tatsächliche Menge an Zeichenfolgendaten empfängt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg269309(v=exchg.10).md">JetStopBackupInstance abgebrochen wurde.</a> Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg294108(v=exchg.10).md">JetStopServiceInstance beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Fehler beim Sicherungsvorgang, weil er nicht sequenziert aufgerufen wurde. <strong>JetGetAttachInfoInstance gibt</strong> diesen Fehler zurück, wenn die aktuelle Sicherung keine vollständige Sicherung ist.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetGetAttachInfoInstance</strong> passieren, wenn das angegebene Instanzhandy ungültig ist (Windows XP und spätere Releases).</p> | 
| <p>JET_errNoBackup</p> | <p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, bei dem nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg werden die angeforderten Informationen zu dem Satz von Datenbankdateien, die Teil des Sicherungsdateisets sein sollen, in den Ausgabepuffern platziert, sofern angegeben.

Bei einem Fehler ist der Zustand der Ausgabepuffer nicht definiert. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die Instanz.

#### <a name="remarks"></a>Hinweise

Beachten Sie, dass diese API keinen Fehler oder eine Warnung zurück gibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Teil des Sicherungsdateisets sein sollten. Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und diese Informationen verwenden, um zu bestimmen, ob die Liste abgeschnitten wurde.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetGetAttachInfoInstanceW</strong> (Unicode) und <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopBackupInstance](./jetstopbackupinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)
