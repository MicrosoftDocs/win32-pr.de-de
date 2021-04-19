---
description: Gibt Toleranzwerte für jede Scheitelpunkt Komponente an, wenn Vertices verglichen werden, um zu bestimmen, ob Sie so ähnlich sind, dass Sie miteinander verbunden werden.
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: D3DX10_WELD_EPSILONS-Struktur (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_WELD_EPSILONS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: c72f63e3ecef1fdb193fcaec9220f9768204d099
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367458"
---
# <a name="d3dx10_weld_epsilons-structure"></a>D3dx10 \_ Weld \_ epsilons-Struktur

Gibt Toleranzwerte für jede Scheitelpunkt Komponente an, wenn Vertices verglichen werden, um zu bestimmen, ob Sie so ähnlich sind, dass Sie miteinander verbunden werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DX10_WELD_EPSILONS {
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
} D3DX10_WELD_EPSILONS, *LPD3DX10_WELD_EPSILONS;
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

Der LPD3DXWeldEpsilons-Typ wird als Zeiger auf die D3DXWeldEpsilons-Struktur definiert.


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx10. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
