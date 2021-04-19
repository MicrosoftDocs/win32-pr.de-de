---
description: Vertex-Cache Optimierungs Hinweise.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: D3DDEVINFO_VCACHE-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 80870c330adf185a869ac5e3543055c82fc7115c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367357"
---
# <a name="d3ddevinfo_vcache-structure"></a>D3DDEVINFO \_ VCACHE-Struktur

Vertex-Cache Optimierungs Hinweise.

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

Bitmuster. Der Rückgabewert muss "FourCC" ("c", "A", "c", "H") sein.

</dd> <dt>

**Optmethod**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Optimierungsmethode. Verwenden Sie 0, um die längsten Striche zu erhalten. Verwenden Sie 1, um die Vertex-Cache Verwendung zu optimieren.

</dd> <dt>

**CacheSize**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Cache Größe, die als Ziel für die Optimierung verwendet wird. Dies ist nur erforderlich, wenn optmethod den Wert 1 hat.

</dd> <dt>

**MagicNumber**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Wird von internen Optimierungsmethoden verwendet, um zu bestimmen, wann Striche neu gestartet werden sollen. Dies kann von einem Benutzer nicht festgelegt oder geändert werden. Dies ist nur erforderlich, wenn optmethod den Wert 1 hat.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
