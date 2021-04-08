---
description: Weitere Informationen finden Sie in der jetgotoposition-Funktion
title: Jetgotoposition-Funktion
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae5148431ad46c5a75bbd804f2c0d777b279561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749720"
---
# <a name="jetgotoposition-function"></a>Jetgotoposition-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgotoposition-function"></a>Jetgotoposition-Funktion

Die **jetgotoposition** -Funktion verschiebt einen Cursor an eine neue Position, die ein Bruchteil der Art und Weise des aktuellen Indexes ist. Der Bruchteil entspricht ungefähr folgendem:

precpos- \> centrieslt/precpos- \> zentriestotal

Dieser Vorgang wird als Reaktion auf die Eingabe des Benutzer Bild Lauf Felds ausgeführt, die empfangen wird, wenn der Benutzer versucht, Daten anzuzeigen, die teilweise durch ein DataSet gestartet werden.

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*präpos*

Die Beschreibung des Bruchteils, der zum Positionieren des Cursors im aktuellen Index verwendet werden soll.

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
<td><p>Der Vorgang konnte nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang konnte nicht ausgeführt werden, da der-Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Die angegebene "precpos- &gt; cbStruct" ist keine gültige Größe für die <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> Struktur, oder "precpos- &gt; centrieslt" ist größer als "precpos- &gt; centriestotal".</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNotFound</p></td>
<td><p>Dieser Fehler wird zurückgegeben, wenn der Index leer ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird der Cursor zu einem aktuellen Datensatz verschoben, der ein Bruchteil der Methode durch den Index ist, bei dem der Bruchteil "precpos- \> centrieslt dividiert" durch "precpos- \> centriestotal" ist.

Wenn diese Funktion fehlschlägt, bleibt die Cursorposition unverändert.

#### <a name="remarks"></a>Bemerkungen

Mit diesem Vorgang wird der Cursor durch die Tabelle an eine Position am folgenden ungefähren Punkt verschoben: precpos- \> centrieslt dividiert durch precpos- \> zentriestotal.

Wenn Updates fortlaufend in der Tabelle auftreten, können nachfolgende Aufrufe mit dem gleichen [JET_RECPOS](./jet-recpos-structure.md) den Cursor an verschiedene Positionen im Index verschieben, sowohl vor als auch nach der vorherigen Position. Die Transaktions Isolation gilt nicht für die Positionierung durch [JET_RECPOS](./jet-recpos-structure.md) , da Sie von den physischen Eigenschaften des Indexes abhängig ist, die nicht Transaktions isoliert sind.

[JET_RECPOS](./jet-recpos-structure.md) sollten nicht zum Beschreiben eines Datensatzes innerhalb einer Tabelle oder zum Neupositionieren eines Datensatzes in der Nähe eines vorhandenen Datensatzes verwendet werden. Stattdessen sollten Lesezeichen für einen vorhandenen Datensatz nach einer anfänglichen **jetgotoposition** abgerufen und dann zum Neupositionieren desselben Datensatzes verwendet werden.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)
