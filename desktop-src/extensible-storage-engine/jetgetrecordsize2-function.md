---
description: 'Weitere Informationen finden Sie hier: JetGetRecordSize2-Funktion'
title: JetGetRecordSize2-Funktion
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363016"
---
# <a name="jetgetrecordsize2-function"></a>JetGetRecordSize2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetrecordsize2-function"></a>JetGetRecordSize2-Funktion

Die **JetGetRecordSize2** -Funktion Ruft Informationen zur Daten Satz Größe vom gewünschten Speicherort ab.

**Windows 7: JetGetRecordSize2** wird im Betriebssystem Windows 7 eingeführt.

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Identifiziert den Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet wird.

*TableID*

Identifiziert die Tabelle oder den Cursor, die für den API-Befehl verwendet werden. Der Cursor muss auf einem Datensatz positioniert werden, oder es muss ein Update vorbereitet werden.

*prägrößengröße*

Ein Zeiger auf einen Ausgabepuffer für die [JET_RECSIZE2](./jet-recsize2-structure.md) -Struktur.

*grbit*

Dabei handelt es sich um einen oder mehrere der folgenden Werte.

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
<td><p>JET_bitRecordSizeInCopyBuffer</p></td>
<td><p>Dadurch wird die Größe des Datensatzes abgerufen, der sich im Kopier Puffer befindet, der für das Update vorbereitet wurde. Andernfalls muss <em>TableID</em> oder Cursor auf einem Datensatz positioniert werden, und dieser Datensatz wird verwendet.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordSizeRunningTotal</p></td>
<td><p>Wenn dieses Bit festgelegt ist, wird das <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> vor dem Ausfüllen des Inhalts nicht mit nullte versehen, was effektiv als Ansammlung der Statistiken für mehrere besuchte oder aktualisierte Datensätze fungiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRecordSizeLocal</p></td>
<td><p>Dies bewirkt, dass die API nicht intrinsische Long-Werte ignoriert. Beispielsweise wird nur der lokale Datensatz auf der Seite verwendet.</p></td>
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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Eine der angeforderten Optionen war ungültig oder nicht implementiert. Dieser Fehler wird von der <strong>JetGetRecordSize2</strong> -Funktion zurückgegeben, wenn ein ungültiges <em>grbit</em> angegeben wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:  </strong> JET_errInstanceUnavailable werden nur vom Betriebssystem Windows XP und höheren Versionen von Windows zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Es ist nicht zulässig, dieselbe Sitzung für mehr als einen Thread gleichzeitig zu verwenden.</p>
<p><strong>Windows XP:  </strong> JET_errInstanceUnavailable werden nur von Windows XP und höheren Versionen von Windows zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Dies kann vorkommen, wenn der Cursor falsch positioniert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Wenn der Cursor nicht in einer Transaktion positioniert war, kann dies vorkommen, wenn der Datensatz von einem anderen Thread aus in dieser Sitzung gelöscht wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Dies kann zurückgegeben werden, wenn eine <strong>null</strong>-<em>prägrößengröße</em> überschritten wurde.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Die Größe des Schlüssels, der im **cboverhead** -Feld von [JET_RECSIZE2](./jet-recsize2-structure.md)akkumuliert wurde, ist von JET_bitRecordSizeInCopyBuffer betroffen. Wenn dieses Bit angegeben ist, ist die Schlüsselgröße, die im Feld **cboverhead** akkumuliert wurde, die vollständige Schlüsselgröße. Wenn dieses Bit nicht verwendet wird, enthält die akkumulierte Schlüsselgröße keine Größe, die aufgrund der Schlüssel Präfix Komprimierung gespeichert wird.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008.</p></td>
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
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)
