---
description: Beschreibt einen dreieckigen Patch für hohe Reihenfolge.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: D3DTRIPATCH_INFO-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355826"
---
# <a name="d3dtripatch_info-structure"></a>D3DTRIPATCH \_ Info-Struktur

Beschreibt einen dreieckigen Patch für hohe Reihenfolge.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Startvertexoffset**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Vertex-Offset wird als Anzahl von Vertices gestartet.

</dd> <dt>

**Numvertices**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Scheitel Punkte.

</dd> <dt>

**Basis**
</dt> <dd>

Typ: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Member des [**D3DBASISTYPE**](./d3dbasistype.md) -Enumerationstyps, der den Basistyp für den dreieckigen Patch für hohe Reihenfolge definiert. Der einzige gültige Wert für diesen Member ist D3DBASIS \_ Bezier.

</dd> <dt>

**Grad**
</dt> <dd>

Typ: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Member des [**D3DDEGREETYPE**](./d3ddegreetype.md) -Enumerationstyps, der den gradtyp für den dreieckigen Patch für hohe Reihenfolge definiert.



| Wert                | Anzahl von Vertices |
|----------------------|--------------------|
| D3DDEGREE \_ kubisch     | 10                 |
| D3DDEGREE \_ linear    | 3                  |
| D3DDEGREE \_ quadratisch | –                |
| D3DDEGREE \_ Quintic   | 21                 |



 

Nicht verfügbar-nicht verfügbar. Wird nicht unterstützt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Im folgenden Diagramm werden z. b. die Scheitelpunkt Reihenfolge und die Segment Nummern für einen kubischen Bézier-Dreiecks Patch identifiziert. Die Scheitelpunkt Reihenfolge bestimmt die Segment Nummern, die von [**drawdreipatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)verwendet werden. Der Offset ist die Anzahl der Bytes für den ersten Dreiecks patchscheitel Punkt im Scheitelpunkt Puffer.

![Diagramm eines dreieckigen hochwertigen Patches mit neun Vertices](images/hop-tripatch-info.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Drawtrick Patch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
