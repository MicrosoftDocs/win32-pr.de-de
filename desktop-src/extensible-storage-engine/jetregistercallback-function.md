---
description: 'Weitere Informationen zu: JetRegisterCallback-Funktion'
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
ms.openlocfilehash: 0ef90466b736facf5bd9fefee31c0449964d003b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985803"
---
# <a name="jetregistercallback-function"></a>JetRegisterCallback-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetregistercallback-function"></a>JetRegisterCallback-Funktion

Mit der **JetRegisterCallback-Funktion** kann die Anwendung die Datenbank-Engine so konfigurieren, dass Benachrichtigungen für bestimmte Ereignisse an die Anwendung ausgegeben werden. Diese Benachrichtigungen sind einer bestimmten Tabelle zugeordnet und bleiben nur wirksam, bis die Instanz, die die Tabelle enthält, mithilfe von [JetTerm](./jetterm-function.md)heruntergefahren wird.

**Windows XP: JetRegisterCallback** wird in Windows XP eingeführt.

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

Um diese Bitmaske zu erstellen, einfach oder zusammen gültige Rückrufgründe aus der [JET_CBTYP](./jet-cbtyp.md) Enumeration.

*pCallback*

Der Funktionszeiger auf die Rückruffunktion für die Anwendung.

*pvContext*

Gibt einen Kontextzeiger an, der der Rückruffunktion für die Anwendung übergeben wird.

*phCallbackId*

Gibt ein Handle zurück, das später verwendet werden kann, um die Registrierung der angegebenen Rückruffunktion mit [jetUnregisterCallback](./jetunregistercallback-function.md)abzubrechen.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dieser Fehler wird von <strong>JetRegisterCallback</strong> zurückgegeben, wenn:</p><ul><li><p><em>cbtyp</em> ist 0 (null),</p></li><li><p><em>pCallback</em> ist NULL.</p></li><li><p><em>phCallbackId</em> ist NULL.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird der angegebene Rückruf aus den angegebenen Rückrufgründen bei der Tabelle registriert, die dem angegebenen Cursor zugeordnet ist. Es wird keine Änderung am Datenbankzustand vorgenommen.

Bei einem Fehler wird der Rückruf nicht registriert. Es wird keine Änderung am Datenbankzustand vorgenommen.

#### <a name="remarks"></a>Bemerkungen

Diese Methode bietet der Anwendung die Möglichkeit, flüchtige Rückrufe einer Tabelle in einer Datenbank zuzuordnen. Wenn die Anwendung persistente Rückrufe einer Tabelle in der Datenbank zuordnen möchte, sollte sie den Rückruf mithilfe von [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)an [JET_TABLECREATE](./jet-tablecreate-structure.md) übergeben.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



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
