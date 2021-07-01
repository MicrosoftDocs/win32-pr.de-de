---
description: Statistiken zur Ressourcennutzung.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: D3DDEVINFO_RESOURCEMANAGER-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_RESOURCEMANAGER
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b0a9fc461564280e4e36dde6bf73e68a78cf1609
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129979"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a>D3DDEVINFO \_ RESOURCEMANAGER-Struktur

Statistiken zur Ressourcennutzung.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DDEVINFO_RESOURCEMANAGER {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_RESOURCEMANAGER, *LPD3DDEVINFO_RESOURCEMANAGER;

```



## <a name="members"></a>Member

<dl> <dt>

**stats**
</dt> <dd>

Typ: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**

</dd> <dd>

Array von Ressourcenstatistikelementen. Siehe [**D3DRESOURCESTATS.**](d3dresourcestats.md)

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

D3DRTYPECOUNT bezieht sich auf die Anzahl der Enumerationen in [**D3DRESOURCETYPE.**](./d3dresourcetype.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
