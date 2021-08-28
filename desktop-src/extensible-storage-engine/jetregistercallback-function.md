---
description: Weitere Informationen finden Sie unter JetRegisterCallback-Funktion.
title: JetRegisterCallback-Funktion
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cdc87805539619ff644afbd295bfa7f1ac76f075
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482786"
---
# <a name="jetregistercallback-function"></a>JetRegisterCallback-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetregistercallback-function"></a>JetRegisterCallback-Funktion

Mit **der JetRegisterCallback-Funktion** kann die Anwendung die Datenbank-Engine so konfigurieren, dass Benachrichtigungen für bestimmte Ereignisse an die Anwendung gesendet werden. Diese Benachrichtigungen sind einer bestimmten Tabelle zugeordnet und bleiben nur wirksam, bis die Instanz, die die Tabelle enthält, mit [JetTerm heruntergefahren wird.](./jetterm-function.md)

**Windows XP: JetRegisterCallback** wird in xp Windows eingeführt.

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*cbtyp*

Eine Bitmaske, die aus den Rückrufgründen besteht, aus denen die Anwendung Benachrichtigungen empfangen möchte.

Um diese Bitmaske zu erstellen, verwenden Sie einfach oder zusammen gültige Rückrufgründe aus [der](./jet-cbtyp.md) JET_CBTYP Enumeration.

*pCallback*

Der Funktionszeiger auf die Rückruffunktion für die Anwendung.

*pvContext*

Gibt einen Kontextzeiger an, der der Rückruffunktion für die Anwendung übergeben wird.

*phCallbackId*

Gibt ein Handle zurück, das später verwendet werden kann, um die Registrierung der angegebenen Rückruffunktion mit [JetUnregisterCallback abzubricht.](./jetunregistercallback-function.md)

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dieser Fehler wird von <strong>JetRegisterCallback zurückgegeben, wenn:</strong></p><ul><li><p><em>cbtyp</em> ist 0 (null),</p></li><li><p><em>pCallback</em> ist NULL.</p></li><li><p><em>phCallbackId</em> ist NULL.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird der angegebene Rückruf aus den angegebenen Rückrufgründen mit der Tabelle registriert, die dem angegebenen Cursor zugeordnet ist. Es erfolgt keine Änderung des Datenbankstatus.

Bei einem Fehler wird der Rückruf nicht registriert. Es erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Hinweise

Mit dieser Methode kann die Anwendung flüchtige Rückrufe einer Tabelle in einer Datenbank zuordnen. Wenn die Anwendung persistente Rückrufe einer Tabelle in der Datenbank zuordnen möchte, [](./jet-tablecreate-structure.md) sollte sie den Rückruf an JET_TABLECREATE [jetCreateTableColumnIndex übergeben.](./jetcreatetablecolumnindex-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetTerm](./jetterm-function.md)  
[JetUnregisterCallback](./jetunregistercallback-function.md)
