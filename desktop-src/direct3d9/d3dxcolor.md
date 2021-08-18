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
ms.openlocfilehash: 28f170814988317cd1cdf3300e4cbb3c2a97fa0fac7a43b2231767914a9b103a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988720"
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

## <a name="remarks"></a>Hinweise

C++-Programmierer können die Vorteile der Operatorüberladung und Typüberlegung mit den [**D3DXCOLOR-Erweiterungen**](d3dxcolor-extensions.md)nutzen, die überladene Konstruktoren sowie Zuweisungs-, unäre und binäre Operatoren (einschließlich Gleichheit) implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
