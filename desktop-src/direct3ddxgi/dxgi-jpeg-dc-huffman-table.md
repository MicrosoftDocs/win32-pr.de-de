---
description: Beschreibt eine JPEG DC huffman-Tabelle.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: DXGI_JPEG_DC_HUFFMAN_TABLE -Struktur (Dxgitype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b431bbccb66bcb24e068229493ef87f2ac96736161bb306609ac4dd479dfb7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987120"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a>DXGI \_ JPEG \_ DC \_ HUFFMAN \_ TABLE-Struktur

Beschreibt eine JPEG DC huffman-Tabelle.

## <a name="syntax"></a>Syntax


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DXGI-Strukturen](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




