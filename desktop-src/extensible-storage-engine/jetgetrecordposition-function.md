---
description: 'Weitere Informationen zu: jetgetrecordposition-Funktion'
title: JetGetRecordPosition-Funktion
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042356"
---
# <a name="jetgetrecordposition-function"></a>JetGetRecordPosition-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetrecordposition-function"></a>JetGetRecordPosition-Funktion

Die **jetgetrecordposition** -Funktion gibt die Bruch Position des aktuellen Datensatzes im aktuellen Index in Form einer [JET_RECPOS](./jet-recpos-structure.md) Struktur zurück. Diese Struktur beschreibt Bruch Positionen in Bezug auf eine ungefähre Anzahl von Indexeinträgen vor dem aktuellen Datensatz und eine ungefähre Gesamtzahl von Einträgen im Index.

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*präpos*

Die Beschreibung des Bruchteils, der verwendet wird, um die Position des aktuellen Datensatzes im aktuellen Index zu erhalten.

*cbrecpos*

Die Größe des Arbeitsspeichers, der in den- *präpos* zugeordnet ist

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
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Dieser Vorgang kann nicht ausgeführt werden, weil der der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist. Es ist erforderlich, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows 2000:</strong>  Dieser Fehler wird vom Betriebssystem Windows 2000 nicht zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Die Größe des zugeordneten Arbeitsspeichers bei den <em>präpos</em> ist nicht ausreichend.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor befindet sich derzeit nicht in einem Datensatz und kann keine Position zurückgeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p><strong>Windows 2000:</strong>  Dieser Fehler wird vom Betriebssystem Windows 2000 nicht zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird die ungefähre Anzahl der Indexeinträge, die dem aktuellen Datensatz im Index vorangestellt sind, in "precpos- \> centrieslt" zurückgegeben. 1 wird in "precpos- \> centriesinrange" zurückgegeben. Die ungefähre Anzahl von Einträgen im Index wird in "precpos- \> centriestotal" zurückgegeben.

Bei einem Fehler werden keine Änderungen an dem Arbeitsspeicher vorgenommen, der in den *präpos* zugeordnet ist.

#### <a name="remarks"></a>Bemerkungen

Mit diesem Vorgang werden unterschiedliche Daten zurückgegeben, wenn Updates kontinuierlich in der Tabelle auftreten. Die Änderungen in den Werten entsprechen nicht immer den Erwartungen, die auf dem Wissen der Updates basieren, da die Werte auf Grundlage physischer Eigenschaften des Indexes zu Näherungen gehören. Die Transaktions Isolation gilt nicht für Positionen von **jetgetrecordposition** , da die Werte von den physischen Eigenschaften des Indexes abhängen, die nicht Transaktions isoliert sind.

[JET_RECPOS](./jet-recpos-structure.md) sollten nicht zum Beschreiben eines Datensatzes innerhalb einer Tabelle oder zum Neupositionieren eines Datensatzes in der Nähe eines vorhandenen Datensatzes verwendet werden. Stattdessen sollten Lesezeichen für einen vorhandenen Datensatz abgerufen und dann zum Neupositionieren desselben Datensatzes verwendet werden.

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
[Jetgotoposition](./jetgotoposition-function.md)  
[Jetstopservice](./jetstopservice-function.md)
