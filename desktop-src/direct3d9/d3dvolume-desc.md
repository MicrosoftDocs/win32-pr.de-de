---
description: Beschreibt ein Volume.
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: D3DVOLUME_DESC-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b736333cefcfc8a3307ff7a0cecd53cd96bc0af2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355187"
---
# <a name="d3dvolume_desc-structure"></a>D3DVOLUME- \_ Struktur

Beschreibt ein Volume.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Oberflächen Format des Volumes beschreibt.

</dd> <dt>

**Type**
</dt> <dd>

Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Member des [**D3DRESOURCETYPE**](./d3dresourcetype.md) -Enumerationstyps, der diese Ressource als Volume identifiziert.

</dd> <dt>

**Verwendung**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Derzeit nicht verwendet. Wird immer als 0 zurückgegeben.

</dd> <dt>

**Pool**
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die für dieses Volume zugewiesene Arbeitsspeicher Klasse angibt.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite des Volumes in Pixel.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe des Volumes in Pixel.

</dd> <dt>

**Tiefe**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Tiefe des Volumes in Pixel.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[**Getleveldebug**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 
