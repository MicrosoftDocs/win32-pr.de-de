---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS Struktur'
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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368963"
---
# <a name="jet_threadstats-structure"></a>JET_THREADSTATS Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_threadstats-structure"></a>JET_THREADSTATS Struktur

Die **JET_THREADSTATS** Struktur enthält kumulative Statistiken für die Arbeit, die von der Datenbank-Engine auf dem aktuellen Thread ausgeführt wird. Diese Informationen werden über [jetgetthreadstats](./jetgetthreadstats-function.md)zurückgegeben.

**Windows Vista:**  Die **JET_THREADSTATS** Struktur wird in Windows Vista eingeführt.

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

Die Größe der zurückgegebenen **JET_THREADSTATS** Struktur in Bytes.

**Hinweis**  Die **JET_THREADSTATS** Struktur wird in Zukunft erweitert, um mehr Statistiken zu enthalten. Neue Statistiken werden am Ende der Struktur hinzugefügt und können mit einer erweiterten Ausgabepuffergröße abgerufen werden. Das vorhanden sein zusätzlicher Statistiken kann durch einen größeren **cbStruct** -Wert abgeleitet werden.

**cpagereferenziert**

Die Gesamtanzahl der Datenbankseiten, die von der Datenbank-Engine im aktuellen Thread besucht wurden.

**cpageread**

Die Gesamtanzahl der Datenbankseiten, die von der Datenbank-Engine auf dem aktuellen Thread von der Festplatte abgerufen wurden.

**cpagepreread**

Die Gesamtanzahl der Datenbankseiten, die von der Datenbank-Engine im aktuellen Thread vorab von der Festplatte abgerufen wurden.

**cpagedirtied**

Die Gesamtanzahl der Datenbankseiten ohne Änderungen, die von der Datenbank-Engine im aktuellen Thread geändert wurden.

**cPageRedirtied**

Die Gesamtanzahl der Datenbankseiten, bei denen Änderungen vorgenommen wurden, die von der Datenbank-Engine im aktuellen Thread geändert wurden.

**clogrecord**

Die Gesamtanzahl der Transaktionsprotokoll-Datensätze, die von der Datenbank-Engine im aktuellen Thread generiert wurden.

**cblogdatensatz**

Die Gesamtgröße der Transaktionsprotokoll Datensätze in Bytes, die von der Datenbank-Engine im aktuellen Thread generiert wurden.

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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Jetgetthreadstats](./jetgetthreadstats-function.md)
