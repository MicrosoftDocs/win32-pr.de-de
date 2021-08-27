---
description: Weitere Informationen finden Sie unter JetGetLS-Funktion.
title: JetGetLS-Funktion
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9eb6eed0bbec7be0acd377fa3b34d1b91a8b3fed
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982543"
---
# <a name="jetgetls-function"></a>JetGetLS-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetls-function"></a>JetGetLS-Funktion

Mit **der JetGetLS-Funktion** kann die Anwendung das Kontexthandl abrufen, das als Local Storage bezeichnet wird und einem Cursor oder der diesem Cursor zugeordneten Tabelle zugeordnet ist. Dieses Kontexthandl muss zuvor mit [JetSetLS festgelegt worden sein.](./jetsetls-function.md) **JetGetLS** kann auch zum gleichzeitigen Abrufen des aktuellen Kontexthandls für einen Cursor oder eine Tabelle und zum Zurücksetzen dieses Kontexthandls verwendet werden.

**Windows XP: JetGetLS** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*pls*

Der Ausgabepuffer, der das Kontexthand handle empfängt, das dem Cursor oder der Tabelle derzeit zugeordnet ist.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen an geben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitLSCursor</p> | <p>Gibt an, dass das Kontexthand handle, das dem angegebenen Cursor zugeordnet ist, abgerufen werden soll.</p><p>Wenn weder JET_bitLSCursor noch JET_bitLSTable angegeben wird, wird JET_bitLSCursor angenommen.</p><p>Diese Option kann nicht zusammen mit JET_bitLSTable. Der Vorgang kann nicht durchgeführt werden JET_errInvalidgrbit wenn dies versucht wird.</p> | 
| <p>JET_bitLSTable</p> | <p>Gibt an, dass das Kontexthand handle, das der Tabelle zugeordnet ist, die den angegebenen Cursor enthält, abgerufen werden soll. Es ist unzulässig, diese Option mit einem JET_bitLSCursor. Der Vorgang kann nicht durchgeführt werden JET_errInvalidgrbit wenn dies versucht wird.</p> | 
| <p>JET_bitLSReset</p> | <p>Gibt an, dass das Kontexthand handle für das ausgewählte Objekt zurückgesetzt werden soll, um JET_LSNil. Der aktuelle Wert des Kontexthandges wird im Ausgabepuffer zurückgegeben.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Eine der angeforderten Optionen war ungültig, wird auf ungültige Weise verwendet oder wurde nicht implementiert.</p><p>Dies kann für <strong>JetGetLS</strong> passieren, wenn sowohl JET_bitLSCursor als auch JET_bitLSTable festgelegt sind.</p> | 
| <p>JET_errLSNotSet</p> | <p>Das Kontexthand handle konnte nicht zurückgegeben werden, da dem angeforderten Objekt derzeit kein Kontexthand handle zugeordnet ist.</p><p><strong>Hinweis:  </strong> Dieser Fehler wird nicht zurückgegeben, wenn JET_bitLSReset angegeben ist, aber dem angeforderten Objekt kein Kontexthand handle zugeordnet wurde.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wurde das Kontexthand handle erfolgreich aus dem angeforderten Objekt abgerufen. Wenn JET_bitLSReset angegeben wurde, wurde dieses Kontexthand handle auch erfolgreich aus dem -Objekt entfernt. Es erfolgt keine Änderung des Datenbankstatus.

Bei einem Fehler ist keine Änderung des Zustands des angeforderten Objekts aufgetreten. Es erfolgt keine Änderung des Datenbankstatus.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetLS](./jetsetls-function.md)
