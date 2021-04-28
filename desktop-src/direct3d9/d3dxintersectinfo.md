---
description: 'D3DXINTERSECTINFO-Struktur: Beschreibt eine Strahldreieck-Schnittmenge.'
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: D3DXINTERSECTINFO-Struktur (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINTERSECTINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: f4a63c7f4a479bfbe9dcb49f485ce0acb8db6486
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098288"
---
# <a name="d3dxintersectinfo-structure"></a>D3DXINTERSECTINFO-Struktur

Beschreibt eine Schnittmenge eines Strahldreiecks.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**FaceIndex**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Index des Dreiecks, das auf den Strahl trifft.

</dd> <dt>

**U**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Barycentric-Koordinate innerhalb des Dreiecks, in dem sich der Strahl überschneidet.

</dd> <dt>

**B**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Barycentric-Koordinate innerhalb des Dreiecks, in dem sich der Strahl überschneidet.

</dd> <dt>

**Dist**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Abstand entlang des Strahls, in dem die Schnittmenge aufgetreten ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks. Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
