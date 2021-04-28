---
description: 'D3DX10_WELD_EPSILONS-Struktur: Gibt Toleranzwerte für jede Scheitelpunktkomponente an, wenn Scheitelpunkte verglichen werden, um zu bestimmen, ob sie ähnlich genug sind, um zusammen zusammengestellt zu werden.'
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: D3DX10_WELD_EPSILONS-Struktur (D3DX10.h)
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
ms.openlocfilehash: 720a10dbe4b22b69910d88d3c03cea9ded768f1b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105428"
---
# <a name="d3dx10_weld_epsilons-structure"></a>D3DX10 \_ VERZEIGEN \_ EPSILONS-Struktur

Gibt Beim Vergleich von Scheitelpunkten Toleranzwerte für jede Scheitelpunktkomponente an, um zu bestimmen, ob sie ähnlich genug sind, um zusammengeknauft zu werden.

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

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Position

</dd> <dt>

**BlendWeights**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Mischungsgewichtung

</dd> <dt>

**Normal**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Normal

</dd> <dt>

**PSize**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Wert der Punktgröße

</dd> <dt>

**Glänzend**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Glanzlichtwert

</dd> <dt>

**Diffus**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Diffuser Beleuchtungswert

</dd> <dt>

**Texcoord**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Acht Texturkoordinaten

</dd> <dt>

**Tangente**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangens

</dd> <dt>

**Binormal**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal

</dd> <dt>

**TessFactor**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Mosaikfaktor

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der LPD3DXWeldEpsilons-Typ ist als Zeiger auf die D3DXWeldEpsilons-Struktur definiert.


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
