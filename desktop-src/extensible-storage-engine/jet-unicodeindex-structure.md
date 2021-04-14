---
description: 'Weitere Informationen finden Sie hier: JET_UNICODEINDEX Struktur'
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
ms.openlocfilehash: c4a2332551fb1f624b75e32596b2941d97ffa47d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104394278"
---
# <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX Struktur

Mit der **JET_UNICODEINDEX** -Struktur wird angepasst, wie Unicode-Daten normalisiert werden, wenn ein Index für eine Unicode-Spalte erstellt wird.

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a>Member

**lcid**

Die Gebiets Schema-ID, die beim Normalisieren der Daten verwendet werden soll. Jedes Gebiets Schema kann verwendet werden, solange das entsprechende Sprachpaket auf dem Computer installiert wurde. Die einzige Ausnahme ist, dass das sprachneutrale Gebiets Schema (LCID of Zero) unzulässig ist.

**dwMapFlags**

Diese Flags werden an [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) übergeben, wenn Unicode-Daten zu einem Schlüssel normalisiert werden, sodass benutzerdefinierte Flags den Standardwert überschreiben können.

**Windows 2000**: die einzigen beiden gültigen Werte für **dwFlags** lauten:

  - (LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE)

<!-- end list -->

  - (LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH)

für **dwmapflags** gelten die folgenden Einschränkungen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>LCMAP_SORTKEY</p></td>
<td><p>Erforderlich.</p></td>
</tr>
<tr class="even">
<td><p>LCMAP_BYTEREV</p></td>
<td><p>Dies ist optional.</p></td>
</tr>
<tr class="odd">
<td><p>NORM_IGNORECASE</p></td>
<td><p>Dies ist optional.</p></td>
</tr>
<tr class="even">
<td><p>NORM_IGNORENONSPACE</p></td>
<td><p>Dies ist optional.</p></td>
</tr>
<tr class="odd">
<td><p>NORM_IGNORESYMBOLS</p></td>
<td><p>Dies ist optional.</p></td>
</tr>
<tr class="even">
<td><p>NORM_IGNOREKANATYPE</p></td>
<td><p>Dies ist optional.</p></td>
</tr>
<tr class="odd">
<td><p>NORM_IGNOREWIDTH</p></td>
<td><p>Dies ist optional.</p></td>
</tr>
<tr class="even">
<td><p>SORT_STRINGSORT</p></td>
<td><p>Dies ist optional.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)
