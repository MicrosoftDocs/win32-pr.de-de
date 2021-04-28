---
description: 'D3DXFLOAT16-Struktur (D3dx9math.h): Beschreibt einen 16-Bit-Gleitkommavektor.'
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: D3DXFLOAT16-Struktur (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: dc878575de4338a2a399f329362d79ff2e7654f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094268"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a>D3DXFLOAT16-Struktur (D3dx9math.h)

Beschreibt einen 16-Bit-Gleitkommavektor.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a>Member

<dl> <dt>

**Wert**
</dt> <dd>

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Die 16-Bit-Daten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

C++-Programmierer können die Vorteile der Operatorüberladung und Typcasting mit den [**D3DXFLOAT16-Erweiterungen**](d3dxfloat16-extensions.md)nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre Operatoren (einschließlich Gleichheitsoperatoren) implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
