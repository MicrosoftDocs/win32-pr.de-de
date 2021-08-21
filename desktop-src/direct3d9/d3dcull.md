---
description: Definiert die unterstützten Cullingmodi.
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: D3DCULL-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 062135f1eff43bd568f1b08674985b4744e0835ebf3fa9e78c2756a798f85ccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989060"
---
# <a name="d3dcull-enumeration"></a>D3DCULL-Enumeration

Definiert die unterstützten Cullingmodi.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ NONE**
</dt> <dd>

Ziehe keine Zurück-Gesichter um.

</dd> <dt>

<span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL \_ CW**
</dt> <dd>

Zurückkullen von Gesichtern mit Scheitelpunkten im Uhrzeigersinn.

</dd> <dt>

<span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL \_ CCW**
</dt> <dd>

Zurückkullen von Gesichtern mit gegen den Uhrzeigersinn.

</dd> <dt>

<span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Werte in diesem Enumerationstyp werden vom D3DRS \_ CULLMODE-Renderzustand verwendet. Die Culling-Modi definieren, wie Hintergesichter beim Rendern einer Geometrie gerendert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
