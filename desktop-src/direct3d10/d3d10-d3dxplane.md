---
description: 'D3DXPLANE-Struktur (D3DX10Math.h): Beschreibt eine Ebene.'
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: D3DXPLANE-Struktur (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ccdc8644f63bdb048f6caa97ef635165a11a4473f549214410558583c8f807c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754260"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a>D3DXPLANE-Struktur (D3DX10Math.h)

Beschreibt eine Ebene.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a>Member

<dl> <dt>

**Eine**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Koeffizient der Clippingebene in der allgemeinen Ebenengleichung. Siehe Hinweise.

</dd> <dt>

**b**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Der b-Koeffizient der Clippingebene in der allgemeinen Ebenengleichung. Siehe Hinweise.

</dd> <dt>

**c**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Der c-Koeffizient der Clippingebene in der allgemeinen Ebenengleichung. Siehe Hinweise.

</dd> <dt>

**d**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Der d-Koeffizient der Clippingebene in der allgemeinen Ebenengleichung. Siehe Hinweise.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Elemente der **D3DXPLANE-Struktur** haben die Form der allgemeinen Ebenengleichung. Sie passen in die allgemeine Ebenengleichung, sodass ax + by + alle + dw = 0 ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
