---
description: 'Weitere Informationen zu: JET_INDEXID-Struktur'
title: JET_INDEXID-Struktur
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: 61e51e85fe990cfeee8a5c1ee048a77179d49766
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475956"
---
# <a name="jet_indexid-structure"></a>JET_INDEXID-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_indexid-structure"></a>JET_INDEXID-Struktur

Die **JET_INDEXID-Struktur** enthält eine Index-ID. Eine Index-ID ist ein Hinweis, der verwendet wird, um die Auswahl des aktuellen Indexes mit [jetSetCurrentIndex](./jetsetcurrentindex-function.md)zu beschleunigen. Dies ist besonders nützlich, wenn es eine sehr große Anzahl von Indizes für eine Tabelle gibt. Die Index-ID kann mit [JetGetIndexInfo](./jetgetindexinfo-function.md) oder [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)abgerufen werden.

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der Index-ID in Bytes.

Dies ist die tatsächliche Größe der Index-ID, die im Ausgabepuffer von [JetGetIndexInfo](./jetgetindexinfo-function.md) oder [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)zurückgegeben wird.

**rgbIndexId**

Ein nicht transparentes BLOB von Informationen, das von der Engine verwendet wird, um schnell einen Index im Schemacache zu identifizieren.

Versuchen Sie nicht, das BLOB der Informationen zu interpretieren. Es handelt sich nicht um eine festgelegte Größe.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
