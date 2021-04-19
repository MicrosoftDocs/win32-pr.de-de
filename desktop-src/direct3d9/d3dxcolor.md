---
description: Beschreibt Farbwerte.
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: D3DXCOLOR-Struktur (D3dx9math. h)
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
ms.openlocfilehash: c7e5c1ac12341ccf6272714511959ee9a131ba4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350693"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a>D3DXCOLOR-Struktur (D3dx9math. h)

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

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Rote Komponente der Farbe.

</dd> <dt>

**g**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Grüne Komponente der Farbe.

</dd> <dt>

**b**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Blaue Komponente der Farbe.

</dd> <dt>

**ein**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Alpha Komponente der Farbe.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

C++-Programmierer können das Überladen von Operatoren und die Typumwandlung mit den [**D3DXCOLOR-Erweiterungen**](d3dxcolor-extensions.md)nutzen, die überladene Konstruktoren implementieren, sowie Zuweisungs-, unäre und binäre (einschließlich Gleichheits-) Operatoren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
