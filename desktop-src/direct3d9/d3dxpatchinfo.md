---
description: -Struktur, die die Attribute eines patchnetzes enthält.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: D3DXPATCHINFO-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354146"
---
# <a name="d3dxpatchinfo-structure"></a>D3DXPATCHINFO-Struktur

-Struktur, die die Attribute eines patchnetzes enthält.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Patchtyp**
</dt> <dd>

Typ: **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**

</dd> <dd>

Der patchetyp. Weitere Informationen zu Patchtypen finden Sie unter [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).

</dd> <dt>

**Grad**
</dt> <dd>

Typ: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Grad der Kurven, die zum Erstellen des Patches verwendet werden. Informationen zu den unterstützten Graden finden Sie unter [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

**Basis**
</dt> <dd>

Typ: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Der Typ der Kurve, der zum Erstellen des Patches verwendet wurde. Informationen zu den unterstützten Basis Typen finden Sie unter [**D3DBASISTYPE**](./d3dbasistype.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Mesh ist ein Satz von Gesichtern, von denen jeder von einem einfachen Polygon beschrieben wird. Objekte können erstellt werden, indem mehrere Netze miteinander verbunden werden. Ein patchmesh wird aus Patches erstellt. Ein Patch ist ein vierseitiges Geometrie Element, das aus Kurven erstellt wurde. Der Typ der verwendeten Kurve und die Reihenfolge der Kurve können variiert werden, sodass die patchoberfläche fast alle Oberflächen Formen passt.

Die folgenden Typen von Patchkombinationen werden unterstützt:



| Patchetyp | Basis       | Grad |
|------------|-------------|--------|
| Rechteck  | Bézier      | 2, 3, 5  |
| Rechteck  | B-Spline    | 2, 3, 5  |
| Rechteck  | Catmull-Rom | 3      |
| Triangle   | Bézier      | 2, 3, 5  |
| N-Patch    | –         | 3      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DRECTPATCH \_ Info**](d3drectpatch-info.md)
</dt> <dt>

[**D3DTRIPATCH \_ Info**](d3dtripatch-info.md)
</dt> <dt>

[**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
