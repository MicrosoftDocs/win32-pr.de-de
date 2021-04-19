---
description: Beschreibt eine Quaternion.
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: D3DXQUATERNION-Struktur (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 59d3f147e8eb233b9197394bad738d19d9ceba5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370424"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a>D3DXQUATERNION-Struktur (D3dx9math. h)

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



C++-Programmierer können das Überladen von Operatoren und die Typumwandlung mit den [**D3DXQUATERNION-Erweiterungen**](d3dxquaternion-extensions.md)nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre (einschließlich Gleichheits-) Operatoren implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[Vektoren, Vertices und Quaternionen (Direct3D 9)](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
