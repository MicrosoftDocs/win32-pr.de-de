---
description: Beschreibt einen 16-Bit-Gleit Komma Vektor.
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: D3DXFLOAT16-Struktur (D3dx9math. h)
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
ms.openlocfilehash: 4b469c770b811ed11ec21b21d2b449df1fd75b1c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355189"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a>D3DXFLOAT16-Struktur (D3dx9math. h)

Beschreibt einen 16-Bit-Gleit Komma Vektor.

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

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Die 16-Bit-Daten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

C++-Programmierer können das Überladen von Operatoren und die Typumwandlung mit den [**D3DXFLOAT16-Erweiterungen**](d3dxfloat16-extensions.md)nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre (einschließlich Gleichheits-) Operatoren implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
