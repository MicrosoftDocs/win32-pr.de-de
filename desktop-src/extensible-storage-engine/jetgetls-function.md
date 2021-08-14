---
description: 'Weitere Informationen zu: JetGetLS-Funktion'
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
ms.openlocfilehash: 3a359bb2899a2dea604e236a7118c914e795bffba7ca675229e28ad3a7f25dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979060"
---
# <a name="jetgetls-function"></a>JetGetLS-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetls-function"></a>JetGetLS-Funktion

Mit der **JetGetLS-Funktion** kann die Anwendung das Kontexthandle abrufen, das als Local Storage bezeichnet wird, das einem Cursor oder der Tabelle zugeordnet ist, die diesem Cursor zugeordnet ist. Dieses Kontexthandle muss zuvor mit [JetSetLS](./jetsetls-function.md)festgelegt worden sein. **JetGetLS** kann auch verwendet werden, um gleichzeitig das aktuelle Kontexthandle für einen Cursor oder eine Tabelle abzurufen und dieses Kontexthandle zurückzusetzen.

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

Der Ausgabepuffer, der das Kontexthandle empfängt, das dem Cursor oder der Tabelle derzeit zugeordnet ist.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.

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
<td><p>Gibt an, dass das Kontexthandle, das dem angegebenen Cursor zugeordnet ist, abgerufen werden soll.</p>
<p>Wenn weder JET_bitLSCursor noch JET_bitLSTable angegeben wird, wird JET_bitLSCursor angenommen.</p>
<p>Diese Option kann nicht mit JET_bitLSTable verwendet werden. Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn dies versucht wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSTable</p></td>
<td><p>Gibt an, dass das Kontexthandle, das der Tabelle zugeordnet ist, die den angegebenen Cursor enthält, abgerufen werden soll. Es ist unzulässig, diese Option mit JET_bitLSCursor zu verwenden. Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn dies versucht wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Gibt an, dass das Kontexthandle für das ausgewählte Objekt auf JET_LSNil zurückgesetzt werden soll. Der aktuelle Wert des Kontexthandle wird im Ausgabepuffer zurückgegeben.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p>
<p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Eine der angeforderten Optionen war ungültig, wurde auf unzulässige Weise verwendet oder nicht implementiert.</p>
<p>Dies kann für <strong>JetGetLS</strong> passieren, wenn sowohl JET_bitLSCursor als auch JET_bitLSTable festgelegt sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSNotSet</p></td>
<td><p>Das Kontexthandle konnte nicht zurückgegeben werden, da dem angeforderten Objekt derzeit kein Kontexthandle zugeordnet ist.</p>
<p><strong>Hinweis  </strong> Dieser Fehler wird nicht zurückgegeben, wenn JET_bitLSReset angegeben ist, dem angeforderten Objekt jedoch noch kein Kontexthandle zugeordnet wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wurde das Kontexthandle erfolgreich aus dem angeforderten Objekt abgerufen. Wenn JET_bitLSReset angegeben wurde, wurde dieses Kontexthandle ebenfalls erfolgreich aus dem -Objekt entfernt. Es wird keine Änderung am Datenbankzustand vorgenommen.

Bei einem Fehler ist keine Änderung am Status des angeforderten Objekts aufgetreten. Es wird keine Änderung am Datenbankzustand vorgenommen.

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
<td><p>Deklariert in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
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
[JetSetLS](./jetsetls-function.md)
