---
description: Beschreibt eine JPEG AC-Huffman-Tabelle.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: DXGI_JPEG_AC_HUFFMAN_TABLE-Struktur (dxgitype. h)
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
ms.openlocfilehash: 760840822eb6b9411983c72324bc1e86a3208195
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353353"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a>DXGI \_ JPEG \_ AC- \_ Huffman- \_ Tabellenstruktur

Beschreibt eine JPEG AC-Huffman-Tabelle.

## <a name="syntax"></a>Syntax


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
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

 

 




