---
title: D3DX11SaveTextureToFile-Funktion (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt. Hinweis Anstelle dieser Funktion wird empfohlen, die DirectXTex-Bibliothek CaptureTexture und dann SaveToXXXFile (wobei XXX WIC, DDS oder TGA ist) zu verwenden. WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Art-Source-Format für Spiele). Für das vereinfachte Szenario der Erstellung eines Screenshots aus einer Renderzieltextur wird empfohlen, die DirectXTK-Bibliothek SaveDDSTextureToFile oder SaveWICTextureToFile zu verwenden. Speichern Sie eine Textur in einer Datei.
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
ms.openlocfilehash: e74f73eaad167c7c813a8effe93b65ea7558514ae78ecc00926b420014f4a37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099262"
---
# <a name="d3dx11savetexturetofile-function"></a>D3DX11SaveTextureToFile-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, wird empfohlen, die [DirectXTex-Bibliothek](https://github.com/Microsoft/DirectXTex) **CaptureTexture** und dann **SaveToXXXFile (wobei** XXX WIC, DDS oder TGA ist) zu verwenden. WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Art-Source-Format für Spiele). Für das vereinfachte Szenario der Erstellung eines Screenshots aus einer Renderzieltextur wird empfohlen, die [DirectXTK-Bibliothek](https://github.com/Microsoft/DirectXTK) **SaveDDSTextureToFile** oder **SaveWICTextureToFile zu** verwenden.

 

Speichern Sie eine Textur in einer Datei.

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

Typ: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Ein Zeiger auf ein [**ID3D11DeviceContext-Objekt.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

</dd> <dt>

*pSrcTexture* \[ In\]
</dt> <dd>

Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Zeiger auf die zu speichernde Textur. Siehe [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*DestFormat* \[ In\]
</dt> <dd>

Typ: **[ **D3DX11 \_ IMAGE \_ FILE \_ FORMAT**](d3dx11-image-file-format.md)**

Das Format, in dem die Textur gespeichert wird (siehe [**D3DX11 \_ IMAGE \_ FILE \_ FORMAT**](d3dx11-image-file-format.md)). D3DX11 \_ IFF \_ DDS ist das bevorzugte Format, da es die einzige Option ist, die alle Formate im [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)unterstützt.

</dd> <dt>

*pDestFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Name der Zielausgabedatei, in der die Textur gespeichert wird. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 11-Rückgabecodes aufgeführten](d3d11-graphics-reference-returnvalues.md)Werte. verwenden Sie den Rückgabewert, um festzustellen, ob *destFormat* unterstützt wird.

## <a name="remarks"></a>Hinweise

**D3DX11SaveTextureToFile** schreibt die zusätzliche [**DDS \_ HEADER \_ DXT10-Struktur**](/windows/desktop/direct3ddds/dds-header-dxt10) nur bei Bedarf für die Eingabetextur (z. B. weil die Eingabetextur im STANDARD-RGB-Format (sRGB) vorliegt). Wenn **D3DX11SaveTextureToFile** die **DDS HEADER \_ \_ DXT10-Struktur** schreibt, wird der **dwFourCC-Member** der [**DDS \_ PIXELFORMAT-Struktur**](/windows/desktop/direct3ddds/dds-pixelformat) für die Textur auf **DX10** festgelegt, um die Präsense des erweiterten **Headers DDS \_ HEADER \_ DXT10** anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

