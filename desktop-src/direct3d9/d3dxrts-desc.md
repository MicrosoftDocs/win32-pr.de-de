---
description: Beschreibt eine Renderoberfläche.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: D3DXRTS_DESC-Struktur (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 838fc7d08eff0889049e7f0c73ae779239934e49049948b926fa956eeac3d40a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607630"
---
# <a name="d3dxrts_desc-structure"></a>\_D3DXRTS-DESC-Struktur

Beschreibt eine Renderoberfläche.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Width**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite der Renderoberfläche in Pixel.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe der Renderoberfläche in Pixel.

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Member des [D3DFORMAT-Enumerationstyps,](d3dformat.md) der das Pixelformat der Renderoberfläche beschreibt.

</dd> <dt>

**Tiefenschablone**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

True gibt an, dass die Renderoberfläche eine Tiefenschablonenoberfläche unterstützt. Andernfalls wird dieser Member auf **FALSE** festgelegt.

</dd> <dt>

**DepthStencilFormat**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Wenn DepthStencil auf **TRUE** festgelegt ist, ist dieser Parameter ein Member des [D3DFORMAT-Enumerationstyps,](d3dformat.md) der das Tiefenschablonenformat der Renderoberfläche beschreibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9core.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**ID3DXRenderToSurface::GetDesc**](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
