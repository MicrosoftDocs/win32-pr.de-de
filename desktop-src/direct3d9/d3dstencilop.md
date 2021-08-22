---
description: Definiert Schablonenpuffervorgänge.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: D3DSTENCILOP-Enumeration (D3D9Types.h)
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
ms.openlocfilehash: 166f670e6e34edd6a3b05584c54e63be274e54161faea242fa701e771a90a771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564940"
---
# <a name="d3dstencilop-enumeration"></a>D3DSTENCILOP-Enumeration

Definiert Schablonenpuffervorgänge.

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

<span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ KEEP**
</dt> <dd>

Aktualisieren Sie den Eintrag im Schablonenpuffer nicht. Dies ist der Standardwert.

</dd> <dt>

<span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ NULL**
</dt> <dd>

Legen Sie den Schablonenpuffereintrag auf 0 fest.

</dd> <dt>

<span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ REPLACE**
</dt> <dd>

Ersetzen Sie den Schablonenpuffereintrag durch einen Verweiswert.

</dd> <dt>

<span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP \_ INCRSAT**
</dt> <dd>

Erhöhen Sie den Schablonenpuffereintrag, und klammern Sie sich an den Maximalwert.

</dd> <dt>

<span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ DECRSAT**
</dt> <dd>

Dekrementieren Sie den Schablonenpuffereintrag, und klammern Sie an 0 (null).

</dd> <dt>

<span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP \_ INVERT**
</dt> <dd>

Invertiert die Bits im Schablonenpuffereintrag.

</dd> <dt>

<span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP \_ INCR**
</dt> <dd>

Inkrementiert den Schablonenpuffereintrag und wird auf 0 (null) gesetzt, wenn der neue Wert den Maximalwert überschreitet.

</dd> <dt>

<span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP \_ DECR**
</dt> <dd>

Dekrementierung des Schablonenpuffereintrags und Umschließen bis zum höchstwert, wenn der neue Wert kleiner als 0 (null) ist.

</dd> <dt>

<span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Schablonenpuffereinträge sind ganzzahlige Werte im Bereich von 0 bis 2ⁿ – 1, wobei n die Bittiefe des Schablonenpuffers ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




