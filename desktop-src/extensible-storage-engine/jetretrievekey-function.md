---
description: Weitere Informationen finden Sie unter JetRetrikey-Funktion.
title: JetRetrieveKey-Funktion
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 65925ce2425dcf717b7db94f5b83ca48a68c8f31
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466219"
---
# <a name="jetretrievekey-function"></a>JetRetrieveKey-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetretrievekey-function"></a>JetRetrieveKey-Funktion

Die **JetRetrikey-Funktion** ruft den Schlüssel für den Indexeintrag an der aktuellen Position eines Cursors ab. Solche Schlüssel werden durch Aufrufe von [JetMakeKey erstellt.](./jetmakekey-function.md) Der abgerufene Schlüssel kann dann verwendet werden, um diesen Cursor durch einen Aufruf von JetSeek effizient an denselben [Indexeintrag zurück zu geben.](./jetseek-function.md)

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*pvData*

Der Ausgabepuffer, der den Schlüssel erhält.

*cbMax*

Die maximale Größe des Ausgabepuffers in Bytes.

*–actual*

Empfängt die tatsächliche Größe des Schlüssels in Bytes.

Wenn dieser Parameter NULL ist, wird die tatsächliche Größe des Schlüssels nicht zurückgegeben.

Wenn der Ausgabepuffer zu klein ist, wird weiterhin die tatsächliche Größe des Schlüssels zurückgegeben. Das bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Wenn angegeben, gibt die Engine den Suchschlüssel für den Cursor zurück. Der Suchschlüssel wird mit mindestens einem vorherigen Aufruf von <a href="gg269329(v=exchg.10).md">JetMakeKey</a> erstellt, um mit <a href="gg294103(v=exchg.10).md">JetSeek</a> nach diesem Schlüssel zu suchen oder einen Indexbereich mit <a href="gg294112(v=exchg.10).md">JetSetIndexRange zu festlegen.</a></p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Es gibt keinen aktuellen Suchschlüssel für den Cursor. Dies geschieht für <strong>JetRetrikey,</strong> wenn JET_bitRetrieveCopy angegeben ist und kein Suchschlüssel für diesen Cursor erstellt wurde, indem ein vorheriger Aufruf von <a href="gg269329(v=exchg.10).md">JetMakeKey verwendet wird.</a> Der Suchschlüssel wird durch einen vorherigen Aufruf einer Navigations-API auf dem Cursor gelöscht, die nicht <a href="gg294117(v=exchg.10).md">JetMove ist.</a></p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor ist nicht auf einem Datensatz positioniert. Dafür sind viele verschiedene Gründe möglich. Dies geschieht beispielsweise, wenn der Cursor derzeit nach dem letzten Datensatz im aktuellen Index positioniert ist.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um den gesamten Schlüssel zu empfangen. Der Ausgabepuffer wurde mit einem so großen Teil des Schlüssels gefüllt, wie er passt. Bei Bedarf wurde auch die tatsächliche Größe des Schlüssels zurückgegeben.</p><p><strong>Hinweis:</strong>   Dieser Fehler wird nicht zurückgegeben, wenn JET_bitRetrieveCopy angegeben wird. Weitere Informationen finden Sie im Abschnitt "Hinweise".</p> | 



Bei Erfolg wird der Schlüssel für den Indexeintrag an der aktuellen Position eines Cursors im Ausgabepuffer zurückgegeben. Wenn JET_wrnBufferTruncated zurückgegeben wird, enthält der Ausgabepuffer so viel Schlüssel wie in den bereitgestellten Speicherplatz passt, und die tatsächliche Größe des Schlüssels ist genau. Es erfolgt keine Änderung des Datenbankstatus.

Bei einem Fehler sind der Zustand des Ausgabepuffers und die tatsächliche Größe des Schlüssels nicht definiert. Es erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Hinweise

Schlüssel sollten in der Regel als nicht transparente Datenbrocken behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Die folgenden Eigenschaften können jedoch für alle ESENT-Schlüssel bekannt sein:

  - Schlüssel können mithilfe der [memcmp-Funktion](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) miteinander verglichen werden, um ihre relative Reihenfolge im ursprünglichen Index über die Tabelle der Quellindexeinträge zu erstellen.

  - Es ist bedeutungslos, Schlüssel von Indexeinträgen aus verschiedenen Indizes miteinander zu vergleichen.

  - Ein Schlüssel ist vor der JET_cbKeyMost Vista immer kleiner Windows oder gleich JET_cbKeyMost (255) Bytes. In Windows Vista und höheren Versionen können die Schlüssel größer sein. Die maximale Größe eines Schlüssels entspricht dem aktuellen Wert JET_paramKeyMost.

Zusätzlich zu den oben genannten Eigenschaften von ESENT-Schlüsseln im Allgemeinen ist es wichtig zu beachten, dass sich ein Suchschlüssel vom Schlüssel für einen Indexeintrag unterscheiden kann. Insbesondere kann ein Suchschlüssel länger als ein gewöhnlicher Schlüssel sein. Diese zusätzliche Länge tritt auf, wenn beim Erstellen des Suchschlüssels eine Platzhalteroption verwendet wird. Weitere Informationen finden Sie unter [JetMakeKey.](./jetmakekey-function.md)

Es gibt einen wichtigen Fehler in dieser API, der in allen Releases vorhanden ist. Wenn der Suchschlüssel mithilfe von JET_bitRetrieveCopy angefordert wird und der Ausgabepuffer zu klein ist, um den gesamten Schlüssel zu empfangen, JET_wrnBufferTruncated NICHT zurückgegeben. JET_errSuccess wird stattdessen zurückgegeben. Es ist wichtig zu überprüfen, ob die tatsächliche Größe des Schlüssels, wie er mithilfe von *"actual"* zurückgegeben wird, kleiner oder gleich der Größe des Ausgabepuffers ist. Wenn die tatsächliche Größe größer als die Größe des Ausgabepuffers ist, sollte der Aufrufer von **JetRetrikey** so reagieren, als ob JET_wrnBufferTruncated zurückgegeben würden.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
