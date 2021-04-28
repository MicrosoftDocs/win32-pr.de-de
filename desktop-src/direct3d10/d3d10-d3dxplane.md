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
ms.openlocfilehash: 440246fb47a851f9f5339c72a484a2cb59e8f662
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103328"
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

## <a name="remarks"></a>Bemerkungen

Die Elemente der **D3DXPLANE-Struktur** haben die Form der allgemeinen Ebenengleichung. Sie passen in die allgemeine Ebenengleichung, sodass ax + by + alle + dw = 0 ist.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
