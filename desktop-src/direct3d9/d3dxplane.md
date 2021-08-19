---
description: 'D3DXPLANE-Struktur (D3dx9math.h): Beschreibt eine Ebene.'
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: D3DXPLANE-Struktur (D3dx9math.h)
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
- d3dx9math.h
ms.openlocfilehash: 5fa7e7155cdcf5c5dc1996dee1dcf02d0190e4bb91b4c319231e2f03168722c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095458"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a>D3DXPLANE-Struktur (D3dx9math.h)

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

Die Elemente der **D3DXPLANE-Struktur** haben die Form der allgemeinen Ebenengleichung. Sie passen in die allgemeine Ebenengleichung, sodass **ein** x + **b** y + **c** z + **d** w = 0 ist.

C++-Programmierer können mit den [**D3DXPLANE-Erweiterungen**](d3dxplane-extensions.md) die Operatorüberladung und Typüberladung nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre Operatoren (einschließlich Gleichheitsoperatoren) implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
