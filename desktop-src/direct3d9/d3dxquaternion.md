---
description: 'D3DXQUATERNION-Struktur (D3dx9math.h): Beschreibt eine Quaternion.'
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: D3DXQUATERNION-Struktur (D3dx9math.h)
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
ms.openlocfilehash: 9818772163d5286d764c0f025b955a663457dd853c2db0efec8ad0b0a4967c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524612"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a>D3DXQUATERNION-Struktur (D3dx9math.h)

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

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die x-Komponente.

</dd> <dt>

**y**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die y-Komponente.

</dd> <dt>

**Z**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die z-Komponente.

</dd> <dt>

**w**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die w-Komponente.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Quaternionen fügen den \[ x-, y-, \] z-Werten, die einen Vektor definieren, ein viertes Element hinzu, was zu willkürlichen 4D-Vektoren führt. Im Folgenden wird jedoch veranschaulicht, wie sich jedes Element einer Einheiten quaternion auf eine Achsenwinkelrotation bezieht (wobei q eine Einheiten quaternion (x, y, z, w) darstellt, die Achse normalisiert wird und theta die gewünschte CCW-Drehung um die Achse darstellt):


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



C++-Programmierer können die Vorteile der Operatorüberladung und Typcasting mit den [**D3DXQUATERNION-Erweiterungen**](d3dxquaternion-extensions.md)nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre Operatoren (einschließlich Gleichheitsoperatoren) implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[Vektoren, Scheitelpunkte und Quaternionen (Direct3D 9)](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
