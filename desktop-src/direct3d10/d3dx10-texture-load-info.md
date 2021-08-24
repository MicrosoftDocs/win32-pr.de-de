---
description: Beschreibt Parameter, die zum Laden einer Textur aus einer anderen Textur verwendet werden.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: D3DX10_TEXTURE_LOAD_INFO -Struktur (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 144475b4b4967ff0a1fd130a658b8276af5d8897cc043000d150417aa01b227e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753470"
---
# <a name="d3dx10_texture_load_info-structure"></a>Struktur "D3DX10 \_ TEXTURE \_ LOAD \_ INFO"

Beschreibt Parameter, die zum Laden einer Textur aus einer anderen Textur verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**pSrcBox**
</dt> <dd>

Typ: **[ **D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Quelltexturfeld (siehe [**D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**pDstBox**
</dt> <dd>

Typ: **[ **D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Zieltexturfeld (siehe [**D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Mipmapebene der Quelltextur finden Sie unter [**D3D10CalcSubresource.**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource)

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Mipmapebene der Zieltextur finden Sie unter [**D3D10CalcSubresource.**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource)

</dd> <dt>

**NumMips**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Mipmapebenen in der Quelltextur.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Erstes Element der Quelltextur.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Erstes Element der Zieltextur.

</dd> <dt>

**NumElements**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der zu ladenden Elemente.

</dd> <dt>

**Filter**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Filteroptionen während des Resamplings (siehe [**D3DX10 \_ FILTER \_ FLAG**](d3dx10-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Filteroptionen beim Generieren von MIP-Ebenen (siehe [**D3DX10 \_ FILTER \_ FLAG**](d3dx10-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird in einem Aufruf von [**D3DX10LoadTextureFromTexture verwendet.**](d3dx10loadtexturefromtexture.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
