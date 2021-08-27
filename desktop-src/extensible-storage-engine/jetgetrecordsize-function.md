---
description: Weitere Informationen finden Sie unter JetGetRecordSize-Funktion.
title: JetGetRecordSize-Funktion
TOCTitle: JetGetRecordSize Function
ms:assetid: a28567ed-c732-4509-9f8d-6f8104f62a86
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294045(v=EXCHG.10)
ms:contentKeyID: 32765644
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 15a94f14962559a63c19c6dce97b1d6dc5a234fd
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982393"
---
# <a name="jetgetrecordsize-function"></a>JetGetRecordSize-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetrecordsize-function"></a>JetGetRecordSize-Funktion

Die **JetGetRecordSize-Funktion** ruft Informationen zur Datensatzgröße vom gewünschten Speicherort ab.

**Windows Vista: JetGetRecordSize** wird in Windows Vista eingeführt.

```cpp
    JET_ERR JET_API JetGetRecordSize(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Identifiziert den Datenbanksitzungskontext, der für den API-Aufruf verwendet wird.

*tableid*

Identifiziert die Tabelle oder den Cursor, die bzw. der für den API-Aufruf verwendet wird. Der Cursor muss auf einem Datensatz positioniert sein oder ein Update vorbereitet haben.

*precsize*

Ein Zeiger auf einen Ausgabepuffer für [die](./jet-recsize-structure.md) JET_RECSIZE Struktur.

*grbit*

Dies ist mindestens einer der folgenden Werte.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitRecordSizeInCopyBuffer</p> | <p>Dadurch wird die Größe des Datensatzes abgerufen, der sich im für die Aktualisierung vorbereiteten Kopierpuffer befindet. Andernfalls <em>muss die tableid</em> oder der Cursor auf einem Datensatz positioniert werden, und dieser Datensatz wird verwendet.</p> | 
| <p>JET_bitRecordSizeRunningTotal</p> | <p>Wenn dieses Bit angegeben <a href="gg294072(v=exchg.10).md"></a> wird, wird die JET_RECSIZE vor dem Auffüllen des Inhalts nicht auf Null gesetzt, was effektiv als Akkumulation der Statistiken für mehrere datensätze, die besucht oder aktualisiert werden, verwendet wird.</p> | 
| <p>JET_bitRecordSizeLocal</p> | <p>Dies bewirkt, dass die API nicht systeminterne Long-Werte ignoriert. Beispielsweise wird nur der lokale Datensatz auf der Seite verwendet.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Eine der angeforderten Optionen war ungültig oder nicht implementiert. Dieser Fehler wird von der <strong>JetGetRecordSize-Funktion</strong> zurückgegeben, wenn ein ungültiges <em>Grbit</em> angegeben wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz nicht initialisiert wurde.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable werden nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Es ist unzulässig, dieselbe Sitzung von mehr als einem Thread gleichzeitig zu verwenden.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable werden nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Dies kann passieren, wenn der Cursor falsch positioniert wurde.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Wenn der Cursor nicht in einer Transaktion positioniert wurde, kann dies passieren, wenn ein anderer Thread den Datensatz aus dieser Sitzung löscht.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Dies kann zurückgegeben werden, wenn eine <strong></strong><em>NULL-Precsize</em> übergeben wurde.</p> | 



#### <a name="remarks"></a>Bemerkungen

Die Größe des Schlüssels, der im **cbOverhead-Feld** von [JET_RECSIZE,](./jet-recsize-structure.md)wird durch die JET_bitRecordSizeInCopyBuffer. Wenn dieses Bit angegeben wird, ist die im **feld cbOverhead** gesammelte Schlüsselgröße die vollständige Schlüsselgröße. Wenn dieses Bit nicht verwendet wird, enthält die akkumulierte Schlüsselgröße keine aufgrund der Schlüsselpräfixkomprimierung gespeicherte Größe.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_TABLEID](./jet-tableid.md)
