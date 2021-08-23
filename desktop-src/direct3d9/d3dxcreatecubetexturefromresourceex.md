---
description: Erstellt eine Cubetextur aus einer Durch eine Zeichenfolge angegebenen Ressource. Dies ist eine erweiterte Funktion als D3DXCreateCubeTextureFromResource.
ms.assetid: 4d263386-8270-4967-8ef5-e9ac69e502a5
title: D3DXCreateCubeTextureFromResourceEx-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8548863f7c35ff3d56fd83287cf1c3628bb1a9ff89d8ad34346530063c494c99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857300"
---
# <a name="d3dxcreatecubetexturefromresourceex-function"></a>D3DXCreateCubeTextureFromResourceEx-Funktion

Erstellt eine Cubetextur aus einer Durch eine Zeichenfolge angegebenen Ressource. Dies ist eine erweiterte Funktion als [**D3DXCreateCubeTextureFromResource.**](d3dxcreatecubetexturefromresource.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateCubeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    HMODULE                hSrcModule,
  _In_    LPCTSTR                pSrcResource,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Cubetextur zugeordnet werden soll.

</dd> <dt>

*hSrcModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle für das Modul, in dem sich die Ressource befindet, oder **NULL** für das Modul, das dem Image zugeordnet ist, mit dem das Betriebssystem den aktuellen Prozess erstellt hat.

</dd> <dt>

*pSrcResource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen. Siehe Hinweise.

</dd> <dt>

*Größe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Breite und Höhe der Cubetextur in Pixel. Wenn es sich bei der Cubetextur beispielsweise um einen Cube mit 8 Pixeln oder 8 Pixeln handelt, sollte der Wert für diesen Parameter 8 sein. Wenn dieser Wert 0 oder D3DX \_ DEFAULT ist, werden die Dimensionen aus der Datei übernommen.

</dd> <dt>

*MipLevels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der angeforderten MIP-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, wird eine vollständige Mipmapkette erstellt.

</dd> <dt>

*Verwendung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0 oder D3DUSAGE \_ RENDERTARGET oder D3DUSAGE \_ DYNAMIC. Das Festlegen dieses Flags auf D3DUSAGE RENDERTARGET gibt an, dass die Oberfläche \_ als Renderziel verwendet werden soll. Die Ressource kann dann an den *pNewRenderTarget-Parameter* der [**SetRenderTarget-Methode übergeben**](/windows/desktop/api) werden. Wenn D3DUSAGE RENDERTARGET angegeben ist, sollte die Anwendung überprüfen, ob das Gerät diesen Vorgang unterstützt, indem \_ [**CheckDeviceFormat aufruft.**](/windows/desktop/api) D3DUSAGE \_ DYNAMIC gibt an, dass die Oberfläche dynamisch behandelt werden soll. Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden von dynamischen Texturen.](performance-optimizations.md)

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [aufzählten D3DFORMAT-Typs,](d3dformat.md) der das angeforderte Pixelformat für die Cubetextur beschreibt. Die zurückgegebene Cubetextur hat möglicherweise ein anderes Format als das von *Format angegebene* Format. Anwendungen sollten das Format der zurückgegebenen Cubetextur überprüfen. Wenn [D3DFMT \_ UNKNOWN](other-d3dx-constants.md)ist, wird das Format aus der Datei übernommen. Wenn D3DFMT FROM FILE, wird das Format genau wie in der Datei verwendet, und der Aufruf ist nicht möglich, wenn dies die \_ \_ Gerätefunktionen verletzt.

</dd> <dt>

*Pool* \[ In\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**aufzählten D3DPOOL-Typs,**](./d3dpool.md) der die Speicherklasse beschreibt, in der die Cubetextur platziert werden soll.

</dd> <dt>

*Filter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus mindestens einem [D3DX-FILTER, \_ ](d3dx-filter.md)der steuert, wie das Bild gefiltert wird. Die Angabe von D3DX DEFAULT für diesen Parameter entspricht der Angabe von \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus mindestens einem [D3DX-FILTER, \_ ](d3dx-filter.md) der steuert, wie das Bild gefiltert wird. Die Angabe von D3DX DEFAULT für diesen Parameter entspricht der Angabe von \_ D3DX \_ FILTER \_ BOX.

</dd> <dt>

*ColorKey* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR-Wert,**](d3dcolor.md) der durch transparentes Schwarz ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren. Dies ist immer eine 32-Bit-ARGB-Farbe, unabhängig vom Quellbildformat. Alpha ist wichtig und sollte für nicht transparente Farbtasten in der Regel auf FF festgelegt werden. Für nicht transparentes Schwarz wäre der Wert also gleich 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Zeiger auf eine [**D3DXIMAGE \_ INFO-Struktur,**](d3dximage-info.md) die mit einer Beschreibung der Daten in der Quellbilddatei gefüllt werden soll, oder **NULL.**

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Typ: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die eine 256-Farbpalette darstellt, die auffüllt werden soll, oder **NULL.**

</dd> <dt>

*ppCubeTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) die das erstellte Cubetexturobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in **D3DXCreateCubeTextureFromResourceExW auflösen.** Andernfalls wird der Funktionsaufruf in **D3DXCreateCubeTextureFromResourceExAauflöset,** da ANSI-Zeichenfolgen verwendet werden.

Diese Funktion unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga. Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Cubetexturen unterscheiden sich von anderen Oberflächen, da sie Auflistungen von Oberflächen sind. Zum Aufrufen [**von SetRenderTarget**](/windows/desktop/api) mit einer Cubetextur müssen Sie ein einzelnes Gesicht mit [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) auswählen und die resultierende Oberfläche **an SetRenderTarget übergeben.**

**D3DXCreateCubeTextureFromResourceEx** verwendet das DirectDraw-Oberflächendateiformat (DDS). Mit dem DirectX-Textur-Editor (Dxtex.exe) können Sie eine Cubemap aus anderen Dateiformaten generieren und im DDS-Dateiformat speichern. Sie können sich Dxtex.exe DirectX SDK darüber informieren. Informationen zum DirectX SDK finden Sie unter [Wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md)
</dt> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
