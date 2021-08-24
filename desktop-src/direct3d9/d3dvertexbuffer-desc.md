---
description: Beschreibt einen Scheitelpunktpuffer.
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: D3DVERTEXBUFFER_DESC-Struktur (D3D9Types.h)
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
ms.openlocfilehash: 1f1809bbf9352b022d2acfb15b119db47b0feab6302020cdaf5b24746945aa05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750580"
---
# <a name="d3dvertexbuffer_desc-structure"></a>\_D3DVERTEXBUFFER-DESC-Struktur

Beschreibt einen Scheitelpunktpuffer.

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

Member des [D3DFORMAT-Enumerationstyps,](d3dformat.md) der das Oberflächenformat der Vertexpufferdaten beschreibt.

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Member des [**D3DRESOURCETYPE-Enumerationstyps,**](./d3dresourcetype.md) der diese Ressource als Scheitelpunktpuffer identifiziert.

</dd> <dt>

**Verwendung**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kombination aus einem oder mehreren [**D3DUSAGE-Flags.**](d3dusage.md)

</dd> <dt>

**Pool**
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Member des [**D3DPOOL-Enumerationstyps,**](./d3dpool.md) der die Für diesen Scheitelpunktpuffer zugeordnete Speicherklasse angibt.

</dd> <dt>

**Größe**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe des Scheitelpunktpuffers in Bytes.

</dd> <dt>

**FVF**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kombination aus [D3DFVF,](d3dfvf.md) die das Scheitelpunktformat der Scheitelpunkte in diesem Puffer beschreibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[Vertexpuffer (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 
