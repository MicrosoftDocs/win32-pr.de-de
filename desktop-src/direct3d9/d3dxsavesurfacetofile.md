---
description: Speichert eine-Oberfläche in einer Datei.
ms.assetid: 28bbf728-afde-4d25-8562-9d6a957aab2d
title: D3DXSaveSurfaceToFile-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: cd19e0a8f7b9557b6bcbe6c71afcdca7c9037b70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361863"
---
# <a name="d3dxsavesurfacetofile-function"></a>D3DXSaveSurfaceToFile-Funktion

Speichert eine-Oberfläche in einer Datei.

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

*psrcsurface* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Ein Zeiger auf die [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle, die das zu speichernde Bild enthält.

</dd> <dt>

*psrcpalette* \[ in\]
</dt> <dd>

Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ein Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine Palette von 256 Farben enthält. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*psrcrect* \[ in\]
</dt> <dd>

Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur. Gibt das Quell Rechteck an. Legen Sie diesen Parameter auf **null** fest, um das gesamte Bild anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXSaveSurfaceToFileW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXSaveSurfaceToFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
