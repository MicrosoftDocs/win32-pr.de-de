---
description: Definiert die unterstützten Vergleichsfunktionen.
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: D3DCMPFUNC-Enumeration (D3D9Types.h)
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
ms.openlocfilehash: 1fa8d0c9288e6c0d516e7fc9b8a07237f553dd6c86072f1895edf9a79c297077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989108"
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

<span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ NEVER**
</dt> <dd>

Der Test ist immer nicht bestanden.

</dd> <dt>

<span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ LESS**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn sein Wert kleiner als der Wert des aktuellen Pixels ist.

</dd> <dt>

<span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP \_ EQUAL**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn sein Wert dem Wert des aktuellen Pixels entspricht.

</dd> <dt>

<span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP \_ LESSEQUAL**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn sein Wert kleiner oder gleich dem Wert des aktuellen Pixels ist.

</dd> <dt>

<span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ GREATER**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn sein Wert größer als der Wert des aktuellen Pixels ist.

</dd> <dt>

<span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP \_ NOTEQUAL**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn sein Wert nicht dem Wert des aktuellen Pixels entspricht.

</dd> <dt>

<span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP \_ GREATEREQUAL**
</dt> <dd>

Akzeptieren Sie das neue Pixel, wenn sein Wert größer oder gleich dem Wert des aktuellen Pixels ist.

</dd> <dt>

<span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP \_ ALWAYS**
</dt> <dd>

Bestehen Sie den Test immer.

</dd> <dt>

<span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Werte in diesem enumerierten Typ definieren die unterstützten Vergleichsfunktionen für die Renderzustände D3DRS \_ DEFINUNC, D3DRS \_ ALPHAFUNC und D3DRS \_ STENCILFUNC.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
