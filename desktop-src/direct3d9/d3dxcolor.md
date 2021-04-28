---
description: 'D3DXCOLOR-Struktur (D3dx9math.h): Beschreibt Farbwerte.'
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: D3DXCOLOR-Struktur (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 58b02abc49b695169674a2579b73dc2359801a73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115928"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a>D3DXCOLOR-Struktur (D3dx9math.h)

Beschreibt Farbwerte.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a>Member

<dl> <dt>

**r**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Rote Komponente der Farbe.

</dd> <dt>

**g**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Grüne Komponente der Farbe.

</dd> <dt>

**b**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Blaue Komponente der Farbe.

</dd> <dt>

**Eine**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Alphakomponente der Farbe.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

C++-Programmierer können die Operatorüberladung und Typcasting mit den [**D3DXCOLOR-Erweiterungen**](d3dxcolor-extensions.md)nutzen, die überladene Konstruktoren sowie Zuweisungs-, unäre und binäre Operatoren (einschließlich Gleichheit) implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
