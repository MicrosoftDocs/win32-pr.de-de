---
description: 'D3DXATTRIBUTEWEIGHTS-Struktur: Gibt Meshgewichtungsattribute an.'
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: D3DXATTRIBUTEWEIGHTS-Struktur (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7a833d2a58db0f434f836126926e461cd2ee3ea0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115968"
---
# <a name="d3dxattributeweights-structure"></a>D3DXATTRIBUTEWEIGHTS-Struktur

Gibt Gitternetzgewichtungsattribute an.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
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

Diese Struktur beschreibt, wie bei einem Vereinfachungsvorgang Scheitelpunktdaten berücksichtigt werden, wenn relative Kosten zwischen reduzierenden Kanten berechnet werden. Wenn das Feld Normal z. B. 0,0 ist, ignoriert der Vereinfachungsvorgang die Vertexnorm normal-Komponente beim Berechnen des Fehlers für das Reduzieren. Wenn das Feld Normal jedoch 1,0 ist, verwendet der Vereinfachungsvorgang die Vertex normal-Komponente. Wenn das Feld Normal 2,0 ist, doppelt so viele Fehler. , wenn das Feld Normal den Wert 4,0 aufweist, verdreiffachen Sie die Anzahl der Fehler usw.

Der LPD3DXATTRIBUTEWEIGHTS-Typ wird als Zeiger auf die **D3DXATTRIBUTEWEIGHTS-Struktur** definiert.


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 
