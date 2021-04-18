---
description: Definiert Schablonen Puffer Vorgänge.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: D3DSTENCILOP-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTENCILOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 34784a57d3afd3862d380554040f3909ec905898
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371900"
---
# <a name="d3dstencilop-enumeration"></a>D3DSTENCILOP-Enumeration

Definiert Schablonen Puffer Vorgänge.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSTENCILOP { 
  D3DSTENCILOP_KEEP         = 1,
  D3DSTENCILOP_ZERO         = 2,
  D3DSTENCILOP_REPLACE      = 3,
  D3DSTENCILOP_INCRSAT      = 4,
  D3DSTENCILOP_DECRSAT      = 5,
  D3DSTENCILOP_INVERT       = 6,
  D3DSTENCILOP_INCR         = 7,
  D3DSTENCILOP_DECR         = 8,
  D3DSTENCILOP_FORCE_DWORD  = 0x7fffffff
} D3DSTENCILOP, *LPD3DSTENCILOP;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ beibehalten**
</dt> <dd>

Aktualisieren Sie den Eintrag nicht im Schablonen Puffer. Dies ist der Standardwert.

</dd> <dt>

<span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ 0**
</dt> <dd>

Legen Sie den Schablone-Puffer Eintrag auf 0 fest.

</dd> <dt>

<span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ ersetzen**
</dt> <dd>

Ersetzen Sie den Stencil-Buffer-Eintrag durch einen Verweis Wert.

</dd> <dt>

<span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP \_ incrsat**
</dt> <dd>

Erhöhen Sie den Schablone-Puffer Eintrag, und legen Sie auf den maximalen Wert an.

</dd> <dt>

<span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ decrsat**
</dt> <dd>

Dekrement der Schablone-Puffer Eintrag, der auf 0 (null) gesetzt wird.

</dd> <dt>

<span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP \_ umkehren**
</dt> <dd>

Umkehren Sie die Bits im Schablone-Puffer Eintrag.

</dd> <dt>

<span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP \_ INCR**
</dt> <dd>

Erhöhen Sie den Schablonen Puffer Eintrag, wobei der Wert auf 0 (null) umwickelt wird, wenn der neue Wert den maximalen Wert überschreitet.

</dd> <dt>

<span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP- \_ decr**
</dt> <dd>

Verringert den Schablonen Puffer Eintrag und umwickelt ihn in den maximalen Wert, wenn der neue Wert kleiner als 0 (null) ist.

</dd> <dt>

<span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Schablone-Puffer Einträge sind ganzzahlige Werte im Bereich von 0 bis 2 ⁿ-1, wobei n die Bittiefe des Schablonen Puffers ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




