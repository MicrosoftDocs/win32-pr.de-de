---
description: Speichert eine Textur in einer Bilddatei.
ms.assetid: 8dcfd58a-ae1e-43c3-8ff1-94e3fa398b0f
title: D3DXSaveTextureToFileInMemory-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 864362d016190abc4168bdfa66714be371b7811d29b281612e6ba7dc3e0f4889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749820"
---
# <a name="d3dxsavetexturetofileinmemory-function"></a>D3DXSaveTextureToFileInMemory-Funktion

Speichert eine Textur in einer Bilddatei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSaveTextureToFileInMemory(
  _Out_       LPD3DXBUFFER           *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_        LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDestBuf* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf einen [**ID3DXBuffer,**](id3dxbuffer.md) der das Image speichern soll.

</dd> <dt>

*DestFormat* \[ In\]
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) gibt das Dateiformat an, das beim Speichern verwendet werden soll. Diese Funktion unterstützt das Speichern in allen **D3DXIMAGE \_ FILEFORMAT-Formaten** mit Ausnahme von Portable Pixmap (.ppm) und Targa/Truevision Graphics Adapter (.tga).

</dd> <dt>

*pSrcTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Zeiger auf die [**IDirect3DBaseTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) die das zu speichernde Bild enthält.

</dd> <dt>

*pSrcPalette* \[ In\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die eine Palette von 256 Farben enthält. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL.

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

[**D3DXSaveSurfaceToFileInMemory**](d3dxsavesurfacetofileinmemory.md)
</dt> <dt>

[**D3DXSaveVolumeToFileInMemory**](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
