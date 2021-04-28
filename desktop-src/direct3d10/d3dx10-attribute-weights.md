---
description: 'D3DX10_ATTRIBUTE_WEIGHTS Struktur: Gibt Die Attribute für die Netzgewichtung an.'
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: D3DX10_ATTRIBUTE_WEIGHTS-Struktur (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ab163149493ad73f892a251a691ad82544d7f382
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094352"
---
# <a name="d3dx10_attribute_weights-structure"></a>D3DX10 \_ ATTRIBUTE \_ WEIGHTS-Struktur

Gibt Gitternetzgewichtungsattribute an.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a>Member

<dl> <dt>

**Position**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Position

</dd> <dt>

**Grenze**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Mischungsgewichtung.

</dd> <dt>

**Normal**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Normal.

</dd> <dt>

**Diffus**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Diffuser Beleuchtungswert.

</dd> <dt>

**Glänzend**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Glanzlichtwert.

</dd> <dt>

**Texcoord**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Acht Texturkoordinaten.

</dd> <dt>

**Tangente**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente.

</dd> <dt>

**Binormal**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur beschreibt, wie bei einem Vereinfachungsvorgang Scheitelpunktdaten berücksichtigt werden, wenn relative Kosten zwischen reduzierenden Kanten berechnet werden. Wenn das Feld Normal z. B. 0,0 ist, ignoriert der Vereinfachungsvorgang die normale Scheitelpunktkomponente, wenn der Fehler für das Reduzieren berechnet wird. Wenn das Feld Normal jedoch 1,0 ist, verwendet der Vereinfachungsvorgang die Scheitelpunktnorm normal-Komponente. Wenn das Feld Normal den Wert 2.0 hat, sollten Sie die Anzahl der Fehler verdoppelt. Wenn das Feld Normal 4.0 ist, verffachen Sie die Anzahl der Fehler, und so weiter.

Der TYP LPD3DX ATTRIBUTE WEIGHTS wird als Zeiger auf die \_ \_ D3DX \_ ATTRIBUTE \_ WEIGHTS-Struktur definiert.


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
