---
description: Statistiken zur Ressourcenverwendung.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: D3DDEVINFO_ResourceManager-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_ResourceManager
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bf4e84fa247ca5b2603547efef73ea6b9cbe0aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761967"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a>D3DDEVINFO \_ ResourceManager-Struktur

Statistiken zur Ressourcenverwendung.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DDEVINFO_ResourceManager {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_ResourceManager, *LPD3DDEVINFO_ResourceManager;
```



## <a name="members"></a>Member

<dl> <dt>

**stats**
</dt> <dd>

Typ: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**

</dd> <dd>

Array von Ressourcen Statistik Elementen. Siehe [**D3DRESOURCESTATS**](d3dresourcestats.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

D3DRTYPECOUNT bezieht sich auf die Anzahl von Enumerationen in [**D3DRESOURCETYPE**](./d3dresourcetype.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
