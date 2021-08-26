---
description: 'Weitere Informationen finden Sie unter: JET_UNICODEINDEX Struktur'
title: JET_UNICODEINDEX Struktur
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
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
ms.openlocfilehash: 544438541affba1121850d5ad5a7a60d54d398bd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471386"
---
# <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX Struktur

Die **JET_UNICODEINDEX-Struktur** passt an, wie Unicode-Daten normalisiert werden, wenn ein Index über eine Unicode-Spalte erstellt wird.

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a>Member

**lcid**

Die Beim Normalisieren der Daten zu verwendende Locale-ID. Ein beliebiges Locale kann verwendet werden, solange das entsprechende Sprachpaket auf dem Computer installiert wurde. Die einzige Ausnahme ist, dass das sprachneutrale Locale (LCID von 0) ungültig ist.

**dwMapFlags**

Diese Flags werden an [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) übergeben, wenn Unicode-Daten in einen Schlüssel normalisiert werden, wodurch benutzerdefinierte Flags die Standardeinstellung überschreiben können.

**Windows 2000:** Die einzigen beiden rechtlichen Werte für **dwFlags** sind:

  - ( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE )

<!-- end list -->

  - ( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH )

**für dwMapFlags** gelten die folgenden Einschränkungen.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>LCMAP_SORTKEY</p> | <p>Erforderlich.</p> | 
| <p>LCMAP_BYTEREV</p> | <p>Optional.</p> | 
| <p>NORM_IGNORECASE</p> | <p>Optional.</p> | 
| <p>NORM_IGNORENONSPACE</p> | <p>Optional.</p> | 
| <p>NORM_IGNORESYMBOLS</p> | <p>Optional.</p> | 
| <p>NORM_IGNOREKANATYPE</p> | <p>Optional.</p> | 
| <p>NORM_IGNOREWIDTH</p> | <p>Optional.</p> | 
| <p>SORT_STRINGSORT</p> | <p>Optional.</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)
