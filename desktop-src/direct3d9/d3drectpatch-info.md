---
description: Beschreibt einen rechteckigen, hochwertigen Patch.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: D3DRECTPATCH_INFO-Struktur (D3D9Types.h)
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
ms.openlocfilehash: b73ebc548031fd931cce0d34edfadf81a73d71d60edf649718875c52cfc992f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850225"
---
# <a name="d3drectpatch_info-structure"></a>D3DRECTPATCH \_ INFO-Struktur

Beschreibt einen rechteckigen, hochwertigen Patch.

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

**StartVertexOffsetWidth**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Beginnende Scheitelpunktoffsetbreite in Anzahl der Scheitelpunkte.

</dd> <dt>

**StartVertexOffsetHeight**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anfangshöhe des Scheitelpunktoffsets in Anzahl der Scheitelpunkte.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite der einzelnen Scheitelpunkte in Anzahl der Scheitelpunkte.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe jedes Scheitelpunkts in Anzahl der Scheitelpunkte.

</dd> <dt>

**Schritt**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite des imaginären zweidimensionalen Vertexarrays, das denselben Raum wie der Scheitelpunktpuffer einnimmt. Ein Beispiel finden Sie im folgenden Diagramm.

</dd> <dt>

**Basis**
</dt> <dd>

Typ: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Member des [**aufzählten D3DBASISTYPE-Typs,**](./d3dbasistype.md) der den Basistyp für den rechteckigen, hochwertigen Patch definiert.



| Wert                 | Auftrag unterstützt            | Breite und Höhe                  |
|-----------------------|----------------------------|-----------------------------------|
| D3DBASIS \_ BEZIER      | Linear, kubisch undic | Width = height = (DWORD)order + 1 |
| D3DBASIS \_ BSPLINE     | Linear, kubisch undic | Width = height > (DWORD)order  |
| D3DBASIS \_ INTERPOLATE | Kubische                      | Width = height > (DWORD)order  |



 

</dd> <dt>

**Grad**
</dt> <dd>

Typ: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Member des [**aufzählten D3DDEGREETYPE-Typs,**](./d3ddegreetype.md) der den Grad für den rechteckigen Patch definiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das folgende Diagramm identifiziert die Parameter, die einen Rechteckpatch angeben.

![Diagramm eines rechteckigen, hochwertigen Patches und der Parameter, die ihn angeben](images/hop-rectpatch.png)

Jeder Scheitelpunkt im Scheitelpunktpuffer wird als schwarzer Punkt angezeigt. In diesem Fall enthält der Scheitelpunktpuffer 20 Scheitelpunkte, von denen sich 16 im Rechteckpatch befinden. Der Schritt ist die Anzahl der Scheitelpunkte in der Breite des Scheitelpunktpuffers, in diesem Fall fünf. Der x-Offset zum ersten Scheitelpunkt wird startIndexVertexWidth genannt und ist in diesem Fall 1. Der y-Offset zum ersten Patchvertex wird als StartIndexVertexHeight bezeichnet und ist in diesem Fall 0.

Zum Rendern eines Streams einzelner rechteckiger Patches (nicht-ung) sollten Sie Ihre Geometrie als langen schmalen (1 x N) rechteckigen Patch interpretieren. Die **D3DRECTPATCH \_ INFO-Struktur** für einen solchen Strip (kubischer Bézier) wird wie folgt eingerichtet.


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
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
