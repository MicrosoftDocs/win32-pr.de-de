---
description: 'Weitere Informationen zu: jetsetls-Funktion'
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
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525556"
---
# <a name="jetsetls-function"></a>JetSetLS-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetls-function"></a>JetSetLS-Funktion

Die **jetsetls** -Funktion ermöglicht es der Anwendung, ein Kontext Handle, das als lokaler Speicher bezeichnet wird, einem Cursor oder der diesem Cursor zugeordneten Tabelle zuzuordnen. Dieses Kontext Handle kann von der Anwendung verwendet werden, um zusätzliche Daten zu speichern, die einem Cursor oder einer Tabelle zugeordnet sind. Die Anwendung wird später mithilfe eines Lauf Zeit Rückrufs benachrichtigt, wenn das Kontext Handle freigegeben werden muss. Dadurch ist es möglich, einem Cursor oder einer Tabelle dynamisch zugeordneten Zustand zuzuordnen.

**Windows XP:**  **jetsetls** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*ls*

Das Kontext Handle, das dem Cursor oder der Tabelle zugeordnet werden soll.

Wenn JET_bitLSReset angegeben wird, wird der tatsächliche Wert dieses Parameters ignoriert und JET_LSNil verwendet.

*grbit*

Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitLSCursor</p></td>
<td><p>Diese Option gibt an, dass das Kontext Handle dem angegebenen Cursor zugeordnet werden soll.</p>
<p>Wenn weder JET_bitLSCursor noch JET_bitLSTable angegeben wird, wird JET_bitLSCursor angenommen.</p>
<p>Diese Option kann nicht mit JET_bitLSTable verwendet werden. Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn ein Versuch unternommen wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSReset</p></td>
<td><p>Diese Option gibt an, dass das angegebene Kontext Handle ignoriert werden soll und dass das Kontext Handle für das ausgewählte Objekt auf JET_LSNil zurückgesetzt werden soll.</p>
<p>Beachten Sie, dass diese Aktion nicht zu einem Rückruf führt, um den vorherigen Wert des Kontext Handles für das ausgewählte Objekt zu bereinigen. Eine ordnungsgemäße Bereinigung des vorherigen Kontext Handles kann mithilfe von <a href="gg269234(v=exchg.10).md">jetgetls</a> mit JET_bitLSReset erreicht werden. Weitere Informationen finden Sie unter <a href="gg269234(v=exchg.10).md">jetgetls</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>Diese Option gibt an, dass das Kontext Handle der Tabelle zugeordnet werden soll, die dem angegebenen Cursor zugeordnet ist.</p>
<p>Diese Option kann nicht mit JET_bitLSCursor verwendet werden. Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn ein Versuch unternommen wird.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Eine der angeforderten Optionen war ungültig, wurde falsch verwendet oder nicht implementiert. Dies kann bei <strong>jetsetls</strong> vorkommen, wenn JET_bitLSCursor und JET_bitLSTable angegeben sind.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet</p></td>
<td><p>Das angegebene Kontext Handle konnte dem angeforderten Objekt nicht zugeordnet werden, da ihm bereits ein Kontext Handle zugeordnet wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified</p></td>
<td><p>Das angegebene Kontext Handle konnte dem angeforderten Objekt nicht zugeordnet werden, weil der Lauf Zeit Rückruf nicht für die Instanz konfiguriert wurde, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wurde das angegebene Kontext Handle erfolgreich dem angeforderten Objekt zugeordnet. Es erfolgt keine Änderung des Daten Bank Status.

Bei einem Fehler ist keine Änderung des Zustands des angeforderten Objekts aufgetreten. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Der lokale Speicher für einen Cursor oder eine Tabelle sollte als flüchtiger Cache angezeigt werden. Die Anwendung sollte zuerst versuchen, das Kontext Handle mithilfe von [jetgetls](./jetgetls-function.md)abzurufen. Wenn der Wert nicht festgelegt ist (d. h., er ist JET_LSNil), sollte die Anwendung einen neuen Kontext erstellen und mithilfe von **jetsetls** in den Cache laden. Die Anwendung kann den Cache mithilfe eines Aufrufens von [jetgetls](./jetgetls-function.md) mit JET_bitLSReset löschen. Wenn die Datenbank-Engine den Cache löscht, wird ein Lauf Zeit Rückruf generiert, um der Anwendung die Möglichkeit zu geben, diesen Kontext zu bereinigen. Der Rückruftyp wird für ein Kontext Handle JET_cbtypFreeCursorLS, das einem Cursor zugeordnet ist, und JET_cbtypFreeTableLS für ein Kontext Handle, das einer Tabelle zugeordnet ist. In beiden Fällen wird das Kontext Handle als pvArg1. Weitere Informationen finden Sie unter [JET_CALLBACK](./jet-callback-callback-function.md) .

Der Lauf Zeit Rückruf muss für die-Instanz, die der angegebenen Sitzung zugeordnet ist, ordnungsgemäß konfiguriert werden, bevor der lokale Speicher verwendet werden kann. Dieser Rückruf kann mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit [JET_paramRuntimeCallback](./callback-parameters.md)festgelegt werden. Weitere Informationen finden Sie unter [jetsetsystemparameter](./jetsetsystemparameter-function.md) und [JET_paramRuntimeCallback](./callback-parameters.md) in System Parametern.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetgetls](./jetgetls-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
