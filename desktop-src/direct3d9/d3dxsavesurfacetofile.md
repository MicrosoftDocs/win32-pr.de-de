---
description: Speichert eine Oberfläche in einer Datei.
ms.assetid: 28bbf728-afde-4d25-8562-9d6a957aab2d
title: D3DXSaveSurfaceToFile-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f28f4958a031a5f5582d26eac6e7c77df241bf5a87316c60970ee38cc56bb35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749950"
---
# <a name="d3dxsavesurfacetofile-function"></a>D3DXSaveSurfaceToFile-Funktion

Speichert eine Oberfläche in einer Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSaveSurfaceToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DSURFACE9   pSrcSurface,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const RECT                 *pSrcRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDestFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen des Zielimages angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*DestFormat* \[ In\]
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT,**](./d3dximage-fileformat.md) das das beim Speichern zu verwendende Dateiformat angibt. Diese Funktion unterstützt das Speichern in allen **D3DXIMAGE \_ FILEFORMAT-Formaten** mit Ausnahme von Portable Pixmap (.ppm) und Targa/Truevision Graphics Adapter (.tga).

</dd> <dt>

*pSrcSurface* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Zeiger auf die [**IDirect3DSurface9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) die das zu speichernde Image enthält.

</dd> <dt>

*pSrcPalette* \[ In\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die eine Palette von 256 Farben enthält. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pSrcRect* \[ In\]
</dt> <dd>

Typ: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Zeiger auf eine [**RECT-Struktur.**](/previous-versions//dd162897(v=vs.85)) Gibt das Quellrechteck an. Legen Sie diesen Parameter auf **NULL** fest, um das gesamte Bild anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXSaveSurfaceToFileW aufgelöst. Andernfalls wird der Funktionsaufruf in D3DXSaveSurfaceToFileA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.

Diese Funktion verarbeitet die Konvertierung in und aus komprimierten Texturformaten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
