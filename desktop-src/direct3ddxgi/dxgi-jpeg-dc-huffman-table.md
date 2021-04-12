---
description: Beschreibt eine JPEG-DC-Huffman-Tabelle.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: DXGI_JPEG_DC_HUFFMAN_TABLE-Struktur (dxgitype. h)
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
ms.openlocfilehash: b2f5f73f7c6def745b987818b9ec30fb3e2752e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219487"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a>DXGI \_ JPEG- \_ DC- \_ Huffman- \_ Tabellenstruktur

Beschreibt eine JPEG-DC-Huffman-Tabelle.

## <a name="syntax"></a>Syntax


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**Codecount**
</dt> <dd>

Die Anzahl der Codes für jede Codelänge.

</dd> <dt>

**Codevalues**
</dt> <dd>

Die Huffman-Codewerte in der Reihenfolge, in der die Codelänge erhöht wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DXGI-Strukturen](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




