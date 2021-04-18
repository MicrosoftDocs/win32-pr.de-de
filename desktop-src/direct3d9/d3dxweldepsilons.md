---
description: Gibt Toleranzwerte für jede Scheitelpunkt Komponente an, wenn Vertices verglichen werden, um zu bestimmen, ob Sie so ähnlich sind, dass Sie miteinander verbunden werden.
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: D3DXWELDEPSILONS-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWELDEPSILONS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6b6673e16b153f53baf17967b7f33c4bcb40d518
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365105"
---
# <a name="d3dxweldepsilons-structure"></a>D3DXWELDEPSILONS-Struktur

Gibt Toleranzwerte für jede Scheitelpunkt Komponente an, wenn Vertices verglichen werden, um zu bestimmen, ob Sie so ähnlich sind, dass Sie miteinander verbunden werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DXWELDEPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DXWELDEPSILONS, *LPD3DXWELDEPSILONS;
```



## <a name="members"></a>Member

<dl> <dt>

**Position**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Position

</dd> <dt>

**Blendweights**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Blend-Gewichtung

</dd> <dt>

**Normal**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Normal

</dd> <dt>

**Psize**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Wert der Punktgröße

</dd> <dt>

**Glänzend**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Glanzlicht Wert

</dd> <dt>

**Diffus**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Diffuses Beleuchtungs Wert

</dd> <dt>

**Texcoord**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Acht Texturkoordinaten

</dd> <dt>

**Tangens**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangens

</dd> <dt>

**Binormal**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal

</dd> <dt>

**Mosaik Faktor**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Mosaik Faktor

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der LPD3DXWELDEPSILONS-Typ wird als Zeiger auf die **D3DXWELDEPSILONS** -Struktur definiert.


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXWeldVertices**](d3dxweldvertices.md)
</dt> </dl>

 

 
