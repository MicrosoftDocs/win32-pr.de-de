---
description: D3DXSHPRTSPLITMESHCLUSTERDATA-Struktur
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: D3DXSHPRTSPLITMESHCLUSTERDATA-Struktur (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHCLUSTERDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: c4405b383e0403326c3cb84f43c97f4c7da826872b62cb21c94b3edb9ef0e475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298289"
---
# <a name="d3dxshprtsplitmeshclusterdata-structure"></a>D3DXSHPRTSPLITMESHCLUSTERDATA-Struktur

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXSHPRTSPLITMESHCLUSTERDATA {
  UINT uVertStart;
  UINT uVertLength;
  UINT uFaceStart;
  UINT uFaceLength;
  UINT uClusterStart;
  UINT uClusterLength;
} D3DXSHPRTSPLITMESHCLUSTERDATA, *LPD3DXSHPRTSPLITMESHCLUSTERDATA;
```



## <a name="members"></a>Member

<dl> <dt>

**uVertStart**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Erster Scheitelpunkt in neu zugeordnetes Vertexarray.

</dd> <dt>

**uVertLength**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Scheitelzeichen in diesem Supercluster.

</dd> <dt>

**uFaceStart**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anfänglicher Index im Gesichtsarray.

</dd> <dt>

**uFaceLength**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Gesichter in diesem Supercluster.

</dd> <dt>

**uClusterStart**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Erster Index im Clusterarray.

</dd> <dt>

**uClusterLength**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Cluster in diesem Superclusterarray.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 
