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
ms.openlocfilehash: be04aa9345f8a5b932d1697dbd85c8f81072bd3087077163d4891b1c19aafbe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991160"
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

Die w--Komponente.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Quaternionen fügen den \[ x-, y-, z-Werten, die einen Vektor definieren, ein viertes Element hinzu, was zu \] beliebigen 4D-Vektoren führt. Im Folgenden wird jedoch veranschaulicht, wie sich jedes Element einer Einheiten quaternion auf eine Achsenwinkelrotation bezieht (wobei q eine Einheiten quaternion (x, y, z, w), die Achse normalisiert wird und theta die gewünschte CCW-Drehung um die Achse darstellt):


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
