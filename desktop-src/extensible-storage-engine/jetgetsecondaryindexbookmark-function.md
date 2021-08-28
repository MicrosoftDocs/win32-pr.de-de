---
description: Weitere Informationen finden Sie unter JetGetSecondaryIndexBookmark-Funktion.
title: JetGetSecondaryIndexBookmark-Funktion
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0773842d7de7d576e9ccbcab2c62ec456912a89
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984823"
---
# <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark-Funktion

Die **JetGetSecondaryIndexBookmark-Funktion** ruft ein spezielles Lesezeichen für den sekundären Indexeintrag an der aktuellen Position eines Cursors ab. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mit [jetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)effizient wieder zum gleichen Indexeintrag zu positionieren. Dies ist besonders nützlich, wenn die Neupositionierung auf einem sekundären Index mit doppelten Schlüsseln oder mehreren Indexeinträgen für denselben Datensatz verwendet wird.

**Windows XP: JetGetSecondaryIndexBookmark** wird in xp Windows eingeführt.

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*pvSecondaryKey*

Der Ausgabepuffer, der den sekundären Schlüssel empfängt.

*cbSecondaryKeyMax*

Die maximale Größe des Ausgabepuffers für den sekundären Schlüssel in Bytes.

*keySecondaryKeyActual*

Empfängt die tatsächliche Größe des sekundären Schlüssels in Bytes.

Wenn dieser Parameter NULL ist, wird die tatsächliche Größe des sekundären Schlüssels nicht zurückgegeben.

Wenn der Ausgabepuffer zu klein ist, wird weiterhin die tatsächliche Größe des sekundären Schlüssels zurückgegeben. Das bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.

*pvPrimaryBookmark*

Der Ausgabepuffer, der das Primärschlüssel-Lesezeichen empfängt.

*cbPrimaryBookmarkMax*

Die maximale Größe des Ausgabepuffers für das Primärschlüssel-Lesezeichen in Bytes.

*keyPrimaryKeyActual*

Empfängt die tatsächliche Größe des Primärschlüssel-Lesezeichens in Bytes.

Wenn dieser Parameter NULL ist, wird die tatsächliche Größe des Primärschlüssel-Lesezeichens nicht zurückgegeben.

Wenn der Ausgabepuffer zu klein ist, wird die tatsächliche Größe des Primärschlüssel-Lesezeichens weiterhin zurückgegeben. Das bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.

*grbit*

Für die zukünftige Verwendung reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen, aber einer der Ausgabepuffer war zu klein, um die angeforderten Daten zu empfangen.</p><p>Der Ausgabepuffer wurde mit so viel Lesezeichen gefüllt, wie es passen würde. Die tatsächliche Größe des Lesezeichens wurde auch zurückgegeben, wenn dies angefordert wird.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Der Cursor befindet sich derzeit nicht in einem sekundären Index.</p><p>Es ist nicht sinnvoll, ein sekundäres Indexzeichen abzurufen, wenn der Cursor derzeit keinen sekundären Index verwendet. <a href="gg269221(v=exchg.10).md">JetGetBookmark sollte</a> verwendet werden, wenn sich der Cursor nicht auf einem sekundären Index befindet.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor ist nicht auf einem Datensatz positioniert.</p><p>Dafür sind viele verschiedene Gründe möglich. Dies geschieht beispielsweise, wenn der Cursor derzeit nach dem letzten Datensatz im aktuellen Index positioniert ist.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird das sekundäre Indexzeichen für den Indexeintrag an der aktuellen Position eines Cursors in den Ausgabepuffern zurückgegeben. Es erfolgt keine Änderung des Datenbankstatus.

Bei einem Fehler sind der Status der Ausgabepuffer und die tatsächliche Größe des sekundären Indexzeichens nicht definiert, es sei denn, JET_errBufferTooSmall zurückgegeben wurde. Wenn JET_errBufferTooSmall zurückgegeben wird, enthalten die Ausgabepuffer so viel sekundäres Index-Lesezeichen wie in den bereitgestellten Platz, und die tatsächliche Größe des sekundären Index-Lesezeichens ist genau. In jedem Fall erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Bemerkungen

Lesezeichen sollten in der Regel als nicht transparente Datenbrocken behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Die folgenden Eigenschaften können jedoch für alle ESENT-Lesezeichen bekannt sein:

  - Ein Lesezeichen identifiziert einen Datensatz in einer bestimmten Tabelle eindeutig.

  - Das Lesezeichen eines Datensatzes ändert sich während der Lebensdauer dieses Datensatzes nicht.

  - Das Lesezeichen eines Datensatzes ist mit dem Schlüssel dieses Datensatzes auf dem primären Index für die Tabelle identisch, die diesen Datensatz enthält. Wenn kein primärer Index für diese Tabelle definiert ist, erstellt die Datenbank-Engine ein eigenes Lesezeichen für den Datensatz.

  - Lesezeichen können mithilfe von [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) miteinander verglichen werden, um ihre relative Reihenfolge im primären Index über die Tabelle der Quelldatensätze zu erstellen. Wenn kein primärer Index für diese Tabelle definiert ist, ist die relative Reihenfolge der Lesezeichen aus dieser Tabelle nicht sinnvoll.

  - Es ist bedeutungslos, Lesezeichen von Datensätzen aus verschiedenen Tabellen miteinander zu vergleichen.

  - Ein Lesezeichen ist immer kleiner oder gleich JET_cbBookmarkMost (256) Bytes länge vor Windows Vista. In Windows Vista und höheren Versionen können Lesezeichen größer sein. Die maximale Größe eines Lesezeichens entspricht dem aktuellen Wert von JET_paramKeyMost + 1.

Schlüssel sollten in der Regel als nicht transparente Datenbrocken behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Die folgenden Eigenschaften können jedoch für alle ESENT-Schlüssel bekannt sein:

  - Schlüssel können mithilfe von [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) miteinander verglichen werden, um ihre relative Reihenfolge im ursprünglichen Index über der Tabelle der Quellindexeinträge zu erstellen.

  - Es ist bedeutungslos, Schlüssel von Indexeinträgen aus verschiedenen Indizes miteinander zu vergleichen.

  - Ein Schlüssel ist vor der JET_cbKeyMost Vista immer kleiner Windows oder gleich JET_cbKeyMost (255) Bytes. In Windows Vista und höheren Versionen können die Schlüssel größer sein. Die maximale Größe eines Schlüssels entspricht dem aktuellen Wert JET_paramKeyMost.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)  
[JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
