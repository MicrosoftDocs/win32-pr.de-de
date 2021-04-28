---
description: 'D3DXQUATERNION-Struktur (D3DX10Math.h): Beschreibt eine Quaternion.'
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: D3DXQUATERNION-Struktur (D3DX10Math.h)
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
ms.openlocfilehash: dac880607cf482b409c407b43992747af4aa39a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103248"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a>D3DXQUATERNION-Struktur (D3DX10Math.h)

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

**z**
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

## <a name="remarks"></a>Bemerkungen

Quaternionen fügen den \[ x-, y-, \] z-Werten, die einen Vektor definieren, ein viertes Element hinzu, was zu beliebigen 4D-Vektoren führt. Im Folgenden wird jedoch veranschaulicht, wie sich jedes Element einer Einheiten quaternion auf eine Achsenwinkelrotation bezieht (wobei q eine Einheiten quaternion (x, y, z, w) darstellt, die Achse normalisiert wird und theta die gewünschte CCW-Drehung um die Achse darstellt):


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
