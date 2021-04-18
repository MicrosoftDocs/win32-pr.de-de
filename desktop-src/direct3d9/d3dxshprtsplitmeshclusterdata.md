---
description: D3DXSHPRTSPLITMESHCLUSTERDATA-Struktur
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: D3DXSHPRTSPLITMESHCLUSTERDATA-Struktur (D3dx9mesh. h)
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
ms.openlocfilehash: e7b1bc23606dbf08f5a924860e12c9c09d719287
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365080"
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

**uvertstart**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ursprünglicher Scheitelpunkt in neu zugeordnete Scheitelpunkt Arrays.

</dd> <dt>

**uvertlength**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Scheitel Punkte in diesem Supercluster.

</dd> <dt>

**ufakestart**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ursprünglicher Index in Flächen Array.

</dd> <dt>

**ufakelength**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Gesichter in diesem Supercluster.

</dd> <dt>

**uclusterstart**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ursprünglicher Index in Cluster Array.

</dd> <dt>

**uclusterlength**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Cluster in diesem Supercluster-Array.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 
