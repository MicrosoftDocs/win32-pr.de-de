---
description: Definiert Konstanten, die Transformations Zustands Werte beschreiben.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: D3DTRANSFORMSTATETYPE-Enumeration (D3D9Types. h)
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
ms.openlocfilehash: c618e0e19bf7dd01dec73d35436f23189f9e78a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366631"
---
# <a name="d3dtransformstatetype-enumeration"></a>D3DTRANSFORMSTATETYPE-Enumeration

Definiert Konstanten, die Transformations Zustands Werte beschreiben.

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

<span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS- \_ Sicht**
</dt> <dd>

Gibt an, dass die Transformationsmatrix als Transformationsmatrix der Sicht festgelegt wird. Der Standardwert ist **null** (die Identitätsmatrix).

</dd> <dt>

<span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS- \_ Projektion**
</dt> <dd>

Gibt an, dass die Transformationsmatrix als Projektions Transformationsmatrix festgelegt wird. Der Standardwert ist **null** (die Identitätsmatrix).

</dd> <dt>

<span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**
</dt> <dd>

Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ TEXTURE1**
</dt> <dd>

Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ Texture2 fest**
</dt> <dd>

Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**
</dt> <dd>

Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**
</dt> <dd>

Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**
</dt> <dd>

Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**
</dt> <dd>

Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.

</dd> <dt>

<span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**
</dt> <dd>

Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.

</dd> <dt>

<span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Transformations Zustände im Bereich 256 bis 511 sind zum Speichern von bis zu 256 World Matrizen reserviert, die mithilfe der \_ Makros D3DTS worldmatrix und D3DTS World indiziert werden können \_ .



| Makros                                                  |                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DTS \_ Welt**](d3dts-world.md)                     | Entspricht D3DTS \_ worldmatrix (0).                                                                                                                                  |
| [**D3DTS \_ Worldmatrix**](d3dts-worldmatrix.md) (Index) | Gibt die Transformationsmatrix an, die für die Weltmatrix beim Index festgelegt werden soll. Mehrere Welt Matrizen werden nur für Vertex-Blending verwendet. Andernfalls wird nur D3DTS \_ World verwendet. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**IDirect3DDevice9:: MultiplyTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**IDirect3DDevice9:: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ Welt**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ worldn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
