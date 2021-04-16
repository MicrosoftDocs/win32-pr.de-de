---
description: Beschreibt einen Scheitelpunkt Puffer.
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: D3DVERTEXBUFFER_DESC-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b2c0838743f8190eeb0e5c825e7125d2e48c0b6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530986"
---
# <a name="d3dvertexbuffer_desc-structure"></a>D3DVERTEXBUFFER- \_ Struktur

Beschreibt einen Scheitelpunkt Puffer.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Oberflächen Format der Vertex-Puffer Daten beschreibt.

</dd> <dt>

**Type**
</dt> <dd>

Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Member des [**D3DRESOURCETYPE**](./d3dresourcetype.md) -Enumerationstyps, der diese Ressource als Vertex-Puffer identifiziert.

</dd> <dt>

**Verwendung**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kombination von mindestens einem [**D3DUSAGE**](d3dusage.md) -Flags.

</dd> <dt>

**Pool**
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die für diesen Vertex-Puffer zugeordnete Arbeitsspeicher Klasse angibt.

</dd> <dt>

**Größe**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe des Scheitelpunkt Puffers in Bytes.

</dd> <dt>

**F-VF**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Eine Kombination aus [D3DFVF](d3dfvf.md) , die das Scheitelpunkt Format der Scheitel Punkte in diesem Puffer beschreibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[Vertex-Puffer (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 
