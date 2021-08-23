---
description: 'D3DX10_ATTRIBUTE_WEIGHTS Struktur: Gibt Gitternetzgewichtungsattribute an.'
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: D3DX10_ATTRIBUTE_WEIGHTS -Struktur (D3DX10.h)
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
ms.openlocfilehash: 1ef80db70d0562b000aa527afe17da43eee0eed5d6498e5da5b3d1ad964f5f87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282780"
---
# <a name="d3dx10_attribute_weights-structure"></a>D3DX10 \_ ATTRIBUTE \_ WEIGHTS-Struktur

Gibt Gittergewichtungsattribute an.

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

Specular-Beleuchtungswert.

</dd> <dt>

**Texcoord**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Acht Texturkoordinaten.

</dd> <dt>

**Tangens**
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

## <a name="remarks"></a>Hinweise

Diese Struktur beschreibt, wie bei einem Vereinfachungsvorgang Scheitelpunktdaten berücksichtigt werden, wenn relative Kosten zwischen reduzierenden Kanten berechnet werden. Wenn das Feld Normal beispielsweise 0,0 ist, ignoriert der Vereinfachungsvorgang die normale Scheitelpunktkomponente, wenn der Fehler für den Reduzieren berechnet wird. Wenn das Feld Normal jedoch 1,0 ist, verwendet der Vereinfachungsvorgang die Scheitelpunkt-Normalkomponente. Wenn das Feld Normal 2.0 ist, doppelt so viele Fehler Wenn das Feld Normal 4.0 ist, ver vierfachen Sie die Anzahl der Fehler, und so weiter.

Der TYP LPD3DX ATTRIBUTE WEIGHTS wird als Zeiger auf die \_ \_ D3DX \_ ATTRIBUTE \_ WEIGHTS-Struktur definiert.


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
