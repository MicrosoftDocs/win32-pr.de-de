---
description: Beschreibt einen dreieckigen, hochwertigen Patch.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: D3DTRIPATCH_INFO -Struktur (D3D9Types.h)
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
ms.openlocfilehash: c20a846d13cd45bb8a1629fca0e958d3042aacf148c24b0633dd19fb5462bd66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850114"
---
# <a name="d3dtripatch_info-structure"></a>D3DTRIPATCH \_ INFO-Struktur

Beschreibt einen dreieckigen, hochwertigen Patch.

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

**StartVertexOffset**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Scheitelpunktoffset wird in Anzahl von Scheitelpunkte gestartet.

</dd> <dt>

**NumVertices**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Scheitelzeichen.

</dd> <dt>

**Basis**
</dt> <dd>

Typ: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Member des [**enumerierten D3DBASISTYPE-Typs,**](./d3dbasistype.md) der den Basistyp für den dreieckigen, hohen Patch definiert. Der einzige gültige Wert für diesen Member ist D3DBASIS \_ BEZIER.

</dd> <dt>

**Grad**
</dt> <dd>

Typ: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Member des [**enumerierten D3DDEGREETYPE-Typs,**](./d3ddegreetype.md) der den Gradtyp für den triangularen Hochordnungspatch definiert.



| Wert                | Anzahl der Scheitelzeichen |
|----------------------|--------------------|
| D3DDEGREE \_ KUBISCH     | 10                 |
| D3DDEGREE \_ LINEAR    | 3                  |
| D3DDEGREE \_ QUADRATIC | Nicht zutreffend                |
| D3DDEGREEIC \_   | 21                 |



 

Nicht verfügbar. Wird nicht unterstützt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Im folgenden Diagramm werden beispielsweise die Scheitelpunkt-Reihenfolge und die Segmentnummern für einen kubischen Bézierdreieckpatch identifiziert. Die Scheitelpunkt-Reihenfolge bestimmt die Segmentnummern, die von [**DrawTriPatch verwendet werden.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) Der Offset ist die Anzahl von Bytes zum ersten Dreieckspatch-Scheitelpunkt im Scheitelpunktpuffer.

![Diagramm eines dreieckigen, hochwertigen Patches mit neun Scheitelungen](images/hop-tripatch-info.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
