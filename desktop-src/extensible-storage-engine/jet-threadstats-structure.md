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
ms.openlocfilehash: 7f94c9911fb7ab974f87cfed41e92b53ac0a66cb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983563"
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

Die Größe der zurückgegebenen **JET_THREADSTATS** -Struktur in Bytes.

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


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetGetThreadStats](./jetgetthreadstats-function.md)
