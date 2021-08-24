---
title: D3DX11SaveTextureToMemory-Funktion (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Hinweis Anstelle dieser Funktion wird empfohlen, die DirectXTex-Bibliothek, CaptureTexture und dann SaveToXXXMemory (wobei XXX WIC, DDS oder TGA ist) zu verwenden. WIC unterstützt DDS und TGA nicht. Von D3DX 9 unterstützte TGA als gängiges Art Source-Format für Spiele). Speichern Sie eine Textur im Arbeitsspeicher.
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- D3DX11SaveTextureToMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8459b9652701110a27efa88cf75d1bd5eb9214f72e860a5a80c18d0fa6292ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124565"
---
# <a name="d3dx11savetexturetomemory-function"></a>D3DX11SaveTextureToMemory-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, wird empfohlen, die [DirectXTex-Bibliothek,](https://github.com/Microsoft/DirectXTex) **CaptureTexture** und **dann SaveToXXXMemory** (wobei XXX WIC, DDS oder TGA ist) zu verwenden. WIC unterstützt DDS und TGA nicht. Von D3DX 9 unterstützte TGA als gängiges Art Source-Format für Spiele).

 

Speichern Sie eine Textur im Arbeitsspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* 
</dt> <dd>

Typ: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Ein Zeiger auf ein [**ID3D11DeviceContext-Objekt.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

</dd> <dt>

*pSrcTexture* \[ In\]
</dt> <dd>

Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Zeiger auf die zu speichernde Textur. Siehe [**ID3D11Ressourcen.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)

</dd> <dt>

*DestFormat* \[ In\]
</dt> <dd>

Typ: **[ **D3DX11 \_ IMAGE \_ FILE \_ FORMAT**](d3dx11-image-file-format.md)**

Das Format, in dem die Textur gespeichert wird. Siehe [**D3DX11 \_ IMAGE FILE \_ \_ FORMAT**](d3dx11-image-file-format.md).

</dd> <dt>

*ppDestBuf* \[ out\]
</dt> <dd>

Typ: **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***

Adresse eines Zeigers auf den Arbeitsspeicher, der die gespeicherte Textur enthält.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Optional.

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

 

