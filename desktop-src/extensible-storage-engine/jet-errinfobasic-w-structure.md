---
description: 'Weitere Informationen finden Sie hier: JET_ERRINFOBASIC_W Struktur'
title: JET_ERRINFOBASIC_W Struktur
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103961782"
---
# <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W Struktur

Die **JET_ERRINFOBASIC_W** -Struktur definiert die Daten, die von der [jetgeterrorinfo ()](./jetgeterrorinfow-function.md) -Methode zurückgegeben werden, wenn die JET_ErrorInfoSpecificErr infolevel-Methode übermittelt wird.

Hinweis: Diese Dokumentation basiert auf einer vorläufigen Version der Extensible Storage-Engine. Diese Informationen können geändert werden.

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

Die Größe der-Struktur in Bytes. Er muss auf sizeof (JET_ERRINFOBASIC) festgelegt werden.

**errvalue**

Der auszuwertende Fehlerwert, wie für das *pvresult* -Argument an [jetgeterrorinfo ()](./jetgeterrorinfow-function.md)übergeben.

**Err| mustspecific**

Die [JET_ERRCAT](./jet-errcat.md) Konstante der untersten Ebene, die dem Fehler zugeordnet ist. Das heißt, die Kategorie auf Blatt Ebene in der Kategoriehierarchie, die in [JET_ERRCAT](./jet-errcat.md)dokumentiert ist.

**rgkategoricalhierarchy \[ 8\]**

Die Hierarchie von Fehlerkategorien, die dem Fehler zugeordnet ist. Position 0 ist die höchste Ebene in der Hierarchie von [JET_ERRCAT](./jet-errcat.md), und der Rest sind Unterkategorien, bis die spezifischere Kategorie festgelegt ist, nach der alle Kategorien JET_errcatUnknown werden.

**lsourceline**

Reserviert.

**rgszsourcefile \[ 64\]**

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
<td><p>Erfordert Windows 8-Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>
