---
description: Weitere Informationen finden Sie in der jetindexrecordcount-Funktion.
title: Jetindexrecordcount-Funktion
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524965"
---
# <a name="jetindexrecordcount-function"></a>Jetindexrecordcount-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetindexrecordcount-function"></a>Jetindexrecordcount-Funktion

Die **jetindexrecordcount** -Funktion zählt die Anzahl der Einträge im aktuellen Index von der aktuellen Position nach vorne. Die aktuelle Position ist in der Anzahl enthalten. Die Anzahl kann größer als die Gesamtanzahl der Datensätze in der Tabelle sein, wenn der aktuelle Index eine mehrwertige Spalte überschreitet und Instanzen der Spalte mehrere Werte aufweisen. Wenn die Tabelle leer ist, wird 0 für die Anzahl zurückgegeben.

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*pkrec*

Der Zeiger auf einen Long-Wert ohne Vorzeichen, der die Anzahl empfängt.

*crecmax*

Die maximale Anzahl der zu zählenden Datensätze. Ein *crecmax* -Wert von 0 gibt an, dass die Anzahl unbegrenzt ist.

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
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor befindet sich derzeit nicht in einem Datensatz, und die Tabelle ist nicht leer.</p>
<p><strong>Windows XP, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:</strong>  Wenn der Cursor auf einem leeren Index oder Index Bereich positioniert ist, gibt <strong>jetindexrecordcount</strong> irrtümlich JET_errNoCurrentRecord zurück.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird die genaue Anzahl von Indexeinträgen, einschließlich der aktuellen Position und bis zu *crecmax* (wenn Sie nicht 0 ist), in "Ganzzahl ohne Vorzeichen long" zurückgegeben, auf das *pkrec* zeigt.

Wenn diese Funktion fehlschlägt, werden keine Änderungen an dem bei den *Vorgängen* zugeordneten Arbeitsspeicher vorgenommen.

#### <a name="remarks"></a>Bemerkungen

Wenn die Tabelle nicht leer ist, sollte der Cursor auf dem Datensatz positioniert werden, von dem aus die Anzahl begonnen werden soll. Die Anzahl schließt diesen Datensatz ein, und der Zähler wird auf den angegebenen Grenzwert in *crecmax* angerechnet. Wenn *crecmax* den Wert 0 hat, wird der Vorgang bis zum Ende des Indexes fortgesetzt.

Index Bereiche können zum Erstellen von künstlichen Index Beschränkungen für die Anzahl verwendet werden. Auf diese Weise können die Unterbereiche eines Indexes genau gezählt werden. Der Cursor sollte in der ersten Zeile im Bereich positioniert werden. Das Ende des Bereichs Schlüssels sollte festgelegt werden, und anschließend sollte [jetsetindexrange](./jetsetindexrange-function.md) verwendet werden, um den oberen Bereich festzulegen, entweder inklusiv oder exklusiv. Schließlich sollte **jetindexrecordcount** aufgerufen werden, um den Bereich exakt zu zählen.

**Jetindexrecordcount** befolgt die Transaktions Semantik und gibt eine Anzahl zurück, die für diese bestimmte Sitzung im aktuellen Transaktionszustand korrekt ist.

**Jetindexrecordcount** greift auf Blattseiten des Indexes zu, um Einträge exakt zu zählen. Folglich kann es viele e/a-Vorgänge durchführen und kann langsam sein. Die *crecmax* -Einschränkung sollte verwendet werden, um eine übermäßige Auslastung zu verhindern. Wenn ein Bereich groß ist, kann es vorkommen, dass der Bereich mithilfe von [jetgetrecordposition](./jetgetrecordposition-function.md)in einer näherten Weise gezählt wird.

**Windows XP, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:**  Wenn der Cursor auf einem leeren Index oder Index Bereich positioniert ist, gibt **jetindexrecordcount** irrtümlich JET_errNoCurrentRecord zurück, anstatt eine Daten Satz Anzahl von 0 (null) zurückzugeben. Die Anwendung sollte überprüfen, ob der Index-oder Index Bereich in diesem Fall leer ist.

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

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetgetrecordposition](./jetgetrecordposition-function.md)  
[Jetsetindexrange](./jetsetindexrange-function.md)  
[Jetstopservice](./jetstopservice-function.md)
