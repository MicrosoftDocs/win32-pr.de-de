---
description: Beschreibt eine Teilmenge des Netzes, das über das gleiche Attribut und die gleiche Kombination aus dem gleichen Knoten verfügt.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: D3DXBONECOMBINATION-Struktur (D3dx9mesh. h)
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
ms.openlocfilehash: 3553ba37d0d9376fa5912143fb58849f03c5a83a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050873"
---
# <a name="d3dxbonecombination-structure"></a>D3DXBONECOMBINATION-Struktur

Beschreibt eine Teilmenge des Netzes, das über das gleiche Attribut und die gleiche Kombination aus dem gleichen Knoten verfügt.

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

**Atungbid**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Attribut Tabellen Bezeichner.

</dd> <dt>

**Fakestart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Startseite.

</dd> <dt>

**FaceCount**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Gesichter.

</dd> <dt>

**VertexStart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Scheitelpunkt wird gestartet.

</dd> <dt>

**VertexCount**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Vertex-Anzahl.

</dd> <dt>

**Boneid**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Ein Zeiger auf ein Array von Werten, die jeden der Knochen identifizieren, die in einem einzelnen Zeichnungs Befehl gezeichnet werden können. Beachten Sie, dass das Array eine Variable Länge aufweisen kann, um die Kombination der Variablen mit variabler Länge von [**convertumindexedblendedmesh**](id3dxskininfo--converttoindexedblendedmesh.md)zu unterstützen.

Die Größe des Arrays variiert je nach Typ des generierten Diagrammtyps. Eine nicht indizierte Gitter Array Größe ist gleich der Anzahl der Gewichtungen pro Scheitelpunkt (pmaxvertexinfl in [**convertumblendedmesh**](id3dxskininfo--converttoblendedmesh.md)). Die Größe eines indizierten Mesh-Arrays entspricht der Anzahl der Einträge in der Band Matrix Palette (palettesize in [**convertumindexedblendedmesh**](id3dxskininfo--converttoindexedblendedmesh.md)).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Teilmenge des von **D3DXBONECOMBINATION** beschriebenen Netzes kann in einem einzelnen Zeichnungs Befehl gerendert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
