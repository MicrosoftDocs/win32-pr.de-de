---
description: 'Weitere Informationen zu: jetescrowupdate-Funktion'
title: JetEscrowUpdate-Funktion
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369753"
---
# <a name="jetescrowupdate-function"></a>JetEscrowUpdate-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetescrowupdate-function"></a>JetEscrowUpdate-Funktion

Die **jetescrowupdate** -Funktion führt eine atomarische Additions Operation für eine Spalte aus. Diese Funktion ermöglicht es mehreren Sitzungen, denselben Datensatz gleichzeitig zu aktualisieren, ohne dass Konflikte auftreten.

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*ColumnID*

Das *ColumnID* der zu aktualisierenden Spalte.

*teuren*

Ein Zeiger auf einen Puffer, der den Addend für die Spalte enthält.

*cbmax*

Die Größe des Puffers, der den Addend enthält.

*pvold*

Der Ausgabepuffer, der den aktuellen Wert der Spalte erhält, wie er in der Datenbank gespeichert wird (die Versionsverwaltung wird ignoriert).

*cboldmax*

Die maximale Größe des Ausgabepuffers, der den aktuellen Wert der Spalte empfängt. Derzeit wird nur JET_coltypLong unterstützt, daher muss der Puffer entweder 4 Bytes oder 0 Byte lang sein. Wenn *pvold* NULL ist, sollte *cboldmax* den Wert 0 aufweisen.

*pcboldactual*

Empfängt die tatsächliche Menge an rohwertdaten, die im Ausgabepuffer empfangen werden.

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
<td><p>JET_bitEscrowNoRollback</p></td>
<td><p>Auch wenn für die Sitzung, die das hinterlegter-Update ausführt, ein Rollback der Transaktion ausgeführt wird, wird dieses Update nicht rückgängig gemacht. Beachten Sie, dass die Protokolldaten Sätze möglicherweise nicht auf den Datenträger geleert werden, wenn ein Absturz vorliegt.</p></td>
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
<td><p>JET_errAlreadyPrepared</p></td>
<td><p>Der Cursor verfügt über ein Update, das mit <a href="gg269339(v=exchg.10).md">jetprepareupdate</a>vorbereitet wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Es wurde eine ungültige Puffergröße übermittelt. Derzeit wird nur JET_coltypLong unterstützt, daher muss der Puffer 4 Bytes groß sein.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOperation</p></td>
<td><p>Es wurde eine ungültige Spalte angegeben. Die Spalte muss mit JET_bitColumnEscrowUpdate angegebenen erstellt werden. Nur festgelegte Spalten von JET_coltypLong können als zu aktualisierbare Hinterlegungs Möglichkeiten angegeben werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor muss sich in einem Datensatz befinden, um eine Spalte zu aktualisieren.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Hinterlegte Updates können nur von Sitzungen in einer Transaktion ausgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Der Cursor kann nicht schreibgeschützt sein und einen Datensatz aktualisieren.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht gleichzeitig von mehreren Threads verwendet werden. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Die Sitzung muss über Schreibberechtigungen zum Aktualisieren eines Datensatzes verfügen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Der zurückgegebene Fehler, wenn ein in Konflikt stehender Update angefordert wird.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Wenn zwei Sitzungen versuchen, einen Datensatz gleichzeitig zu aktualisieren, empfängt die zweite Sitzung normalerweise einen JET_errWriteConflict Fehler, es sei denn, die Sitzungen werden vollständig serialisiert. Zum Serialisieren von zwei Sitzungen, die denselben Datensatz aktualisieren, muss die zweite Sitzung die Transaktion starten, nachdem die erste Transaktion einen Commit für die Transaktion ausgeführt hat. Weitere Informationen finden Sie unter [jetbegintransaction](./jetbegintransaction-function.md) .

Mehrere Spalten im gleichen Datensatz können mit einem Hinterlegungs Wert aktualisiert werden. Die Updates wirken sich nicht gegenseitig aus.

Nur **jetescrowupdate** -Vorgänge sind miteinander kompatibel. Wenn zwei verschiedene Sitzungen versuchen, Updates vorzubereiten oder denselben Datensatz zu löschen, wird ein Schreib Konflikt generiert.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p>Sitzung B<br />
<strong>Jetescrowupdate</strong></p></th>
<th><p><a href="gg269339(v=exchg.10).md">Jetprepareupdate</a></p></th>
<th><p><a href="gg269315(v=exchg.10).md">Jetdelete</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Jetescrowupdate</strong></p></td>
<td><p>JET_errSuccess</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><a href="gg269288(v=exchg.10).md">Jetupdate</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="odd">
<td><p>Sitzung A</p></td>
<td><p><a href="gg269315(v=exchg.10).md">Jetdelete</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
</tbody>
</table>


Hinterlegte Vorgänge werden mit einer Versions Angabe versehen und mit [jetrollback Rück](./jetrollback-function.md) gängig gemacht (es sei denn, JET_bitEscrowNoRollback wurde angegeben). **Jetescrowupdate** gibt den Rohwert der in der Datenbank gespeicherten Spalte zurück, weil eine Anwendung möglicherweise eine spezielle Aktion ausführt, wenn ein Sentinelwert getroffen wird. [Jetretrievecolumn](./jetretrievecolumn-function.md) gibt die korrekt versionierte Sicht der Spalte zurück, wobei Updates von gleichzeitigen Sitzungen ignoriert werden.

Wenn zwei Sitzungen in derselben Spalte desselben Datensatzes ausgeführt werden, können wir sehen, wie dies funktioniert. Angenommen, die Spalte beginnt mit einem Wert von 0.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Sitzung</p></th>
<th><p>Vorgang</p></th>
<th><p>Gespeicherter Wert</p></th>
<th><p>Rückgabewert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p><a href="gg294083(v=exchg.10).md">Jetbegintransations</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg294083(v=exchg.10).md">Jetbegintransations</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>A</p></td>
<td><p><strong>Jetescrowupdate</strong> (4)</p></td>
<td><p>4</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></p></td>
<td><p></p></td>
<td><p>4</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg294083(v=exchg.10).md">Jetbegintransaction</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><strong>Jetescrowupdate</strong> (3)</p></td>
<td><p>7</p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p>A</p></td>
<td><p><strong>Jetescrowupdate</strong> (2)</p></td>
<td><p>9</p></td>
<td><p>7</p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><strong>Jetescrowupdate</strong> (-7)</p></td>
<td><p>2</p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269273(v=exchg.10).md">Jetrollback</a></p></td>
<td><p>-1</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
</tbody>
</table>


Es wird nicht empfohlen, einen Datensatz in der gleichen Transaktion zu ersetzen, der Änderungen an einem Datensatz ausführt. Insbesondere, wenn ein Update für einen Datensatz mit einem [JET_TABLEID](./jet-tableid.md) vorbereitet wird und ein anderer [JET_TABLEID](./jet-tableid.md) verwendet wird, um die Aktualisierung des Datensatzes zu übernehmen, geht der aktualisierte hinterlegter-Wert verloren, wenn [jetupdate](./jetupdate-function.md) aufgerufen wird. Dies geschieht auch, wenn die hinterlegte Spalte während des Updates nicht festgelegt wurde.

Wenn für eine aktualisierbare Hinterlegungs Spalte der Wert 0 (null) festgelegt ist, kann ein spezielles Verhalten ausgelöst werden. Dieses Verhalten tritt nur auf, wenn ein **jetescrowupdate** -Vorgang bewirkt, dass die Spalte den Wert 0 (null) aufweist. Die Aktion wird nicht sofort ausgeführt. Sie tritt jedoch irgendwann nach der Transaktion auf, die bewirkt hat, dass die Spalte einen Wert von 0 (null) hat. Die Spalte muss weiterhin den Wert 0 (null) aufweisen (d. h., wenn keine anderen Sitzungen die Spalte geändert haben). Wenn die Spalte mit JET_bitColumnDeleteOnZero erstellt wurde, wird der Datensatz, der die Spalte enthält, gelöscht. Wenn die Spalte mit JET_bitColumnFinalize erstellt wurde, wird ein Rückruf ausgegeben. Ein Absturz kann dazu führen, dass diese Aktionen nicht ausgeführt werden, aber die Online Wartung (mithilfe der [jetdefragment](./jetdefragment-function.md) -Funktion) führt zu einer ordnungsgemäßen Wiederholung der Aktionen.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetbegintransaction](./jetbegintransaction-function.md)  
[Jetdebug](./jetdefragment-function.md)  
[Jetprepareupdate](./jetprepareupdate-function.md)  
[Jetretrievecolumschlag](./jetretrievecolumn-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[Jetupdate](./jetupdate-function.md)
