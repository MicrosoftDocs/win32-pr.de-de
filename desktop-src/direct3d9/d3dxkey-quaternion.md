---
description: Beschreibt einen Quaternion-Schlüssel zur Verwendung in der Keyframe-Animation. Ein Quaternion-Schlüssel ist ein Quaternion-Wert zu einem bestimmten Zeitpunkt.
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: D3DXKEY_QUATERNION-Struktur (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354807"
---
# <a name="d3dxkey_quaternion-structure"></a>D3DXKEY \_ Quaternion-Struktur

Beschreibt einen Quaternion-Schlüssel zur Verwendung in der Keyframe-Animation. Ein Quaternion-Schlüssel ist ein Quaternion-Wert zu einem bestimmten Zeitpunkt.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a>Member

<dl> <dt>

**Time**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeitwert.

</dd> <dt>

**Wert**
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)**

</dd> <dd>

[**D3DXQUATERNION**](d3dxquaternion.md) Quaternion, das Rotations Werte bereitstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
