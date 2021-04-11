---
description: Beschreibt eine Quaternion.
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: D3DXQUATERNION-Struktur (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 405e48c99d7298708af193016930a8defdf9d600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355327"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a>D3DXQUATERNION-Struktur (D3DX10Math. h)

Beschreibt eine Quaternion.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a>Member

<dl> <dt>

**x**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die x-Komponente.

</dd> <dt>

**y**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die y-Komponente.

</dd> <dt>

**z**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die z-Komponente.

</dd> <dt>

**w**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die w-Komponente.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Quaternionen fügen den \[ x-, y-, z- \] Werten, die einen Vektor definieren, ein viertes Element hinzu, was zu beliebigen 4D-Vektoren führt. Im folgenden wird jedoch veranschaulicht, wie sich die einzelnen Elemente einer Einheits-Quaternion auf eine Achse-Winkel Drehung beziehen (wobei q eine Einheits Quaternion (x, y, z, w), die Achse normalisiert und die gewünschte CCW-Drehung der Achse darstellt):


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
