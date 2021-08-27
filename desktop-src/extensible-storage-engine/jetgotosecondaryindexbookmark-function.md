---
description: 'Weitere Informationen zu: JetGotoSecondaryIndexBookmark-Funktion'
title: JetGotoSecondaryIndexBookmark-Funktion
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84f9b90d617c11e3e304aa375e25a96b446114da
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984582"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark-Funktion

Die **JetGotoSecondaryIndexBookmark-Funktion** positioniert einen Cursor in einem Indexeintrag, der dem angegebenen sekundären Indexlesezeichen zugeordnet ist. Das sekundäre Indexlesezeichen muss mit demselben Index für dieselbe Tabelle verwendet werden, aus der es ursprünglich abgerufen wurde. Das sekundäre Indexlesezeichen für einen Indexeintrag kann mit **JetGotoSecondaryIndexBookmark** abgerufen werden.

**Windows XP:****JetGotoSecondaryIndexBookmark** wurde in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*pvSecondaryKey*

Der Puffer, der den sekundären Schlüssel enthält, der zum Positionieren des Cursors verwendet werden soll.

*cbSecondaryKey*

Die Größe des sekundären Schlüssels im Puffer.

*pvPrimaryBookmark*

Der Puffer, der das Primärschlüssellesezeichen enthält, das zum Positionieren des Cursors verwendet werden soll.

*cbPrimaryBookmark*

Die Größe des Primärschlüssellesezeichens im Puffer.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitBookmarkPermitVirtualCurrency</p> | <p>Wenn der Indexeintrag nicht mehr gefunden werden kann, wird der Cursor an der Stelle positioniert, an der dieser Indexeintrag zuvor gefunden wurde. Der Vorgang schlägt weiterhin mit JET_errRecordDeleted fehl. Es ist jedoch möglich, relativ zum Indexeintrag, der jetzt fehlt, zum nächsten oder vorherigen Indexeintrag zu wechseln.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>beendet wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 
| <p>JET_errInvalidBookmark</p> | <p>Das sekundäre Indexlesezeichen, das bereitgestellt wurde, war ungültig. Dieser Fehler ist möglicherweise aufgetreten, weil der sekundäre Schlüssel 0 (null) oder der sekundäre Schlüsselpufferzeiger <strong>NULL</strong>ist. Dieser Fehler tritt auf, weil</p><ul><li><p>Der aktuelle sekundäre Index verfügt nicht über eine Eindeutigkeitseinschränkung, und die Größe des bereitgestellten Lesezeichens ist 0 (null).</p></li><li><p>Der Lesezeichenpufferzeiger ist <strong>NULL.</strong></p></li></ul> | 
| <p>JET_errNoCurrentIndex</p> | <p>Der Cursor befindet sich derzeit nicht in einem sekundären Index. Es ist nicht sinnvoll, zu einem sekundären Indexlesezeichen zu wechseln, wenn der Cursor derzeit keinen sekundären Index verwendet. <a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> sollte verwendet werden, wenn sich der Cursor nicht in einem sekundären Index befindet.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Der Indexeintrag, der dem sekundären Indexlesezeichen zugeordnet ist, wurde nicht gefunden.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, wird der Cursor an einem Indexeintrag positioniert, der dem angegebenen sekundären Indexlesezeichen zugeordnet ist. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist, wird dieser Indexbereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, der verwendet werden soll, wird dieser Suchschlüssel gelöscht. Es wird keine Änderung am Datenbankzustand vorgenommen.

Wenn diese Funktion fehlschlägt, bleibt die Position des Cursors unverändert, es sei denn, JET_errRecordDeleted wird zurückgegeben und JET_bitBookmarkPermitVirtualCurrency angegeben. In diesem Fall wird der Cursor an der Stelle positioniert, an der sich der Indexeintrag befindet, der dem angegebenen sekundären Indexlesezeichen zugeordnet ist. Der Cursor kann relativ zu dieser Position verschoben werden, befindet sich jedoch immer noch nicht in einem gültigen Indexeintrag.

Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist, wird dieser Indexbereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, der verwendet werden soll, wird dieser Suchschlüssel gelöscht. In jedem Fall erfolgt keine Änderung des Datenbankzustands.

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
[JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)
