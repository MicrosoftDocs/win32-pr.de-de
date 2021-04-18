---
description: 'Weitere Informationen: jetgetthreadstats-Funktion'
title: Jetgetthreadstats-Funktion
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
ms.openlocfilehash: 85d45021910f818f297cd0bc9829580a18b7a296
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344032"
---
# <a name="jetgetthreadstats-function"></a>Jetgetthreadstats-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetthreadstats-function"></a>Jetgetthreadstats-Funktion

Die **jetgetthreadstats** -Funktion ruft Leistungsinformationen aus der Datenbank-Engine für den aktuellen Thread ab. Mehrere Aufrufe können verwendet werden, um Statistiken zu sammeln, die die Aktivität der Datenbank-Engine in diesem Thread zwischen diesen Aufrufen widerspiegeln.

**Windows Vista:**  **jetgetthreadstats** wird in Windows Vista eingeführt.

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parameter

*pvresult*

Der Ausgabepuffer, der die Thread Statistikdaten empfängt. Der Puffer enthält eine [JET_THREADSTATS](./jet-threadstats-structure.md) Struktur nach einem erfolgreichen-Rückruf.

*cbmax*

Die maximale Größe des Ausgabepuffers in Bytes.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da der angegebene Ausgabepuffer zu klein war, um die angeforderten Daten zu enthalten. Die <strong>jetgetthreadstats</strong> -Funktion gibt diesen Fehler zurück, wenn der Ausgabepuffer zu klein ist, um die kleinste Version der <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> Struktur zu enthalten, die von der Datenbank-Engine unterstützt wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg enthält der Ausgabepuffer eine [JET_THREADSTATS](./jet-threadstats-structure.md) Struktur, die Datenbank-Engine-Statistiken für den aktuellen Thread enthält.

Bei einem Fehler ist der Status des Ausgabepuffers nicht definiert.

#### <a name="remarks"></a>Bemerkungen

Die Informationen, die von zwei aufeinander folgenden Aufrufen dieser API bereitgestellt werden, sollen verwendet werden, um die Kosten anderer Datenbankmodul Vorgänge im aktuellen Thread zu berechnen. Im Allgemeinen wird dies erreicht, indem ein vor und nach dem Lesen der Statistiken durchgeführt wird und die nach Anzahl von der vorher-Anzahl subtrahieren, um die Netto Anzahl der ausgeführten Vorgänge zu erhalten.

Beispielsweise könnte eine Anwendung **jetgetthreadstats** einmal aufrufen, um das erste Lesen der Statistiken für den aktuellen Thread zu erhalten. Anschließend kann die [jetmove](./jetmove-function.md) -Funktion aufgerufen werden, wobei der " *cRow* "-Parameter auf JET_MoveNext festgelegt ist, um zum nächsten Index Eintrag eines Indexes zu wechseln. Anschließend kann **jetgetthreadstats** erneut aufgerufen werden, um ein weiteres lesen der Thread Statistik zu erhalten. Der cpagereferenzierte-Counter kann dann vom zweiten Lesevorgang aus dem ersten gelesen werden. Das Ergebnis ist die Anzahl der Datenbankseiten, auf die von der Datenbank-Engine verwiesen wird, um den [jetmove](./jetmove-function.md) -Vorgang auszuführen.

Die Statistiken für jeden Thread werden für die Lebensdauer dieses Threads akkumuliert. Die Statistiken werden zurückgesetzt, wenn die dll der Datenbank-Engine aus dem Host Prozess entladen wird.

Die [JET_THREADSTATS](./jet-threadstats-structure.md) Struktur wird in Zukunft wahrscheinlich erweitert, um mehr Statistiken zu enthalten. Neue Statistiken werden am Ende der Struktur hinzugefügt und können mit einer erweiterten Ausgabepuffergröße abgerufen werden. Das vorhanden sein zusätzlicher Statistiken kann durch einen größeren cbStruct-Wert abgeleitet werden.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_THREADSTATS](./jet-threadstats-structure.md)  
[Jetmove](./jetmove-function.md)
