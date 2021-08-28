---
description: Weitere Informationen finden Sie unter JetSetLS-Funktion.
title: JetSetLS-Funktion
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c94e5dc01d2aff69b699894f88287122cb9530cf
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984283"
---
# <a name="jetsetls-function"></a>JetSetLS-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetls-function"></a>JetSetLS-Funktion

Mit **der JetSetLS-Funktion** kann die Anwendung einem Cursor oder der diesem Cursor zugeordneten Tabelle ein Kontexthandl zuordnen, das als Local Storage bezeichnet wird. Dieses Kontexthand handle kann von der Anwendung verwendet werden, um zusätzliche Daten zu speichern, die einem Cursor oder einer Tabelle zugeordnet sind. Die Anwendung wird später mithilfe eines Laufzeitrückrufs benachrichtigt, wenn das Kontexthand handle freigegeben werden muss. Dadurch kann einem Cursor oder einer Tabelle ein dynamisch zugeordneter Zustand zugeordnet werden.

**Windows XP:****JetSetLS** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*ls*

Das Kontexthand handle, das dem Cursor oder der Tabelle zugeordnet werden soll.

Wenn JET_bitLSReset angegeben wird, wird der tatsächliche Wert dieses Parameters ignoriert und JET_LSNil verwendet.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitLSCursor</p> | <p>Diese Option gibt an, dass das Kontexthand handle dem angegebenen Cursor zugeordnet werden soll.</p><p>Wenn weder JET_bitLSCursor noch JET_bitLSTable angegeben wird, wird JET_bitLSCursor angenommen.</p><p>Es ist unzulässig, diese Option mit einem JET_bitLSTable. Der Vorgang kann nicht durchgeführt werden JET_errInvalidgrbit wenn dies versucht wird.</p> | 
| <p>JET_bitLSReset</p> | <p>Diese Option gibt an, dass das angegebene Kontexthand handle ignoriert werden soll und dass das Kontexthand handle für das ausgewählte Objekt auf die JET_LSNil.</p><p>Es ist wichtig zu beachten, dass diese Aktion nicht zu einem Rückruf führt, um den vorherigen Wert des Kontexthandpunkts für das ausgewählte Objekt zu bereinigen. Die ordnungsgemäße Bereinigung des vorherigen Kontexthandls kann mit <a href="gg269234(v=exchg.10).md">JetGetLS</a> mit JET_bitLSReset. Weitere <a href="gg269234(v=exchg.10).md">Informationen finden Sie unter JetGetLS.</a></p> | 
| <p>JET_bitLSTable</p> | <p>Diese Option gibt an, dass das Kontexthand handle der Tabelle zugeordnet werden soll, die dem angegebenen Cursor zugeordnet ist.</p><p>Es ist unzulässig, diese Option mit einem JET_bitLSCursor. Der Vorgang kann nicht durchgeführt werden JET_errInvalidgrbit wenn dies versucht wird.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInvalidgrbit</p> | <p>Eine der angeforderten Optionen war ungültig, wurde falsch verwendet oder nicht implementiert. Dies kann für <strong>JetSetLS</strong> passieren, wenn JET_bitLSCursor und JET_bitLSTable angegeben sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errLSAlreadySet</p> | <p>Das kontextorientierte Handle konnte dem angeforderten Objekt nicht zugeordnet werden, da ihm bereits ein Kontexthand handle zugeordnet war.</p> | 
| <p>JET_errLSCallbackNotSpecified</p> | <p>Das kontextorientierte Handle konnte dem angeforderten Objekt nicht zugeordnet werden, da der Laufzeitrückruf nicht für die -Instanz konfiguriert wurde, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wurde das kontextorientierte Handle erfolgreich dem angeforderten Objekt zugeordnet. Es erfolgt keine Änderung des Datenbankstatus.

Bei einem Fehler ist keine Änderung des Zustands des angeforderten Objekts aufgetreten. Es erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Bemerkungen

Die lokale Storage für einen Cursor oder eine Tabelle sollte als flüchtiger Cache angezeigt werden. Die Anwendung sollte zunächst versuchen, das Kontexthandl mit [JetGetLS abzurufen.](./jetgetls-function.md) Wenn der Wert nicht festgelegt ist (d.h. JET_LSNil), sollte die Anwendung einen neuen Kontext erstellen und ihn mit **jetSetLS** in den Cache laden. Die Anwendung kann den Cache mithilfe eines Aufrufs von [JetGetLS](./jetgetls-function.md) mit JET_bitLSReset. Wenn die Datenbank-Engine den Cache bereinigt, wird ein Laufzeitrückruf generiert, um der Anwendung die Möglichkeit zu geben, diesen Kontext zu bereinige. Der Rückruftyp wird für JET_cbtypFreeCursorLS Kontexthand handle verwendet, das einem Cursor zugeordnet ist, und JET_cbtypFreeTableLS für ein Kontexthand handle, das einer Tabelle zugeordnet ist. In beiden Fällen wird das Kontexthandler als pvArg1 übergeben. Weitere [JET_CALLBACK](./jet-callback-callback-function.md) finden Sie unter .

Der Laufzeitrückruf muss ordnungsgemäß für die -Instanz konfiguriert werden, die der angegebenen Sitzung zugeordnet ist, bevor lokale Storage verwendet werden können. Dieser Rückruf kann mithilfe von [JetSetSystemParameter mit JET_paramRuntimeCallback.](./jetsetsystemparameter-function.md) [](./callback-parameters.md) Weitere [Informationen finden Sie unter JetSetSystemParameter](./jetsetsystemparameter-function.md) [JET_paramRuntimeCallback](./callback-parameters.md) unter Systemparameter.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLS](./jetgetls-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
