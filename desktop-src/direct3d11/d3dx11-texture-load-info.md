---
title: D3DX11_TEXTURE_LOAD_INFO-Struktur (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beschreibt Parameter, mit denen eine Textur aus einer anderen Textur geladen wird.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- D3DX11_TEXTURE_LOAD_INFO Struktur Direct3D 11
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
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996058"
---
# <a name="d3dx11_texture_load_info-structure"></a>Bibliothek d3dx11 \_ Textur \_ Lade- \_ Informationsstruktur

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Beschreibt Parameter, mit denen eine Textur aus einer anderen Textur geladen wird.

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

**psrcbox**
</dt> <dd>

Typ: **[ **D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Quell Textur Feld (siehe [**D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**pdstbox**
</dt> <dd>

Typ: **[ **D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Ziel Textur Feld (siehe [**D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**Srcfirstmip**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

MipMap-Ebene der Quell Textur. Weitere Informationen finden Sie unter [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) .

</dd> <dt>

**Dstfirstmip**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die MipMap-Ebene der Ziel Textur. weitere Details finden Sie unter [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) .

</dd> <dt>

**Nummips**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl von MipMap-Ebenen in der Quell Textur.

</dd> <dt>

**Srcfirstelement**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Erstes Element der Quell Textur.

</dd> <dt>

**Dstfirstelement**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Erstes Element der Ziel Textur.

</dd> <dt>

**NumElements**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der zu ladenden Elemente.

</dd> <dt>

**Filter**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filteroptionen während der erneuten Stichprobenentnahme (siehe [**Bibliothek d3dx11 \_ Filter \_ Flag**](d3dx11-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filteroptionen beim Erzeugen von Mip-Ebenen (siehe [**Bibliothek d3dx11 \_ Filter \_ Flag**](d3dx11-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in einem [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md)-aufrufswert verwendet.

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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

