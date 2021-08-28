---
description: 'Weitere Informationen finden Sie unter: JetGetRecordPosition-Funktion'
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
ms.openlocfilehash: bd1e84b995485afd46119b78289c1cac23e19215
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982433"
---
# <a name="jetgetrecordposition-function"></a>JetGetRecordPosition-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetrecordposition-function"></a>JetGetRecordPosition-Funktion

Die **JetGetRecordPosition-Funktion** gibt die Bruchposition des aktuellen Datensatzes im aktuellen Index in Form einer JET_RECPOS [zurück.](./jet-recpos-structure.md) Diese Struktur beschreibt Bruchpositionen in Bezug auf eine ungefähre Anzahl von Indexeinträgen vor dem aktuellen Datensatz und eine ungefähre Gesamtzahl von Einträgen im Index.

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*precpos*

Die Beschreibung des Bruchs, der zum Abrufen der Position des aktuellen Datensatzes im aktuellen Index verwendet werden soll.

*cbRecpos*

Die Größe des Arbeitsspeichers, der beim *Precpos zugeordnet ist.*

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Dieser Vorgang kann nicht abgeschlossen werden, da für die -Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist. Der Zugriff auf alle Daten muss widerrufen werden, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows 2000:</strong>  Dieser Fehler wird vom Betriebssystem Windows 2000 nicht zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Die Größe des zugeordneten Arbeitsspeichers bei <em>der</em> Vorbereitung ist nicht ausreichend.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor befindet sich derzeit nicht in einem Datensatz und kann keine Position zurückgeben.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die -Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungsvorgang durchgeführt wird.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p><strong>Windows 2000:</strong>  Dieser Fehler wird vom Betriebssystem Windows 2000 nicht zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird die ungefähre Anzahl von Indexeinträgen vor dem aktuellen Datensatz im Index in precpos- \> centriesLT zurückgegeben. 1 wird in precpos- \> centriesInRange zurückgegeben. Die ungefähre Anzahl von Einträgen im Index wird in precpos- \> centriesTotal zurückgegeben.

Bei einem Fehler werden keine Änderungen am Speicher vorgenommen, der im *Voraus zugeordnet wurde.*

#### <a name="remarks"></a>Bemerkungen

Dieser Vorgang gibt unterschiedliche Daten zurück, wenn updates kontinuierlich für die Tabelle erfolgen. Die Änderungen an den Werten entsprechen nicht immer den Erwartungen, die auf den Informationen zu den Updates basieren, da die Werte Näherungen sind, die auf den physischen Eigenschaften des Indexes basieren. Die Transaktionsisolation gilt nicht für Positionen von **JetGetRecordPosition,** da die Werte von physischen Eigenschaften des Indexes abhängen, die nicht transaktionsisoliert sind.

[JET_RECPOS](./jet-recpos-structure.md) sollte nicht verwendet werden, um einen Datensatz innerhalb einer Tabelle zu beschreiben oder einen Datensatz in der Nähe eines vorhandenen Datensatzes neu zu positionieren. Stattdessen sollten Lesezeichen für einen vorhandenen Datensatz abgerufen und dann verwendet werden, um denselben Datensatz neu zu positionieren.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetGotoPosition](./jetgotoposition-function.md)  
[JetStopService](./jetstopservice-function.md)
