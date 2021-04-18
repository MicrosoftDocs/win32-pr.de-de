---
description: Beschreibt eine Ebene.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: D3DXPLANE-Struktur (D3dx9math. h)
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
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354982"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a>D3DXPLANE-Struktur (D3dx9math. h)

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

**ein**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene. Siehe Hinweise.

</dd> <dt>

**b**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der b-Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene. Siehe Hinweise.

</dd> <dt>

**c**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der c-Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene. Siehe Hinweise.

</dd> <dt>

**d**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der d-Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene. Siehe Hinweise.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Member der **D3DXPLANE** -Struktur haben die Form der allgemeinen ebenengleichung. Sie passen in die Gleichung der allgemeinen Ebene an, sodass **ein** x + **b** y + **c** z + **d** w = 0 ist.

C++-Programmierer können den Vorteil von Operator Überladungen und Typumwandlungen mit den [**D3DXPLANE-Erweiterungen**](d3dxplane-extensions.md) nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre (einschließlich Gleichheits-) Operatoren implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
