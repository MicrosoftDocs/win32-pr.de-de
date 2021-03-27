---
title: D3DX11SaveTextureToFile-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie anstelle dieser Funktion, dass Sie die directxtex-Bibliothek, capturetexture und savetoxxxfile (mit XXX ist WIC, DDS oder TGA) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele). Für das vereinfachte Szenario der Erstellung eines Screenshots aus einer renderzieltextur empfiehlt es sich, die directxtk-Bibliothek "saveddstexturedefile" oder "savewictexturedefile" zu verwenden. Speichert eine Textur in einer Datei.
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- D3DX11SaveTextureToFile-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982317"
---
# <a name="d3dx11savetexturetofile-function"></a>D3DX11SaveTextureToFile-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfiehlt es sich, dass Sie die [directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek **capturetexture** und **savetoxxxfile** verwenden (wobei xxx gleich WIC, DDS oder TGA ist). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele). Für das vereinfachte Szenario der Erstellung eines Screenshots aus einer renderzieltextur empfiehlt es sich, die [directxtk](https://github.com/Microsoft/DirectXTK) -Bibliothek " **saveddstexturedefile** " oder " **savewictexturedefile**" zu verwenden.

 

Speichert eine Textur in einer Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* 
</dt> <dd>

Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Ein Zeiger auf ein [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt.

</dd> <dt>

*psrctexture* \[ in\]
</dt> <dd>

Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Zeiger auf die zu speichernde Textur. Siehe [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*Destformat* \[ in\]
</dt> <dd>

Type: **[ **Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)**

Das Format, in dem die Textur gespeichert wird (siehe [**Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)). Bibliothek d3dx11 \_ IFF \_ DDS ist das bevorzugte Format, da es die einzige Option ist, die alle Formate im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)unterstützt.

</dd> <dt>

*pdestfile* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name der Ziel Ausgabedatei, in der die Textur gespeichert wird. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind. Verwenden Sie den Rückgabewert, um festzustellen, ob *destformat* unterstützt wird.

## <a name="remarks"></a>Bemerkungen

**D3DX11SaveTextureToFile** schreibt die zusätzliche [**DDS- \_ Header \_ DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) -Struktur nur bei Bedarf für die Eingabe Textur (z. b. weil die Eingabe Textur im Standard-RGB-Format (sRGB) vorliegt). Wenn **D3DX11SaveTextureToFile** die **DDS- \_ Header \_ DXT10** -Struktur ausgibt, wird der **dwfourcc** -Member der [**DDS- \_ Pixel Format**](/windows/desktop/direct3ddds/dds-pixelformat) -Struktur für die Textur auf **DX10** festgelegt, um die präscense des **DDS- \_ Headers \_ DXT10** Extended-Header anzugeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

