---
description: 'Weitere Informationen finden Sie unter: JET_THREADSTATS Struktur'
title: JET_THREADSTATS Struktur
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9dcf88afc4b0f01a1691f9fb287491e9adfe71521e394a0e6b278c556fb5741f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832860"
---
# <a name="jet_threadstats-structure"></a>JET_THREADSTATS Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_threadstats-structure"></a>JET_THREADSTATS Struktur

Die **JET_THREADSTATS-Struktur** enthält kumulative Statistiken zur Arbeit, die von der Datenbank-Engine im aktuellen Thread ausgeführt wird. Diese Informationen werden über [JetGetThreadStats zurückgegeben.](./jetgetthreadstats-function.md)

**Windows Vista:**  Die **JET_THREADSTATS-Struktur** wird in Windows Vista eingeführt.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der zurückgegebenen **JET_THREADSTATS-Struktur** in Bytes.

**Hinweis:**  Die **JET_THREADSTATS-Struktur** wird in Zukunft erweitert, um weitere Statistiken zu enthalten. Neue Statistiken werden am Ende der Struktur hinzugefügt und können mit einer erhöhten Ausgabepuffergröße abgerufen werden. Das Vorhandensein zusätzlicher Statistiken kann durch einen größeren **cbStruct-Wert abgeleitet** werden.

**cPageReferenced**

Die Gesamtanzahl der Datenbankseiten, die von der Datenbank-Engine im aktuellen Thread besucht werden.

**cPageRead**

Die Gesamtanzahl der Datenbankseiten, die von der Datenbank-Engine im aktuellen Thread vom Datenträger abgerufen wurden.

**cPagePreread**

Die Gesamtanzahl der Datenbankseiten, die von der Datenbank-Engine im aktuellen Thread vorab vom Datenträger abgerufen wurden.

**cPageDirtied**

Die Gesamtanzahl der Datenbankseiten ohne ungeschriebene Änderungen, die von der Datenbank-Engine im aktuellen Thread geändert wurden.

**cPageRedirtied**

Die Gesamtanzahl der Datenbankseiten mit nicht geschriebenen Änderungen, die von der Datenbank-Engine im aktuellen Thread geändert wurden.

**cLogRecord**

Die Gesamtanzahl der Transaktionsprotokolldatensätze, die von der Datenbank-Engine im aktuellen Thread generiert wurden.

**cbLogRecord**

Die Gesamtgröße von Transaktionsprotokolldatensätzen in Bytes, die von der Datenbank-Engine im aktuellen Thread generiert wurden.

### <a name="requirements"></a>Anforderungen

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
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JetGetThreadStats](./jetgetthreadstats-function.md)
