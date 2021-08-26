---
description: Beschreibt eine Teilmenge des Gitters, die über das gleiche Attribut und die gleiche Kombination aus Kombinationen verfügt.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: D3DXBONECOMBINATION-Struktur (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 72d60b5c87d43763be4700ba7931c61c41cf0101d80390afb737c7f4afda83a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952490"
---
# <a name="d3dxbonecombination-structure"></a>D3DXBONECOMBINATION-Struktur

Beschreibt eine Teilmenge des Gitters, die über das gleiche Attribut und die gleiche Kombination aus Kombinationen verfügt.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a>Member

<dl> <dt>

**AttribId**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Attributtabellenbezeichner.

</dd> <dt>

**FaceStart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Startgesicht.

</dd> <dt>

**FaceCount**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Gesichtserkennungen.

</dd> <dt>

**VertexStart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Scheitelpunkt wird gestartet.

</dd> <dt>

**VertexCount**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Scheitelpunktanzahl.

</dd> <dt>

**OmId**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Zeiger auf ein Array von Werten, die die einzelnen Zeichner identifizieren, die in einem einzigen Zeichnungsaufruf gezeichnet werden können. Beachten Sie, dass das Array eine variable Länge haben kann, um Kombinationen von [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)mit variabler Länge aufnehmen zu können.

Die Größe des Arrays variiert je nach Typ des generierten Gitters. Eine nicht indizierte Gitternetzarraygröße entspricht der Anzahl der Gewichtungen pro Scheitelpunkt (pMaxVertexInfl in [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)). Die Größe eines indizierten Gitternetzarrays entspricht der Anzahl von Matrixpaletteneinträgen (paletteSize in [**ConvertToIndexedBlendedMesh).**](id3dxskininfo--converttoindexedblendedmesh.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Teilmenge des Gitters, die **von D3DXBONECOMBINATION** beschrieben wird, kann in einem einzigen Zeichnungsaufruf gerendert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
