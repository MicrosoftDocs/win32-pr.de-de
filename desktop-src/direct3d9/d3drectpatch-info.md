---
description: Beschreibt einen rechteckigen Patch für hohe Reihenfolge.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: D3DRECTPATCH_INFO-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355204"
---
# <a name="d3drectpatch_info-structure"></a>D3DRECTPATCH \_ Info-Struktur

Beschreibt einen rechteckigen Patch für hohe Reihenfolge.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Startvertexoffsetwidth**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Vertex-Offset Breite wird als Anzahl von Vertices gestartet.

</dd> <dt>

**Startvertexoffsetheight**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Vertex-Offset Höhe wird in der Anzahl der Scheitel Punkte gestartet.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite der einzelnen Scheitel Punkte (in Anzahl der Vertices).

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Höhe der einzelnen Scheitel Punkte (in Anzahl der Vertices).

</dd> <dt>

**Schritt**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite des imaginären zweidimensionalen Scheitelpunkt Arrays, das denselben Raum einnimmt wie der Scheitelpunkt Puffer. Ein Beispiel finden Sie im folgenden Diagramm.

</dd> <dt>

**Basis**
</dt> <dd>

Typ: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Member des [**D3DBASISTYPE**](./d3dbasistype.md) -Enumerationstyps, der den Basistyp für den rechteckigen hochwertigen Patch definiert.



| Wert                 | Unterstützte Reihenfolge            | Breite und Höhe                  |
|-----------------------|----------------------------|-----------------------------------|
| D3DBASIS \_ Bezier      | Linear, kubisch und quintisch | Width = Height = (DWORD) Reihenfolge + 1 |
| D3DBASIS \_ Bspline     | Linear, kubisch und quintisch | Width = Height > Reihenfolge (DWORD)  |
| D3DBASIS \_ Interpolate | Kilometern                      | Width = Height > Reihenfolge (DWORD)  |



 

</dd> <dt>

**Grad**
</dt> <dd>

Typ: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Member des [**D3DDEGREETYPE**](./d3ddegreetype.md) -Enumerationstyps, der den Grad für den rechteckigen Patch definiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Im folgenden Diagramm werden die Parameter angegeben, die einen Rechteck Patch angeben.

![Diagramm eines rechteckigen hochwertigen Patches und der Parameter, die es angeben](images/hop-rectpatch.png)

Alle Scheitel Punkte im Scheitelpunkt Puffer werden als schwarzer Punkt angezeigt. In diesem Fall verfügt der Vertex-Puffer über 20 Vertices, von denen 16 im Rechteck Patch sind. Der Stride-Wert ist die Anzahl der Scheitel Punkte in der Breite des Scheitelpunkt Puffers (in diesem Fall fünf). Der x-Offset bis zum ersten Scheitelpunkt wird startindexvertexwidth genannt und ist in diesem Fall 1. Der y-Offset für den ersten patchvertex heißt startindexvertexheight und ist in diesem Fall 0.

Wenn Sie einen Stream einzelner rechteckiger Patches (nicht-Mosaik) rendern möchten, sollten Sie die Geometrie als lange schmale (1 x N) rechteckige Patch interpretieren. Die **D3DRECTPATCH \_ Info** -Struktur für einen solchen Strip (kubische Bézier) würde wie folgt eingerichtet werden.


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Drawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
