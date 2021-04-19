---
description: Speichert eine Textur in einer Datei.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: D3DXSaveTextureToFile-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c11cc8b512527fb0610c288fdbaeba6c976604a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367364"
---
# <a name="d3dxsavetexturetofile-function"></a>D3DXSaveTextureToFile-Funktion

Speichert eine Textur in einer Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdestfile* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ein Zeiger auf eine Zeichenfolge, die den Dateinamen des Ziel Bilds angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der String-Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*Destformat* \[ in\]
</dt> <dd>

Type: **[ **D3DXIMAGE \_ File Format**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ Dateiformat**](./d3dximage-fileformat.md) , das das beim Speichern zu verwendende Dateiformat angibt. Diese Funktion unterstützt das Speichern in allen **D3DXIMAGE \_ File Format** -Formaten außer Portable pixmap (. ppm) und TARGA/Truevision Graphics Adapter (. TGA).

</dd> <dt>

*psrctexture* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Zeiger auf die [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) -Schnittstelle, die die zu speichernde Textur enthält.

</dd> <dt>

*psrcpalette* \[ in\]
</dt> <dd>

Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ein Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine Palette von 256 Farben enthält. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXSaveTextureToFileW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXSaveTextureToFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.

Wenn das Volume nicht dynamisch ist (weil ein Verwendungs Parameter bei der Erstellung auf 0 festgelegt ist) und sich im Videospeicher befindet (der auf D3DPOOL default festgelegte Speicherpool \_ ), schlägt **D3DXSaveTextureToFile** fehl, da D3DX nicht dynamische Volumes nicht sperren kann, die sich im Videospeicher befinden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFile**](d3dxsavesurfacetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
