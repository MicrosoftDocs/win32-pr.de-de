---
description: Vertexcache-Optimierungshinweise.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: D3DDEVINFO_VCACHE-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e065c981cc42db6adbad8cfa7a14e415712aae74942e9f3aab3ecb0b353f5ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894500"
---
# <a name="d3ddevinfo_vcache-structure"></a>\_D3DDEVINFO-VCACHE-Struktur

Vertexcache-Optimierungshinweise.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a>Member

<dl> <dt>

**Muster**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Bitmuster. Der Rückgabewert muss FOURCC ('C', 'A', 'C', 'H') sein.

</dd> <dt>

**OptMethod**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Optimierungsmethode. Verwenden Sie 0, um die längsten Strips abzurufen. Verwenden Sie 1, um die Verwendung des Scheitelpunktcaches zu optimieren.

</dd> <dt>

**CacheSize**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Cachegröße, die als Ziel für die Optimierung verwendet wird. Dies ist nur erforderlich, wenn OptMethod 1 ist.

</dd> <dt>

**MagicNumber**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Wird von internen Optimierungsmethoden verwendet, um zu bestimmen, wann Strips neu gestartet werden sollen. Dies kann nicht von einem Benutzer festgelegt oder geändert werden. Dies ist nur erforderlich, wenn OptMethod 1 ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
