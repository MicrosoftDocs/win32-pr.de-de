---
description: Weitere Informationen finden Sie unter JetGetAttachInfo-Funktion.
title: JetGetAttachInfo-Funktion
TOCTitle: JetGetAttachInfo Function
ms:assetid: 6b1392f3-f40a-4eb0-aea8-1508b23ed649
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269286(v=EXCHG.10)
ms:contentKeyID: 32765578
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfo
- JetGetAttachInfoA
- JetGetAttachInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0847fdef5b522a31192eeb153a286784f7bc73f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465057"
---
# <a name="jetgetattachinfo-function"></a>JetGetAttachInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetattachinfo-function"></a>JetGetAttachInfo-Funktion

Die **JetGetAttachInfo-Funktion** wird während einer von [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) initiierten Sicherung verwendet, um eine -Instanz nach den Namen der Datenbankdateien abzufragen, die Teil des Sicherungsdateisatzes werden sollen. Es werden nur Datenbanken berücksichtigt, die derzeit mit [JetAttachDatabase](./jetattachdatabase-function.md) an die Instanz angefügt sind. Diese Dateien können anschließend mit [JetOpenFile](./jetopenfile-function.md) geöffnet und mit [JetReadFile](./jetreadfile-function.md)gelesen werden.

```cpp
    JET_ERR JET_API JetGetAttachInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parameter

*szz*

Der Ausgabepuffer, der die Liste der auf NULL endenden Zeichenfolgen empfängt, die den Satz von Datenbankdateien beschreiben, die Teil des Sicherungsdateisatzes sein sollen. Die Liste der in diesem Puffer zurückgegebenen Zeichenfolgen hat das gleiche Format wie eine von der Registrierung verwendete Mehrfachzeichenfolge. Jede auf NULL endende Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Abschlusszeichen.

*cbMax*

Die maximale Größe des Ausgabepuffers in Bytes.

*actual*

Zeiger auf den Ausgabepuffer, der die tatsächliche Menge an Zeichenfolgendaten empfangen hat.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg294067(v=exchg.10).md">JetStopBackup</a>abgebrochen wurde. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Der Sicherungsvorgang ist fehlgeschlagen, da er außerhalb der Sequenz aufgerufen wurde. <strong>JetGetAttachInfo</strong> gibt diesen Fehler zurück, wenn es sich bei der aktuellen Sicherung nicht um eine vollständige Sicherung handelt.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann bei <strong>JetGetAttachInfo</strong> auftreten, wenn das angegebene Instanzhandle ungültig ist (Windows XP und höher).</p> | 
| <p>JET_errNoBackup</p> | <p>Fehler beim Vorgang, weil keine externe Sicherung ausgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Fehler beim Vorgang, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, wobei nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg werden die angeforderten Informationen zum Satz von Datenbankdateien, die Teil des Sicherungsdateisatzes sein sollen, in den Ausgabepuffern platziert, sofern angegeben.

Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die Instanz.

#### <a name="remarks"></a>Hinweise

Beachten Sie, dass diese API keinen Fehler oder keine Warnung zurückgibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Teil des Sicherungsdateisatzes sein sollten. Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und diese Informationen verwenden, um zu bestimmen, ob die Liste abgeschnitten wurde.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetGetAttachInfoW</strong> (Unicode) und <strong>JetGetAttachInfoA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
