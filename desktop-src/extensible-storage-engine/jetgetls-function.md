---
description: 'Weitere Informationen: jetgetls-Funktion'
title: Jetgetls-Funktion
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
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351532"
---
# <a name="jetgetls-function"></a>Jetgetls-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetls-function"></a>Jetgetls-Funktion

Die **jetgetls** -Funktion ermöglicht der Anwendung das Abrufen des Kontext Handles, das als lokaler Speicher bezeichnet wird, der einem Cursor oder der diesem Cursor zugeordneten Tabelle zugeordnet ist. Dieses Kontext Handle muss zuvor mithilfe von [jetsetls](./jetsetls-function.md)festgelegt worden sein. **Jetgetls** kann auch zum gleichzeitigen Abrufen des aktuellen Kontext Handles für einen Cursor oder eine Tabelle und zum Zurücksetzen dieses Kontext Handles verwendet werden.

**Windows XP: jetgetls** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*pls*

Der Ausgabepuffer, der das Kontext Handle empfängt, das momentan dem Cursor oder der Tabelle zugeordnet ist.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.

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
<td><p>Gibt an, dass das dem angegebenen Cursor zugeordnete Kontext Handle abgerufen werden soll.</p>
<p>Wenn weder JET_bitLSCursor noch JET_bitLSTable angegeben wird, wird JET_bitLSCursor angenommen.</p>
<p>Diese Option kann nicht mit JET_bitLSTable verwendet werden. Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn ein Versuch unternommen wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSTable</p></td>
<td><p>Gibt an, dass das Kontext Handle, das der Tabelle zugeordnet ist, die den angegebenen Cursor enthält, abgerufen werden soll. Diese Option kann nicht mit JET_bitLSCursor verwendet werden. Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn ein Versuch unternommen wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Gibt an, dass das Kontext Handle für das ausgewählte Objekt auf JET_LSNil zurückgesetzt werden soll. Der aktuelle Wert des Kontext Handles wird im Ausgabepuffer zurückgegeben.</p></td>
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
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Eine der angeforderten Optionen war ungültig, wird in unzulässiger Weise verwendet oder nicht implementiert.</p>
<p>Dies kann bei <strong>jetgetls</strong> vorkommen, wenn sowohl JET_bitLSCursor als auch JET_bitLSTable festgelegt sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSNotSet</p></td>
<td><p>Das Kontext Handle konnte nicht zurückgegeben werden, da dem angeforderten Objekt derzeit kein Kontext Handle zugeordnet ist.</p>
<p><strong>Hinweis  </strong> Dieser Fehler wird nicht zurückgegeben, wenn JET_bitLSReset angegeben wurde, dem angeforderten Objekt aber kein Kontext Handle zugeordnet wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wurde das Kontext Handle erfolgreich aus dem angeforderten Objekt abgerufen. Wenn JET_bitLSReset angegeben wurde, wurde dieses Kontext Handle ebenfalls erfolgreich aus dem Objekt entfernt. Es erfolgt keine Änderung des Daten Bank Status.

Bei einem Fehler ist keine Änderung des Zustands des angeforderten Objekts aufgetreten. Es erfolgt keine Änderung des Daten Bank Status.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetsetls](./jetsetls-function.md)
