---
description: 'Weitere Informationen zu: JetGetRecordSize-Funktion'
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
ms.openlocfilehash: f42defeefa4d01648d34b971cce994fbebf8f0e8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481296"
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

Ein Zeiger auf einen [](./jet-recsize-structure.md) Ausgabepuffer für die JET_RECSIZE-Struktur.

*grbit*

Dies ist mindestens einer der folgenden Werte.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitRecordSizeInCopyBuffer</p> | <p>Dadurch wird die Größe des Datensatzes abgerufen, der sich im für das Update vorbereiteten Kopierpuffer befindet. Andernfalls muss <em>tableid</em> oder cursor auf einem Datensatz positioniert werden, und dieser Datensatz wird verwendet.</p> | 
| <p>JET_bitRecordSizeRunningTotal</p> | <p>Wenn dieses Bit angegeben wird, wird die <a href="gg294072(v=exchg.10).md">JET_RECSIZE</a> vor dem Auffüllen des Inhalts nicht auf Null gesetzt, was effektiv als Ansammlung der Statistiken für mehrere Datensätze fungiert, die besucht oder aktualisiert wurden.</p> | 
| <p>JET_bitRecordSizeLocal</p> | <p>Dies bewirkt, dass die API nicht systeminterne Long-Werte ignoriert. Beispielsweise wird nur der lokale Datensatz auf der Seite verwendet.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Eine der angeforderten Optionen war ungültig oder nicht implementiert. Dieser Fehler wird von der <strong>JetGetRecordSize-Funktion</strong> zurückgegeben, wenn ein ungültiges <em>Grbit</em> angegeben wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz nicht initialisiert wurde.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable werden nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Es ist unzulässig, dieselbe Sitzung von mehreren Threads gleichzeitig zu verwenden.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable werden nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Dies kann passieren, wenn der Cursor falsch positioniert wurde.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Wenn der Cursor nicht in einer Transaktion positioniert wurde, kann dies passieren, wenn ein anderer Thread den Datensatz aus unter dieser Sitzung löscht.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Dies kann zurückgegeben werden, wenn eine<em>NULL-Präcsize</em> übergeben wurde. <strong></strong></p> | 



#### <a name="remarks"></a>Hinweise

Die Größe des Schlüssels, der sich im **cbOverhead-Feld** von [JET_RECSIZE](./jet-recsize-structure.md)angesammelt hat, wird von JET_bitRecordSizeInCopyBuffer beeinflusst. Wenn dieses Bit angegeben wird, entspricht die im **cbOverhead-Feld** akkumulierte Schlüsselgröße der vollständigen Schlüsselgröße. Wenn dieses Bit nicht verwendet wird, enthält die akkumulierte Schlüsselgröße aufgrund der Schlüsselpräfixkomprimierung keine gespeicherte Größe.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_TABLEID](./jet-tableid.md)
