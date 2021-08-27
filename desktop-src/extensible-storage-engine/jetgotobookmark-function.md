---
description: 'Weitere Informationen zu: JetGotoBookmark-Funktion'
title: JetGotoBookmark-Funktion
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54a6370badcdd83e1beed4cc50f42a52eab797ba
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984643"
---
# <a name="jetgotobookmark-function"></a>JetGotoBookmark-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgotobookmark-function"></a>JetGotoBookmark-Funktion

Die **JetGotoBookmark-Funktion** positioniert einen Cursor an einem Indexeintrag für den Datensatz, der dem angegebenen Lesezeichen zugeordnet ist. Das Lesezeichen kann mit einem beliebigen Index verwendet werden, der für eine Tabelle definiert ist. Das Lesezeichen für einen Datensatz kann mit [JetGetBookmark](./jetgetbookmark-function.md)abgerufen werden.

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*pvBookmark*

Der Puffer, der das Lesezeichen enthält, das zum Positionieren des Cursors verwendet werden soll.

*cbBookmark*

Die Größe des Lesezeichens im Puffer.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>beendet wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>   Dieser Rückgabewert wurde in Windows XP eingeführt.</p> | 
| <p>JET_errInvalidBookmark</p> | <p>Das bereitgestellte Lesezeichen ist ungültig. Dies ist möglicherweise aufgetreten, weil die Größe des Lesezeichens 0 (null) oder der Lesezeichenpufferzeiger <strong>NULL</strong>ist.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor befindet sich in einem sekundären Index, und für den Datensatz, der dem Lesezeichen zugeordnet ist, konnte kein Indexeintrag gefunden werden.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Der Datensatz, der dem Lesezeichen zugeordnet ist, wurde nicht gefunden.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p><strong>Windows XP:</strong>   Dieser Rückgabewert wurde in Windows XP eingeführt.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, wird der Cursor an einem Indexeintrag für den Datensatz positioniert, der dem angegebenen Lesezeichen zugeordnet ist. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist, wird dieser Indexbereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird dieser Suchschlüssel gelöscht. Es wird keine Änderung am Datenbankzustand vorgenommen.

Wenn diese Funktion fehlschlägt, bleibt die Position des Cursors unverändert. Wenn ein Datensatz für das Update vorbereitet wurde, wird dieses Update abgebrochen. Wenn ein Indexbereich in Kraft ist, wird dieser Indexbereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird dieser Suchschlüssel gelöscht. Es wird keine Änderung am Datenbankzustand vorgenommen.

#### <a name="remarks"></a>Bemerkungen

Es gibt zwei Möglichkeiten, ein Lesezeichen zu verwenden, um einen Cursor auf einem Index zu positionieren. Die erste besteht darin, das Lesezeichen zu verwenden, um direkt auf dem Datensatz zu positionieren. Dies tritt auf, wenn der aktuelle Index des Cursors der primäre Index ist. Diese Technik funktioniert, da ein ESENT-Lesezeichen mit dem Primärschlüssel des zugeordneten Datensatzes identisch ist.

Die zweite Möglichkeit zur Verwendung eines Lesezeichens besteht darin, es in einem Eintrag in einem sekundären Index zu positionieren, der dem Datensatz entspricht, der diesem Lesezeichen zugeordnet ist. Während dieses Vorgangs sucht die Engine den tatsächlichen Datensatz mithilfe des Lesezeichens für den primären Index. Anschließend werden die Datensatzdaten und die sekundäre Indexdefinition verwendet, um einen Schlüssel in den sekundären Index zu berechnen, der auf den Datensatz verweist. Anschließend positioniert er den Cursor auf dem Indexeintrag für diesen Schlüssel. Wenn sich der Cursor derzeit in einem sekundären Index für eine oder mehrere mehrwertige Schlüsselspalten befindet, wird der Cursor auf dem Indexeintrag positioniert, der dem ersten Mehrwert jeder dieser Schlüsselspalten entspricht.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)
