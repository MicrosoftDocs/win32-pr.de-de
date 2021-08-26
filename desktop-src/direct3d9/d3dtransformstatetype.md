---
description: Definiert Konstanten, die Transformationszustandswerte beschreiben.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: D3DTRANSFORMSTATETYPE-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 299246ef890015a6d7de465ecc7c00251a52432d276a87f3d5f336b63d563737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986990"
---
# <a name="d3dtransformstatetype-enumeration"></a>D3DTRANSFORMSTATETYPE-Enumeration

Definiert Konstanten, die Transformationszustandswerte beschreiben.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS-ANSICHT \_**
</dt> <dd>

Identifiziert die Transformationsmatrix, die als Ansichtstransformationsmatrix festgelegt wird. Der Standardwert ist **NULL** (die Identitätsmatrix).

</dd> <dt>

<span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS-PROJEKTION \_**
</dt> <dd>

Identifiziert die Transformationsmatrix, die als Projektionstransformationsmatrix festgelegt wird. Der Standardwert ist **NULL** (die Identitätsmatrix).

</dd> <dt>

<span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**
</dt> <dd>

Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ TEXTURE1**
</dt> <dd>

Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ TEXTURE2**
</dt> <dd>

Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**
</dt> <dd>

Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**
</dt> <dd>

Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**
</dt> <dd>

Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**
</dt> <dd>

Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**
</dt> <dd>

Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.

</dd> <dt>

<span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Transformationszustände im Bereich von 256 bis 511 sind für die Speicherung von bis zu 256 Weltmatrizen reserviert, die mithilfe der D3DTS \_ WORLDMATRIX- und D3DTS WORLD-Makros indiziert werden \_ können.



| Makros                                                  | BESCHREIBUNG                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DTS \_ WORLD**](d3dts-world.md)                     | Entspricht D3DTS \_ WORLDMATRIX(0).                                                                                                                                  |
| [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (Index) | Identifiziert die Transformationsmatrix, die für die Weltmatrix am Index festgelegt werden soll. Mehrere Weltmatrizen werden nur für Scheitelpunktmischungen verwendet. Andernfalls wird nur D3DTS \_ WORLD verwendet. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**IDirect3DDevice9::MultiplyTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ WORLD**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ WORLDn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
