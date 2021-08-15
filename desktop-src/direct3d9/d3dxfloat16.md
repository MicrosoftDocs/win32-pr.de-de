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
ms.openlocfilehash: c6f1c204dfe674a2c2db995e158891ea03ca571b00c0fc4f49f4e52884042c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526064"
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

## <a name="remarks"></a>Hinweise

C++-Programmierer können mit den [**D3DXFLOAT16-Erweiterungen**](d3dxfloat16-extensions.md)operator overloading und type casting nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre Operatoren (einschließlich Gleichheit) implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
