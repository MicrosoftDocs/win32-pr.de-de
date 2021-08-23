---
title: D3DX11FilterTexture-Funktion (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Hinweis Anstelle dieser Funktion wird empfohlen, die DirectXTex-Bibliothek, GenerateMipMaps und GenerateMipMaps3D zu verwenden. Generiert eine Mipmap-Kette mithilfe eines bestimmten Texturfilters.
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- D3DX11FilterTexture-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 728f76a28a2d97d3e6789a35c2f375d964d331c607c7570e44aa44a17ccbaa8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124695"
---
# <a name="d3dx11filtertexture-function"></a>D3DX11FilterTexture-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, wird empfohlen, die [DirectXTex-Bibliothek,](https://github.com/Microsoft/DirectXTex) **GenerateMipMaps** und **GenerateMipMaps3D zu verwenden.**

 

Generiert eine Mipmap-Kette mithilfe eines bestimmten Texturfilters.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* 
</dt> <dd>

Typ: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Ein Zeiger auf ein [**ID3D11DeviceContext-Objekt.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

</dd> <dt>

*pTexture* 
</dt> <dd>

Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Das zu filternde Texturobjekt. Siehe [**ID3D11Ressourcen.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)

</dd> <dt>

*SrcLevel* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Mipmapebene, deren Daten verwendet werden, um den Rest der Mipmapkette zu generieren.

</dd> <dt>

*MipFilter* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Flags, die steuern, wie die einzelnen miplevel-Ebenen gefiltert werden (oder D3DX11 \_ DEFAULT für D3DX11 \_ FILTER \_ LINEAR). Weitere Informationen [**finden Sie unter D3DX11 \_ FILTER \_ FLAG**](d3dx11-filter-flag.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die unter [Direct3D 11-Rückgabecodes aufgeführt sind.](d3d11-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

