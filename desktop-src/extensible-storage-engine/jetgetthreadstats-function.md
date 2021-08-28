---
description: Weitere Informationen finden Sie unter JetGetThreadStats-Funktion.
title: JetGetThreadStats-Funktion
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 87f3bed1dcd9fd43a67c96cbcb53d2496a976afa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474086"
---
# <a name="jetgetthreadstats-function"></a>JetGetThreadStats-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetthreadstats-function"></a>JetGetThreadStats-Funktion

Die **JetGetThreadStats-Funktion** ruft Leistungsinformationen aus der Datenbank-Engine für den aktuellen Thread ab. Es können mehrere Aufrufe verwendet werden, um Statistiken zu sammeln, die die Aktivität der Datenbank-Engine in diesem Thread zwischen diesen Aufrufen widerspiegeln.

**Windows Vista:****JetGetThreadStats** wird in Windows Vista eingeführt.  

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parameter

*pvResult*

Der Ausgabepuffer, der die Threadstatistikdaten empfängt. Der Puffer enthält eine [JET_THREADSTATS](./jet-threadstats-structure.md) nach einem erfolgreichen Aufruf.

*cbMax*

Die maximale Größe des Ausgabepuffers in Bytes.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Fehler beim Vorgang, weil der bereitgestellte Ausgabepuffer zu klein war, um die angeforderten Daten zu enthalten. Die <strong>JetGetThreadStats-Funktion</strong> gibt diesen Fehler zurück, wenn der Ausgabepuffer zu klein ist, um die kleinste Version der <a href="gg269227(v=exchg.10).md">JET_THREADSTATS-Struktur</a> zu enthalten, die von der Datenbank-Engine unterstützt wird.</p> | 



Bei Erfolg enthält der Ausgabepuffer eine JET_THREADSTATS Struktur, die Datenbank-Engine-Statistiken für den aktuellen Thread enthält. [](./jet-threadstats-structure.md)

Bei einem Fehler ist der Status des Ausgabepuffers nicht definiert.

#### <a name="remarks"></a>Hinweise

Die informationen, die von zwei aufeinander folgenden Aufrufen dieser API bereitgestellt werden, sollen verwendet werden, um die Kosten anderer Datenbank-Engine-Vorgänge für den aktuellen Thread zu berechnen. Im Allgemeinen erfolgt dies, indem ein vor und nach dem Lesen der Statistiken verwendet und die Nachzählung von der Anzahl der Vorher-Vorgänge subtrahiert wird, um die Nettoanzahl der ausgeführten Vorgänge zu erhalten.

Beispielsweise könnte eine Anwendung **JetGetThreadStats** einmal aufrufen, um ein erstes Lesen der Statistiken für den aktuellen Thread zu erhalten. Anschließend könnte die [JetMove-Funktion](./jetmove-function.md) mit dem *cRow-Parameter* auf JET_MoveNext, um zum nächsten Indexeintrag in einem Index zu wechseln. Anschließend könnte **JetGetThreadStats erneut aufgerufen werden,** um einen weiteren Lesedatenaufruf für die Statistiken des Threads zu erhalten. Anschließend könnte der cPageReferenced-Zähler vom zweiten Lese-Wert des ersten Werts subtrahiert werden. Das Ergebnis wäre die Anzahl der Datenbankseiten, auf die die Datenbank-Engine verweist, um den [JetMove-Vorgang](./jetmove-function.md) durchzuführen.

Die Statistiken für jeden Thread werden für die Lebensdauer dieses Threads akkumuliert. Die Statistiken werden zurückgesetzt, wenn die DLL der Datenbank-Engine aus dem Hostprozess entladen wird.

Die [JET_THREADSTATS](./jet-threadstats-structure.md) struktur wird in Zukunft wahrscheinlich erweitert, um weitere Statistiken zu enthalten. Neue Statistiken werden am Ende der Struktur hinzugefügt und können mit einer erhöhten Ausgabepuffergröße abgerufen werden. Das Vorhandensein zusätzlicher Statistiken kann durch einen größeren cbStruct-Wert abgeleitet werden.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_THREADSTATS](./jet-threadstats-structure.md)  
[JetMove](./jetmove-function.md)
