---
description: 'Weitere Informationen finden Sie unter: JET_ERRINFOBASIC_W Struktur'
title: JET_ERRINFOBASIC_W Struktur
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: f6a91d14fe636a2ccf3b00935af53db7caa0bf257833e72780d706e14822d5a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401840"
---
# <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W Struktur

Die **JET_ERRINFOBASIC_W** definiert die Daten, die von der [JetGetErrorInfo()-Methode](./jetgeterrorinfow-function.md) zurückgegeben werden, wenn der JET_ErrorInfoSpecificErr InfoLevel übergeben wird.

Hinweis: Diese Dokumentation basiert auf einer vorläufigen Version der Extensible Storage Engine. Diese Informationen können geändert werden.

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der -Struktur in Bytes. Sie muss auf sizeof( JET_ERRINFOBASIC ) festgelegt werden.

**errValue**

Der Fehlerwert, der ausgewertet wurde, wie für das *pvResult-Argument* an [JetGetErrorInfo() übergeben.](./jetgeterrorinfow-function.md)

**errcatMostSpecific**

Die Konstante der niedrigsten [JET_ERRCAT,](./jet-errcat.md) die dem Fehler zugeordnet ist. Das heißt, die Kategorie auf Blattebene in der Kategoriehierarchie, die [in](./jet-errcat.md)JET_ERRCAT.

**rgCategoricalHierarchy \[ 8\]**

Die Hierarchie der Fehlerkategorien, die dem Fehler zugeordnet ist. Position 0 ist die höchste Ebene in der Hierarchie von [JET_ERRCAT,](./jet-errcat.md)und die übrigen sind Unterkategorien, bis die spezifischste Kategorie festgelegt ist, nach der alle Kategorien JET_errcatUnknown.

**lSourceLine**

Reserviert.

**rgszSourceFile \[ 64\]**

Reserviert.

### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>
