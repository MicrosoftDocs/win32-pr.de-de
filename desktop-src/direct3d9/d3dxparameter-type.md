---
description: Beschreibt die in der -Enumeration enthaltenen Daten.
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: D3DXPARAMETER_TYPE -Enumeration (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 2d342e664aac81cf337cde2de7669c94a4ac6c94ce85c564a29da1f38dd93bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096190"
---
# <a name="d3dxparameter_type-enumeration"></a>D3DXPARAMETER \_ TYPE-Enumeration

Beschreibt die in der -Enumeration enthaltenen Daten.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ VOID**
</dt> <dd>

Parameter ist ein void-Zeiger.

</dd> <dt>

<span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT \_ BOOL**
</dt> <dd>

Parameter ist ein boolescher Wert. Jeder Wert, der nicht null ist und an [**ID3DXConstantTable::SetBool,**](id3dxconstanttable--setbool.md) [**ID3DXConstantTable::SetBoolArray,**](id3dxconstanttable--setboolarray.md) [**ID3DXConstantTable::SetValue,**](id3dxconstanttable--setvalue.md) [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md)oder [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) übergeben wird, wird 1 (TRUE) zugeordnet, bevor er in die konstante Tabelle geschrieben wird. Andernfalls wird der Wert in der konstanten Tabelle auf 0 festgelegt.

</dd> <dt>

<span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ INT**
</dt> <dd>

Der Parameter ist eine ganze Zahl. Alle Gleitkommawerte, die an [**ID3DXConstantTable::SetValue,**](id3dxconstanttable--setvalue.md) [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md)oder [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) übergeben werden, werden vor dem Schreiben in die Konstantentabelle abgerundet (auf null Dezimalstellen).

</dd> <dt>

<span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ FLOAT**
</dt> <dd>

Parameter ist eine Gleitkommazahl.

</dd> <dt>

<span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**D3DXPT \_ STRING**
</dt> <dd>

Der Parameter ist eine Zeichenfolge.

</dd> <dt>

<span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**D3DXPT-TEXTUR \_**
</dt> <dd>

Parameter ist eine Textur.

</dd> <dt>

<span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**
</dt> <dd>

Parameter ist eine 1D-Textur.

</dd> <dt>

<span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**
</dt> <dd>

Parameter ist eine 2D-Textur.

</dd> <dt>

<span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**
</dt> <dd>

Parameter ist eine 3D-Textur.

</dd> <dt>

<span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ TEXTURECUBE**
</dt> <dd>

Der Parameter ist eine Cubetextur.

</dd> <dt>

<span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT \_ SAMPLER**
</dt> <dd>

Parameter ist ein Sampler.

</dd> <dt>

<span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**
</dt> <dd>

Parameter ist ein 1D-Sampler.

</dd> <dt>

<span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**
</dt> <dd>

Parameter ist ein 2D-Sampler.

</dd> <dt>

<span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**
</dt> <dd>

Parameter ist ein 3D-Sampler.

</dd> <dt>

<span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ SAMPLERCUBE**
</dt> <dd>

Parameter ist ein Cube-Sampler.

</dd> <dt>

<span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ PIXELSHADER**
</dt> <dd>

Parameter ist ein Pixel-Shader.

</dd> <dt>

<span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ VERTEXSHADER**
</dt> <dd>

Parameter ist ein Vertex-Shader.

</dd> <dt>

<span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ PIXELFRAGMENT**
</dt> <dd>

Parameter ist ein Pixel-Shaderfragment.

</dd> <dt>

<span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ VERTEXFRAGMENT**
</dt> <dd>

Parameter ist ein Vertex-Shaderfragment.

</dd> <dt>

<span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT \_ NICHT UNTERSTÜTZT**
</dt> <dd>

Der Parameter wird nicht unterstützt.

</dd> <dt>

<span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




