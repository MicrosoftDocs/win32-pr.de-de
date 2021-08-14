---
description: Speichert ein Volume in einer Datei auf dem Datenträger.
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: D3DXSaveVolumeToFile-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e6c5a03f9e1874d7706ecbf43cfd312abc472b8e7127ba9f21a35313374157b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524445"
---
# <a name="d3dxsavevolumetofile-function"></a>D3DXSaveVolumeToFile-Funktion

Speichert ein Volume in einer Datei auf dem Datenträger.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDestFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen des Zielimages angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen. Siehe Hinweise.

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

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXSaveVolumeToFileW auflösen. Andernfalls wird der Funktionsaufruf in >D3DXSaveVolumeToFileA,da ANSI-Zeichenfolgen verwendet werden.

Diese Funktion verarbeitet die Konvertierung in und aus komprimierten Texturformaten.

Wenn das Volume nicht dynamisch ist (aufgrund eines Verwendungsparameters, der bei der Erstellung auf 0 festgelegt ist) und sich im Videospeicher befindet (der Speicherpool ist auf D3DPOOL DEFAULT festgelegt), kann \_ [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) nicht gesperrt werden, da D3DX nicht dynamische Volumes im Videospeicher sperren kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFile**](d3dxsavesurfacetofile.md)
</dt> <dt>

[**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFileInMemory**](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
