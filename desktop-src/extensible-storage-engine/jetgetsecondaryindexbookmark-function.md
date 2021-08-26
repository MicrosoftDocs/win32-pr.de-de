---
description: 'Weitere Informationen zu: JetGetSecondaryIndexBookmark-Funktion'
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
ms.openlocfilehash: 3a27d34b2622c5fe4ce2c72e3781394457e9cc20
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472521"
---
# <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark-Funktion

Die **JetGetSecondaryIndexBookmark-Funktion** ruft ein spezielles Lesezeichen für den sekundären Indexeintrag an der aktuellen Position eines Cursors ab. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mit [jetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)effizient wieder auf denselben Indexeintrag zu positionieren. Dies ist besonders nützlich bei der Neupositionierung in einem sekundären Index, der doppelte Schlüssel oder mehrere Indexeinträge für denselben Datensatz enthält.

**Windows XP: JetGetSecondaryIndexBookmark** wurde in Windows XP eingeführt.

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

*pwSecondaryKeyActual*

Empfängt die tatsächliche Größe des sekundären Schlüssels in Bytes.

Wenn dieser Parameter NULL ist, wird die tatsächliche Größe des sekundären Schlüssels nicht zurückgegeben.

Wenn der Ausgabepuffer zu klein ist, wird die tatsächliche Größe des sekundären Schlüssels weiterhin zurückgegeben. Dies bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.

*pvPrimaryBookmark*

Der Ausgabepuffer, der das Primärschlüssellesezeichen empfängt.

*cbPrimaryBookmarkMax*

Die maximale Größe des Ausgabepuffers für das Primärschlüssellesezeichen in Bytes.

*sidePrimaryKeyActual*

Empfängt die tatsächliche Größe des Primärschlüssellesezeichens in Bytes.

Wenn dieser Parameter NULL ist, wird die tatsächliche Größe des Primärschlüssellesezeichens nicht zurückgegeben.

Wenn der Ausgabepuffer zu klein ist, wird die tatsächliche Größe des Primärschlüssellesezeichens weiterhin zurückgegeben. Dies bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.

*grbit*

Für die zukünftige Verwendung reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen, aber einer der Ausgabepuffer war zu klein, um die angeforderten Daten zu empfangen.</p><p>Der Ausgabepuffer wurde mit so viel Lesezeichen gefüllt, wie es passt. Die tatsächliche Größe des Lesezeichens wurde ebenfalls zurückgegeben, falls angefordert.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Der Cursor befindet sich derzeit nicht in einem sekundären Index.</p><p>Es ist nicht sinnvoll, ein sekundäres Indexlesezeichen abzurufen, wenn der Cursor derzeit keinen sekundären Index verwendet. <a href="gg269221(v=exchg.10).md">JetGetBookmark</a> sollte verwendet werden, wenn sich der Cursor nicht in einem sekundären Index befindet.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor wird nicht in einem Datensatz positioniert.</p><p>Dafür sind viele verschiedene Gründe möglich. Dies geschieht beispielsweise, wenn der Cursor derzeit nach dem letzten Datensatz im aktuellen Index positioniert ist.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird das sekundäre Indexlesezeichen für den Indexeintrag an der aktuellen Position eines Cursors in den Ausgabepuffern zurückgegeben. Es wird keine Änderung am Datenbankzustand vorgenommen.

Bei einem Fehler sind der Status der Ausgabepuffer und die tatsächliche Größe des sekundären Indexlesezeichens nicht definiert, es sei denn, JET_errBufferTooSmall wurde zurückgegeben. Wenn JET_errBufferTooSmall zurückgegeben wird, enthalten die Ausgabepuffer so viel des sekundären Indexlesezeichens, wie es in den bereitgestellten Bereich passt, und die tatsächliche Größe des sekundären Indexlesezeichens ist genau. In jedem Fall erfolgt keine Änderung des Datenbankzustands.

#### <a name="remarks"></a>Hinweise

Lesezeichen sollten im Allgemeinen als nicht transparente Datenblöcke behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Die folgenden Eigenschaften können jedoch über alle ESENT-Lesezeichen bekannt sein:

  - Ein Lesezeichen identifiziert einen Datensatz in einer bestimmten Tabelle eindeutig.

  - Das Lesezeichen eines Datensatzes ändert sich während der Lebensdauer dieses Datensatzes nicht.

  - Das Lesezeichen eines Datensatzes entspricht dem Schlüssel dieses Datensatzes im primären Index für die Tabelle, die diesen Datensatz enthält. Wenn für diese Tabelle kein primärer Index definiert ist, erstellt die Datenbank-Engine ein eigenes Lesezeichen für den Datensatz.

  - Lesezeichen können miteinander verglichen werden, indem [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) verwendet wird, um ihre relative Reihenfolge im primären Index für die Tabelle der Quelldatensätze festzulegen. Wenn für diese Tabelle kein primärer Index definiert ist, ist die relative Reihenfolge der Lesezeichen aus dieser Tabelle nicht sinnvoll.

  - Es ist bedeutungslos, Lesezeichen von Datensätzen aus verschiedenen Tabellen miteinander zu vergleichen.

  - Ein Lesezeichen ist vor Windows Vista immer kleiner oder gleich JET_cbBookmarkMost (256) Bytes. In Windows Vista und höheren Versionen können Lesezeichen größer sein. Die maximale Größe eines Lesezeichens entspricht dem aktuellen Wert von JET_paramKeyMost + 1.

Schlüssel sollten im Allgemeinen als nicht transparente Datenblöcke behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Die folgenden Eigenschaften können jedoch über alle ESENT-Schlüssel bekannt sein:

  - Schlüssel können miteinander verglichen werden, indem [sie memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) verwenden, um ihre relative Reihenfolge im ursprünglichen Index über der Tabelle der Quellindexeinträge herzustellen.

  - Es ist bedeutungslos, Schlüssel von Indexeinträgen aus verschiedenen Indizes miteinander zu vergleichen.

  - Ein Schlüssel ist vor Windows Vista immer kleiner oder gleich JET_cbKeyMost (255) Bytes. Bei Windows Vista und höheren Versionen können die Schlüssel größer sein. Die maximale Größe eines Schlüssels entspricht dem aktuellen Wert von JET_paramKeyMost.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)  
[JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
