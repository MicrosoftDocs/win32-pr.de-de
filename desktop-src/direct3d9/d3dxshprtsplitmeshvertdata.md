---
description: D3DXSHPRTSPLITMESHVERTDATA-Struktur
ms.assetid: 8799a680-bf5f-42cc-91aa-1a6aed164ca5
title: D3DXSHPRTSPLITMESHVERTDATA-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHVERTDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 55424929a3d415fc1b89f7a1af53be849cf90185
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762024"
---
# <a name="d3dxshprtsplitmeshvertdata-structure"></a>D3DXSHPRTSPLITMESHVERTDATA-Struktur

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXSHPRTSPLITMESHVERTDATA {
  UINT uVertRemap;
  UINT uSubCluster;
  UINT ucVertStatus;
} D3DXSHPRTSPLITMESHVERTDATA, *LPD3DXSHPRTSPLITMESHVERTDATA;
```



## <a name="members"></a>Member

<dl> <dt>

**uvertremap**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Scheitelpunkt im ursprünglichen Mesh, dies entspricht.

</dd> <dt>

**usubcluster**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Cluster Index relativ zum Supercluster.

</dd> <dt>

**ucvertstatus**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

1, wenn der Scheitelpunkt gültige Daten aufweist, 0 (null), wenn er "Full" ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md)zugeordnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
