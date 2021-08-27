---
description: Beschreibt einen Vektorschlüssel für die Verwendung in der Keyframe-Animation. Sie gibt einen Vektor zu einem bestimmten Zeitpunkt an. Dies wird für Skalierungs- und Übersetzungsschlüssel verwendet.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: D3DXKEY_VECTOR3-Struktur (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0214582b3fb1267caeb30a6cca905cbf7243ecf5dd1af40365841b315359317f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119180"
---
# <a name="d3dxkey_vector3-structure"></a>D3DXKEY \_ VECTOR3-Struktur

Beschreibt einen Vektorschlüssel für die Verwendung in der Keyframe-Animation. Sie gibt einen Vektor zu einem bestimmten Zeitpunkt an. Dies wird für Skalierungs- und Übersetzungsschlüssel verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a>Member

<dl> <dt>

**Time**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Keyframe-Zeitstempel.

</dd> <dt>

**Wert**
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)**

</dd> <dd>

[**D3DXVECTOR3-**](d3dxvector3.md) 3D-Vektor, der Skalierungs- und/oder Übersetzungswerte liefert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
