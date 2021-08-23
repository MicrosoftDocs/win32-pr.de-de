---
description: 'Weitere Informationen zu: JetEscrowUpdate-Funktion'
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
ms.openlocfilehash: d244bf16ab02d0bfd6f975f63c2ece32ed40119b30c178e4674037d36f519508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667420"
---
# <a name="jetescrowupdate-function"></a>JetEscrowUpdate-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetescrowupdate-function"></a>JetEscrowUpdate-Funktion

Die **JetEscrowUpdate-Funktion** führt einen atomaren Additionsvorgang für eine Spalte aus. Diese Funktion ermöglicht es mehreren Sitzungen, denselben Datensatz gleichzeitig ohne Konflikte zu aktualisieren.

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

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*Columnid*

Die *columnid* der zu aktualisierenden Spalte.

*Pv*

Ein Zeiger auf einen Puffer, der das Add-In für die Spalte enthält.

*cbMax*

Die Größe des Puffers, der das Add-In enthält.

*pvOld*

Der Ausgabepuffer, der den aktuellen Wert der Spalte empfängt, wie er in der Datenbank gespeichert ist (Versionsinformationen werden ignoriert).

*cbOldMax*

Die maximale Größe des Ausgabepuffers, der den aktuellen Wert der Spalte empfängt. Derzeit wird nur JET_coltypLong unterstützt, sodass der Puffer entweder 4 Bytes oder 0 Bytes lang sein muss. Wenn *pvOld* NULL ist, sollte *cbOldMax* 0 sein.

*pwOldActual*

Empfängt die tatsächliche Menge an Rohwertdaten, die im Ausgabepuffer empfangen werden.

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
<td><p>JET_bitEscrowNoRollback</p></td>
<td><p>Auch wenn für die Sitzung, die das Escrow-Update ausführt, ein Transaktionsrollback ausgeführt wird, wird dieses Update nicht rückgängig. Beachten Sie Folgendes: Da die Protokolldatensätze möglicherweise nicht auf den Datenträger geleert werden, können kürzlich mit diesem Flag durchgeführte Escrow-Updates verlorengehen, wenn ein Absturz vorliegt.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Der Cursor verfügt über ein Update, das mit <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>vorbereitet wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Eine ungültige Puffergröße wurde übergeben. Derzeit wird nur JET_coltypLong unterstützt, sodass der Puffer 4 Bytes betragen muss.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOperation</p></td>
<td><p>Es wurde eine ungültige Spalte angegeben. Die Spalte muss mit JET_bitColumnEscrowUpdate angegeben werden. Nur feste Spalten von JET_coltypLong können als escrow updateable angegeben werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor muss sich in einem Datensatz befinden, um eine Spalte zu aktualisieren.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Escrow-Updates können nur von Sitzungen in einer Transaktion ausgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Cursor kann nicht schreibbar sein und einen Datensatz aktualisieren.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht von mehreren Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Die Sitzung muss über Schreibberechtigungen zum Aktualisieren eines Datensatzes verfügen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Der Fehler, der zurückgegeben wird, wenn ein in Konfliktstehendes Update angefordert wird.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Hinweise

Wenn zwei Sitzungen versuchen, einen Datensatz gleichzeitig zu aktualisieren, erhält die zweite Sitzung normalerweise einen JET_errWriteConflict Fehler, es sei denn, die Sitzungen sind vollständig serialisiert. Um zwei Sitzungen zu serialisieren, die denselben Datensatz aktualisieren, muss die zweite Sitzung ihre Transaktion starten, nachdem die erste Transaktion einen Commit für die Transaktion ausgeführt hat. Weitere Informationen finden Sie unter [JetBeginTransaction.](./jetbegintransaction-function.md)

Mehrere Spalten im selben Datensatz können aktualisiert werden. Die Updates wirken sich nicht gegenseitig aus.

Nur **JetEscrowUpdate-Vorgänge** sind miteinander kompatibel. Wenn zwei verschiedene Sitzungen versuchen, Updates vorzubereiten oder denselben Datensatz zu löschen, wird ein Schreibkonflikt generiert.

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
<strong>JetEscrowUpdate</strong></p></th>
<th><p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></p></th>
<th><p><a href="gg269315(v=exchg.10).md">JetDelete</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>JetEscrowUpdate</strong></p></td>
<td><p>JET_errSuccess</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><a href="gg269288(v=exchg.10).md">JetUpdate</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="odd">
<td><p>Sitzung A</p></td>
<td><p><a href="gg269315(v=exchg.10).md">JetDelete</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
</tbody>
</table>


Escrow-Vorgänge werden mithilfe von [JetRollback](./jetrollback-function.md) versioniert und rückgängig erklärt (es sei denn, JET_bitEscrowNoRollback wurde angegeben). **JetEscrowUpdate** gibt den Rohwert der in der Datenbank gespeicherten Spalte zurück, da eine Anwendung möglicherweise eine besondere Aktion ausführen möchte, wenn ein Sentinelwert erreicht wird. [JetRetrieveColumn gibt](./jetretrievecolumn-function.md) die Ansicht mit korrekter Versionierung der Spalte zurück und ignoriert updates, die von gleichzeitigen Sitzungen vorgenommen wurden.

Wenn zwei Sitzungen für dieselbe Spalte desselben Datensatzes ausgeführt werden, können wir sehen, wie dies funktioniert. Angenommen, die Spalte beginnt mit dem Wert 0.

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
<td><p>Ein</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Ein</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>Ein</p></td>
<td><p><strong>JetEscrowUpdate</strong> (4)</p></td>
<td><p>4</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Ein</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>4</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><strong>JetEscrowUpdate</strong> (3)</p></td>
<td><p>7</p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p>Ein</p></td>
<td><p><strong>JetEscrowUpdate</strong> (2)</p></td>
<td><p>9</p></td>
<td><p>7</p></td>
</tr>
<tr class="even">
<td><p>Ein</p></td>
<td><p><strong>JetEscrowUpdate</strong> (-7)</p></td>
<td><p>2</p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>Ein</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>–1</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269273(v=exchg.10).md">JetRollback</a></p></td>
<td><p>–1</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Ein</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>–1</p></td>
</tr>
</tbody>
</table>


Es wird davon abraten, einen Datensatz in derselben Transaktion zu ersetzen, die Aktualisierungen an einem Datensatz ausführt. Insbesondere wenn ein Update für einen Datensatz mit einer [JET_TABLEID](./jet-tableid.md) vorbereitet wird und eine andere [JET_TABLEID](./jet-tableid.md) verwendet wird, um den Datensatz zu aktualisieren, geht die aktualisierte Escrow verloren, wenn [JetUpdate](./jetupdate-function.md) aufgerufen wird. Dies geschieht auch, wenn die Spalte "escrow" während des Updates nicht festgelegt wurde.

Wenn eine spalte, die aktualisiert werden kann, einen Wert von 0 hat, kann ein spezielles Verhalten ausgelöst werden. Dieses Verhalten tritt nur auf, wenn **ein JetEscrowUpdate-Vorgang** bewirkt, dass die Spalte den Wert 0 hat. Die Aktion erfolgt nicht sofort, sondern irgendwann nach der Transaktion, die dazu führte, dass die Spalte den Wert 0 (null) Commits hatte. Die Spalte muss weiterhin den Wert 0 (null) haben (d. h., wenn die Spalte von keiner anderen Sitzung geändert wurde). Wenn die Spalte mit einem JET_bitColumnDeleteOnZero wurde, wird der Datensatz gelöscht, der die Spalte enthält. Wenn die Spalte mit einem JET_bitColumnFinalize wurde, wird ein Rückruf ausgegeben. Ein Absturz kann dazu führen, dass diese Aktionen nicht ausgeführt werden, aber die Onlinewartung (mit der [JetDefragment-Funktion)](./jetdefragment-function.md) wird die Aktionen ordnungsgemäß wiederholen.

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
<td><p>Wird in Esent.h deklariert.</p></td>
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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
