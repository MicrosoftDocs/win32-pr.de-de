---
description: Speichert ein Volume in einem Puffer. Die -Methode erstellt einen ID3DXBuffer-Puffer zum Speichern der Daten und gibt dieses Objekt zurück.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: D3DXSaveVolumeToFileInMemory-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7c7326609d6d3c006f3c97aeff18de425a27569db63378864fc34335558117e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298403"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a>D3DXSaveVolumeToFileInMemory-Funktion

Speichert ein Volume in einem Puffer. Die -Methode erstellt einen [**ID3DXBuffer-Puffer**](id3dxbuffer.md) zum Speichern der Daten und gibt dieses Objekt zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDestBuf* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf einen [**ID3DXBuffer-Puffer,**](id3dxbuffer.md) in dem das Bild gespeichert wird.

</dd> <dt>

*DestFormat* \[ In\]
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) gibt das Dateiformat an, das beim Speichern verwendet werden soll. Diese Funktion unterstützt das Speichern in allen **D3DXIMAGE \_ FILEFORMAT-Formaten** mit Ausnahme von Portable Pixmap (.ppm) und Targa/Truevision Graphics Adapter (.tga).

</dd> <dt>

*pSrcVolume* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Zeiger auf die [**IDirect3DVolume9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) die das zu speichernde Bild enthält.

</dd> <dt>

*pSrcPalette* \[ In\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die eine Palette mit 256 Farben enthält. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pSrcBox* \[ In\]
</dt> <dd>

Typ: **const [**D3DBOX**](d3dbox.md) \***

Zeiger auf eine [**D3DBOX-Struktur.**](d3dbox.md) Gibt das Quellfeld an. Legen Sie diesen Parameter auf **NULL fest,** um das gesamte Volume anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
