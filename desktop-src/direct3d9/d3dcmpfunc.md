---
description: Definiert die unterstützten Vergleichsfunktionen.
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: D3DCMPFUNC-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCMPFUNC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e49f0e058e795e00349020619f1e6d6310dfd94f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870091"
---
# <a name="d3dcmpfunc-enumeration"></a>D3DCMPFUNC-Enumeration

Definiert die unterstützten Vergleichsfunktionen.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DCMPFUNC { 
  D3DCMP_NEVER         = 1,
  D3DCMP_LESS          = 2,
  D3DCMP_EQUAL         = 3,
  D3DCMP_LESSEQUAL     = 4,
  D3DCMP_GREATER       = 5,
  D3DCMP_NOTEQUAL      = 6,
  D3DCMP_GREATEREQUAL  = 7,
  D3DCMP_ALWAYS        = 8,
  D3DCMP_FORCE_DWORD   = 0x7fffffff
} D3DCMPFUNC, *LPD3DCMPFUNC;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ nie**
</dt> <dd>

Fehler beim Test immer.

</dd> <dt>

<span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ less**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn der Wert kleiner ist als der Wert des aktuellen Pixels.

</dd> <dt>

<span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP \_ gleich**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn sein Wert dem Wert des aktuellen Pixels gleicht.

</dd> <dt>

<span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP \_ lessequal**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn der Wert kleiner oder gleich dem Wert des aktuellen Pixels ist.

</dd> <dt>

<span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ größer**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn der Wert größer ist als der Wert des aktuellen Pixels.

</dd> <dt>

<span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP \_ NotEqual**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn der Wert nicht dem Wert des aktuellen Pixels entspricht.

</dd> <dt>

<span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP \_ greaterequal**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn der Wert größer oder gleich dem Wert des aktuellen Pixels ist.

</dd> <dt>

<span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP \_ immer**
</dt> <dd>

Bestanden Sie den Test immer.

</dd> <dt>

<span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Werte in diesem enumerierten Typ definieren die unterstützten Vergleichsfunktionen für die \_ Rendering-Zustände D3DRS zfunc, D3DRS \_ alphafunc und D3DRS \_ stencilfunc.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
