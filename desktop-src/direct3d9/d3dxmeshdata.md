---
description: Mesh-Datenstruktur.
ms.assetid: 9164b956-95b7-4bc0-bf7e-feed2e3b4a2b
title: D3DXMESHDATA-Struktur (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATA
api_type:
- HeaderDef
api_location:
- D3dx9anim.h
ms.openlocfilehash: 785284ba1330c957813a099eb6cf1c74521d3c90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354176"
---
# <a name="d3dxmeshdata-structure"></a>D3DXMESHDATA-Struktur

Mesh-Datenstruktur.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a>Member

<dl> <dt>

**Type**
</dt> <dd>

Typ: **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**

</dd> <dd>

Definiert den Mesh-Datentyp. Siehe [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).

</dd> <dt>

**pmesh**
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

</dd> <dd>

Zeiger auf ein Mesh. Siehe [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

**ppatchmesh**
</dt> <dd>

Typ: **LPD3DXPATCHMESH**

</dd> <dd>

Zeiger auf ein patchmesh. Siehe [**ID3DXPatchMesh**](id3dxpatchmesh.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)
</dt> </dl>

 

 
