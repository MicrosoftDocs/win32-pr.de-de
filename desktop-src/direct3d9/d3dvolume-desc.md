---
description: Beschreibt ein Volume.
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: D3DVOLUME_DESC -Struktur (D3D9Types.h)
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
ms.openlocfilehash: 1ddf80819818bf23985c5ca81e2d26e80b51662388ec5808579c74146c152ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300178"
---
# <a name="d3dvolume_desc-structure"></a>D3DVOLUME \_ DESC-Struktur

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

Member des [aufzählten D3DFORMAT-Typs,](d3dformat.md) der das Oberflächenformat des Volumes beschreibt.

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Member des [**aufzählten D3DRESOURCETYPE-Typs,**](./d3dresourcetype.md) der diese Ressource als Volume identifiziert.

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

Member des [**enumerierten D3DPOOL-Typs,**](./d3dpool.md) der die Klasse des für dieses Volume zugeordneten Arbeitsspeichers an gibt.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite des Volumes in Pixel.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe des Volumes in Pixel.

</dd> <dt>

**Tiefe**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tiefe des Volumes in Pixel.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 
