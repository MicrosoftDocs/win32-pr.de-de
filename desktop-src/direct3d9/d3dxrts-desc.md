---
description: Beschreibt eine Renderoberfläche.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: D3DXRTS_DESC-Struktur (D3dx9core. h)
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
ms.openlocfilehash: 3a0b52f258956f7b62734ca97cc5d1bf5ed00ac3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961593"
---
# <a name="d3dxrts_desc-structure"></a>D3DXRTS- \_ Struktur

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

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite der Renderoberfläche in Pixel.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe der Renderoberfläche in Pixel.

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Pixel Format der Renderoberfläche beschreibt.

</dd> <dt>

**Depthstencil**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

**True** gibt an, dass die Renderoberfläche eine tiefen Schablone unterstützt. Andernfalls ist dieser Member auf **false** festgelegt.

</dd> <dt>

**Depthstencilformat**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Wenn depthstencil auf **true** festgelegt ist, ist dieser Parameter ein Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das tiefen Schablone-Format der Renderoberfläche beschreibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**ID3DXRenderToSurface:: getdebug**](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
