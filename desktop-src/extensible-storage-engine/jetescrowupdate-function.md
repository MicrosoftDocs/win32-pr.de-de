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
ms.openlocfilehash: e9f037b8c26829d7b1f3a10b05e1d4bd83bd186a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469797"
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


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitEscrowNoRollback</p> | <p>Auch wenn für die Sitzung, die das Escrow-Update ausführt, ein Transaktionsrollback ausgeführt wird, wird dieses Update nicht rückgängig. Beachten Sie Folgendes: Da die Protokolldatensätze möglicherweise nicht auf den Datenträger geleert werden, können kürzlich mit diesem Flag durchgeführte Escrow-Updates verlorengehen, wenn ein Absturz vorliegt.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errAlreadyPrepared</p> | <p>Für den Cursor wurde ein Update mit <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>vorbereitet.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Eine ungültige Puffergröße wurde übergeben. Derzeit wird nur JET_coltypLong unterstützt, sodass der Puffer 4 Bytes betragen muss.</p> | 
| <p>JET_errInvalidOperation</p> | <p>Es wurde eine ungültige Spalte angegeben. Die Spalte muss mit JET_bitColumnEscrowUpdate angegeben werden. Nur feste Spalten von JET_coltypLong können als escrow updateable angegeben werden.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor muss sich in einem Datensatz befinden, um eine Spalte zu aktualisieren.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Escrow-Updates können nur von Sitzungen in einer Transaktion ausgeführt werden.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Cursor kann nicht schreibbar sein und einen Datensatz aktualisieren.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht von mehreren Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Die Sitzung muss über Schreibberechtigungen zum Aktualisieren eines Datensatzes verfügen.</p> | 
| <p>JET_errWriteConflict</p> | <p>Der Fehler, der zurückgegeben wird, wenn ein in Konfliktstehendes Update angefordert wird.</p> | 



#### <a name="remarks"></a>Hinweise

Wenn zwei Sitzungen versuchen, einen Datensatz gleichzeitig zu aktualisieren, erhält die zweite Sitzung normalerweise einen JET_errWriteConflict Fehler, es sei denn, die Sitzungen sind vollständig serialisiert. Um zwei Sitzungen zu serialisieren, die denselben Datensatz aktualisieren, muss die zweite Sitzung ihre Transaktion starten, nachdem die erste Transaktion einen Commit für die Transaktion ausgeführt hat. Weitere Informationen finden Sie unter [JetBeginTransaction.](./jetbegintransaction-function.md)

Mehrere Spalten im selben Datensatz können aktualisiert werden. Die Updates wirken sich nicht gegenseitig aus.

Nur **JetEscrowUpdate-Vorgänge** sind miteinander kompatibel. Wenn zwei verschiedene Sitzungen versuchen, Updates vorzubereiten oder denselben Datensatz zu löschen, wird ein Schreibkonflikt generiert.


| <p></p> | <p></p> | <p>Sitzung B<br /><strong>JetEscrowUpdate</strong></p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | 
|---------|---------|--------------------------------------------------------|---------------------------------------------------------------|--------------------------------------------------------|
| <p></p> | <p><strong>JetEscrowUpdate</strong></p> | <p>JET_errSuccess</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p></p> | <p><a href="gg269288(v=exchg.10).md">JetUpdate</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p>Sitzung A</p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 



Escrow-Vorgänge werden mithilfe von [JetRollback](./jetrollback-function.md) versioniert und rückgängig erklärt (es sei denn, JET_bitEscrowNoRollback wurde angegeben). **JetEscrowUpdate** gibt den Rohwert der in der Datenbank gespeicherten Spalte zurück, da eine Anwendung möglicherweise eine besondere Aktion ausführen möchte, wenn ein Sentinelwert erreicht wird. [JetRetrieveColumn](./jetretrievecolumn-function.md) gibt die Ansicht mit der richtigen Version der Spalte zurück, wobei Updates von gleichzeitigen Sitzungen ignoriert werden.

Bei zwei Sitzungen, die auf derselben Spalte desselben Datensatzes arbeiten, können wir sehen, wie dies funktioniert. Angenommen, die Spalte beginnt mit dem Wert 0.


| <p>Sitzung</p> | <p>Vorgang</p> | <p>Gespeicherter Wert</p> | <p>Rückgabewert</p> | 
|----------------|------------------|---------------------|-----------------------|
| <p>Ein</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p></p> | 
| <p>Ein</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p>0</p> | 
| <p>Ein</p> | <p><strong>JetEscrowUpdate</strong> (4)</p> | <p>4</p> | <p>0</p> | 
| <p>Ein</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></p> | <p></p> | <p></p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>0</p> | 
| <p>B</p> | <p><strong>JetEscrowUpdate</strong> (3)</p> | <p>7</p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>Ein</p> | <p><strong>JetEscrowUpdate</strong> (2)</p> | <p>9</p> | <p>7</p> | 
| <p>Ein</p> | <p><strong>JetEscrowUpdate</strong> (-7)</p> | <p>2</p> | <p>9</p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>Ein</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 
| <p>B</p> | <p><a href="gg269273(v=exchg.10).md">JetRollback</a></p> | <p>-1</p> | <p></p> | 
| <p>Ein</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 



Es wird nicht empfohlen, einen Datensatz in derselben Transaktion zu ersetzen, die Escrow-Updates für einen Datensatz ausführt. Insbesondere wenn ein Update für einen Datensatz mit einem [JET_TABLEID](./jet-tableid.md) vorbereitet wird und ein anderer [JET_TABLEID](./jet-tableid.md) verwendet wird, um den Datensatz zu aktualisieren, geht die aktualisierte Füllung verloren, wenn [JetUpdate](./jetupdate-function.md) aufgerufen wird. Dies geschieht auch, wenn die Spalte escrow während des Updates nicht festgelegt wurde.

Wenn eine spalte, die aktualisierbar ist, den Wert 0 hat, kann ein besonderes Verhalten ausgelöst werden. Dieses Verhalten tritt nur auf, wenn ein **JetEscrowUpdate-Vorgang** bewirkt, dass die Spalte den Wert 0 (null) hat. Die Aktion findet nicht sofort statt, sondern tritt irgendwann nach der Transaktion auf, die dazu geführt hat, dass die Spalte den Wert 0 (null) Commits hat. Die Spalte muss weiterhin den Wert 0 (null) aufweisen (d. b. wenn die Spalte von keiner anderen Sitzung geändert wurde). Wenn die Spalte mit JET_bitColumnDeleteOnZero erstellt wurde, wird der Datensatz mit der Spalte gelöscht. Wenn die Spalte mit JET_bitColumnFinalize erstellt wurde, wird ein Rückruf ausgegeben. Ein Absturz kann dazu führen, dass diese Aktionen nicht ausgeführt werden, aber bei der Onlinewartung (mit der [JetDefragment-Funktion)](./jetdefragment-function.md) werden die Aktionen ordnungsgemäß wiederholt.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



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
