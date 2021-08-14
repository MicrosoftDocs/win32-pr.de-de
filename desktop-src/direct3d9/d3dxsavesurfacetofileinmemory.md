---
description: Speichert eine Oberfläche in einer Bilddatei.
ms.assetid: 6320e5ed-e43d-43bf-a746-5478df42941d
title: D3DXSaveSurfaceToFileInMemory-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6dd6715c05be0e6472b1c630ebdda209d48dfc571d4b3d5234b80f3700e597d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986440"
---
# <a name="d3dxsavesurfacetofileinmemory-function"></a>D3DXSaveSurfaceToFileInMemory-Funktion

Speichert eine Oberfläche in einer Bilddatei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSaveSurfaceToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DSURFACE9   pSrcSurface,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const RECT                 *pSrcRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDestBuf* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf einen [**ID3DXBuffer,**](id3dxbuffer.md) der das Bild speichert.

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

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

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

[**D3DXSaveVolumeToFileInMemory**](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
