---
title: D3DX11_TEXTURE_LOAD_INFO -Struktur (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Beschreibt Parameter, die zum Laden einer Textur aus einer anderen Textur verwendet werden.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- D3DX11_TEXTURE_LOAD_INFO-Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b441ed81e7054cb84731f204ddbf2a863b7a98a75e5e01ed54cf49b28dba7957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989900"
---
# <a name="d3dx11_texture_load_info-structure"></a>Struktur "D3DX11 \_ TEXTURE \_ LOAD \_ INFO"

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Beschreibt Parameter, die zum Laden einer Textur aus einer anderen Textur verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**pSrcBox**
</dt> <dd>

Typ: **[ **D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Quelltexturfeld (siehe [**D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**pDstBox**
</dt> <dd>

Typ: **[ **D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Zieltexturfeld (siehe [**D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Mipmapebene der Quelltextur finden Sie [**unter D3D11CalcSubresource.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource)

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Mipmapebene der Zieltextur finden Sie unter [**D3D11CalcSubresource.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource)

</dd> <dt>

**NumMips**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Mipmapebenen in der Quelltextur.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Erstes Element der Quelltextur.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Erstes Element der Zieltextur.

</dd> <dt>

**NumElements**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der zu ladenden Elemente.

</dd> <dt>

**Filter**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filteroptionen während des Resamplings (siehe [**D3DX11 \_ FILTER \_ FLAG**](d3dx11-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filteroptionen beim Generieren von MIP-Ebenen (siehe [**D3DX11 \_ FILTER \_ FLAG**](d3dx11-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird in einem Aufruf von [**D3DX11LoadTextureFromTexture verwendet.**](d3dx11loadtexturefromtexture.md)

Die Standardwerte lauten wie folgt:


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

