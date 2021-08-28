---
description: Weitere Informationen finden Sie unter JetIndexRecordCount-Funktion.
title: JetIndexRecordCount-Funktion
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
ms.openlocfilehash: 4105dec0217c1fea2e00d92c9d217fcf2d7e40b4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480436"
---
# <a name="jetindexrecordcount-function"></a>JetIndexRecordCount-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetindexrecordcount-function"></a>JetIndexRecordCount-Funktion

Die **JetIndexRecordCount-Funktion** zählt die Anzahl der Einträge im aktuellen Index von der aktuellen Position nach vorn. Die aktuelle Position ist in der Anzahl enthalten. Die Anzahl kann größer als die Gesamtzahl der Datensätze in der Tabelle sein, wenn sich der aktuelle Index über einer mehrwertigen Spalte befindet und Instanzen der Spalte mehrere Werte haben. Wenn die Tabelle leer ist, wird 0 für die Anzahl zurückgegeben.

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*pcrec*

Der Zeiger auf einen long-Wert ohne Vorzeichen, um die Anzahl zu empfangen.

*crecMax*

Die maximale Anzahl der zu zählenden Datensätze. Der *crecMax-Wert* 0 gibt an, dass die Anzahl unbegrenzt ist.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die -Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in xp Windows eingeführt.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor befindet sich derzeit nicht in einem Datensatz, und die Tabelle ist nicht leer.</p><p><strong>Windows XP, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:</strong>  Wenn der Cursor auf einem leeren Index oder Indexbereich positioniert ist, gibt <strong>JetIndexRecordCount</strong> fälschlicherweise JET_errNoCurrentRecord.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in xp Windows eingeführt.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 



Wenn diese Funktion erfolgreich ist, wird die genaue Anzahl von Indexeinträgen einschließlich der aktuellen Position und bis *zu crecMax* (wenn sie nicht 0 ist) in der unsigned long zurückgegeben, auf die *pcrec* zeigt.

Wenn bei dieser Funktion ein Fehler auftritt, werden keine Änderungen am Arbeitsspeicher vorgenommen, der vor *dem Zeitpunkt zugeordnet wurde.*

#### <a name="remarks"></a>Hinweise

Wenn die Tabelle nicht leer ist, sollte der Cursor auf dem Datensatz positioniert werden, ab dem die Anzahl beginnen soll. Die Anzahl enthält diesen Datensatz und die Anzahl bis zum angegebenen Grenzwert in *crecMax.* Wenn *crecMax* 0 ist, wird der Vorgang bis zum Ende des Indexes fortgesetzt.

Indexbereiche können verwendet werden, um künstliche End-of-Index-Einschränkungen für die Anzahl zu erstellen. Auf diese Weise können Unterbereiche eines Indexes genau gezählt werden. Der Cursor sollte an der ersten Zeile im Bereich positioniert werden. Das Ende des Bereichsschlüssels sollte festgelegt werden, und [dann sollte JetSetIndexRange](./jetsetindexrange-function.md) zum Festlegen des oberen Bereichs verwendet werden, entweder ausschließlich oder ausschließlich. Schließlich sollte **JetIndexRecordCount** aufgerufen werden, um den Bereich genau zu zählen.

**JetIndexRecordCount** folgt der Transaktionssemantik und gibt eine Anzahl zurück, die für diese bestimmte Sitzung im aktuellen Transaktionszustand genau ist.

**JetIndexRecordCount greifen** auf Indexblattseiten zu, um Einträge genau zu zählen. Daher kann es sehr viele E/A-Aktionen und langsame E/A-Aktionen geben. Die *crecMax-Einschränkung* sollte verwendet werden, um übermäßige Last zu verhindern. Wenn ein Bereich groß ist, kann es möglich sein, den Bereich mit [jetGetRecordPosition](./jetgetrecordposition-function.md)auf ungefähre Weise zu zählen.

**Windows XP, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:**  Wenn der Cursor auf einem leeren Index oder Indexbereich positioniert ist, gibt **JetIndexRecordCount** fälschlicherweise JET_errNoCurrentRecord zurück, anstatt eine Datensatzanzahl von 0 (null) zurückgibt. Die Anwendung sollte überprüfen, ob der Index oder Indexbereich in diesem Fall leer ist.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
