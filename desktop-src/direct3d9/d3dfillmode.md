---
description: Definiert Konstanten, die den Füllmodus beschreiben.
ms.assetid: be835432-e8d5-4afb-a810-2dac25bdc9dc
title: D3DFILLMODE-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFILLMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e92d91c13718462487eb3dac07ba1d5fc61a2d428bf610dd9575b080d375676d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857450"
---
# <a name="d3dfillmode-enumeration"></a>D3DFILLMODE-Enumeration

Definiert Konstanten, die den Füllmodus beschreiben.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DFILLMODE { 
  D3DFILL_POINT        = 1,
  D3DFILL_WIREFRAME    = 2,
  D3DFILL_SOLID        = 3,
  D3DFILL_FORCE_DWORD  = 0x7fffffff
} D3DFILLMODE, *LPD3DFILLMODE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**D3DFILL \_ POINT**
</dt> <dd>

Füllpunkte.

</dd> <dt>

<span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL \_ WIREFRAME**
</dt> <dd>

Füllen Sie Wireframes aus.

</dd> <dt>

<span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL \_ SOLID**
</dt> <dd>

Auffüllen von Vollkörpern.

</dd> <dt>

<span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Werte in diesem Enumerationstyp werden vom D3DRS \_ FILLMODE-Renderzustand verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
