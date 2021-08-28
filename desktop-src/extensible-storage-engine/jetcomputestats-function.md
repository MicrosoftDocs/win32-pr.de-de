---
description: 'Weitere Informationen zu: JetComputeStats-Funktion'
title: JetComputeStats-Funktion
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d990e4ded7dc2485bec6b5ecf92d9999aad57ce5
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981973"
---
# <a name="jetcomputestats-function"></a>JetComputeStats-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcomputestats-function"></a>JetComputeStats-Funktion

Die **JetComputeStats-Funktion** führt jeden Index einer Tabelle durch, um die Anzahl der Einträge in einem Index und die Anzahl der unterschiedlichen Schlüssel in einem Index genau zu berechnen. Diese Informationen werden zusammen mit der Anzahl der Datenbankseiten, die einem Index zugeordnet sind, und der aktuellen Berechnungszeit in Indexmetadaten in der Datenbank gespeichert. Diese Daten können anschließend mit Informationsvorgängen abgerufen werden.

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet wird. Beschreibt die Tabelle, für die Statistiken berechnet werden sollen.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRollbackError</p> | <p>Es ist ein Fehler aufgetreten, der erfordert, dass für diesen Vorgang ein Rollback aller Änderungen ausgeführt wird, aber beim Transaktionsrollback selbst ist ein Fehler aufgetreten.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg werden aktuelle Statistiken in den Datenbankkatalogen für die tabelle gespeichert, die mit dem angegebenen Cursor beschrieben wird.

Bei einem Fehler werden keineRlei Aktualisierungen an der Datenbank vorgenommen.

#### <a name="remarks"></a>Bemerkungen

Dieser Vorgang kann ressourcenintensiv sein, da jeder Index in einer Tabelle vollständig erläutert werden muss. [JetGetRecordPosition](./jetgetrecordposition-function.md) kann verwendet werden, um eine grobe Schätzung der Anzahl von Einträgen in einem Index zu erhalten, die Anzahl unterschiedlicher Werte in einem Index kann jedoch nicht allein geschätzt werden.

Die von diesem Vorgang berechneten Daten werden veraltet, und die Tabelle wird anschließend aktualisiert.

Aktualisierungen der von **JetComputeStats vorgenommenen** Datenbank erfolgen verzögert. Dies bedeutet, dass keine Protokolllöschung von diesem Vorgang begleitet wird und ein Systemabsturz nach einer Rückgabe von JET_errSuccess von **JetComputeStats** weiterhin dazu führen kann, dass diese Updates verloren gegangen sind.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SESID](./jet-sesid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetStopService](./jetstopservice-function.md)
