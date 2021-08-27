---
description: 'Weitere Informationen zu: JET_RECPOS-Struktur'
title: JET_RECPOS-Struktur
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
ms.openlocfilehash: 6eb136ef309bad4ffd5c02768a3ca5b8e0d52f3c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470515"
---
# <a name="jet_recpos-structure"></a>JET_RECPOS-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_recpos-structure"></a>JET_RECPOS-Struktur

Die **JET_RECPOS-Struktur** enthält eine Auflistung von ganzen Zahlen, die eine Bruchposition innerhalb eines Indexes darstellen. **centriesLT** ist die Anzahl der Indexeinträge kleiner als der aktuelle Indexschlüssel. **centriesInRange** ist die Anzahl der Indexeinträge, die dem aktuellen Schlüssel entsprechen. **centriesInRange** wird nicht unterstützt und immer als 1 zurückgegeben. **centriesTotal** ist die Anzahl der Indexeinträge im Index. Alle Werte sind Näherungen ohne Garantie der Genauigkeit.

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

Die Größe der [JET_RETINFO-Struktur](./jet-retinfo-structure.md) in Bytes. Dieser Wert bestätigt das Vorhandensein der folgenden Felder.

**centriesLT**

Die ungefähre Anzahl von Indexeinträgen kleiner als der aktuelle Schlüssel.

**centriesInRange**

Die ungefähre Anzahl von Indexeinträgen, die dem aktuellen Schlüssel entsprechen. Dieses Feld ist immer auf 1 festgelegt, unabhängig von der Anzahl der Indexeinträge, die tatsächlich dem aktuellen Schlüssel entsprechen.

**centriesTotal**

Die ungefähre Anzahl von Einträgen im Index.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)
