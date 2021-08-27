---
description: 'Weitere Informationen finden Sie unter: JET_RECPOS Struktur'
title: JET_RECPOS Struktur
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: ed374030bd3ab577b209d326d21110482c9cf37a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989113"
---
# <a name="jet_recpos-structure"></a>JET_RECPOS Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_recpos-structure"></a>JET_RECPOS Struktur

Die **JET_RECPOS-Struktur** enthält eine Auflistung von ganzen Zahlen, die eine Bruchposition innerhalb eines Indexes darstellen. **centriesLT** ist die Anzahl von Indexeinträgen, die kleiner als der aktuelle Indexschlüssel sind. **centriesInRange** ist die Anzahl von Indexeinträgen, die dem aktuellen Schlüssel entspricht. **centriesInRange** wird nicht unterstützt und immer als 1 zurückgegeben. **centriesTotal ist** die Anzahl der Indexeinträge im Index. Alle Werte sind Näherungen ohne Genauigkeitsgarantie.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der [JET_RETINFO](./jet-retinfo-structure.md) -Struktur in Bytes. Dieser Wert bestätigt das Vorhandensein der folgenden Felder.

**centriesLT**

Die ungefähre Anzahl von Indexeinträgen, die kleiner als der aktuelle Schlüssel sind.

**centriesInRange**

Die ungefähre Anzahl von Indexeinträgen, die dem aktuellen Schlüssel entspricht. Dieses Feld ist immer auf 1 festgelegt, unabhängig davon, wie viele Indexeinträge tatsächlich gleich dem aktuellen Schlüssel sind.

**centriesTotal**

Die ungefähre Anzahl von Einträgen im Index.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)
