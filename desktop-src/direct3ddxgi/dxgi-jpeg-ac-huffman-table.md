---
description: Beschreibt eine JPEG AC huffman-Tabelle.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: DXGI_JPEG_AC_HUFFMAN_TABLE -Struktur (Dxgitype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 21e279e4974d221a6feba6f135343d122f30f3da1edb18210e0e14f92fdb94a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518373"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a>DXGI \_ JPEG \_ AC \_ HUFFMAN \_ TABLE-Struktur

Beschreibt eine JPEG AC huffman-Tabelle.

## <a name="syntax"></a>Syntax


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**CodeCounts**
</dt> <dd>

Die Anzahl der Codes für jede Codelänge.

</dd> <dt>

**CodeValues**
</dt> <dd>

Die Huffman-Codewerte in der Reihenfolge, in der die Codelänge erhöht wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dxgitype.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DXGI-Strukturen](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




