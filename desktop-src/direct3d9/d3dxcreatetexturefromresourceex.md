---
description: Erstellt eine Textur aus einer Ressource. Dies ist eine erweiterte Funktion als D3DXCreateTextureFromResource.
ms.assetid: 6015e2fa-9deb-4e6a-a401-f10fb05f40b7
title: D3DXCreateTextureFromResourceEx-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cc3d8d8bce22a8a77f8744bf2540fba7ede58fc4122c8fa2a8fea8147a8f6332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732041"
---
# <a name="d3dxcreatetexturefromresourceex-function"></a>D3DXCreateTextureFromResourceEx-Funktion

Erstellt eine Textur aus einer Ressource. Dies ist eine erweiterte Funktion als [**D3DXCreateTextureFromResource.**](d3dxcreatetexturefromresource.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    HMODULE            hSrcModule,
  _In_    LPCTSTR            pSrcResource,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Textur zugeordnet werden soll.

</dd> <dt>

*hSrcModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Behandeln Sie das Modul, in dem sich die Ressource befindet, oder **NULL** für das Modul, das dem Image zugeordnet ist, das vom Betriebssystem zum Erstellen des aktuellen Prozesses verwendet wurde.

</dd> <dt>

*pSrcResource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*Breite* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Breite in Pixel. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, werden die Dimensionen aus der Datei übernommen.

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Höhe in Pixel. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, werden die Dimensionen aus der Datei übernommen.

</dd> <dt>

*MipLevels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der angeforderten MIP-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, wird eine vollständige Mipmapkette erstellt.

</dd> <dt>

*Nutzung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET oder D3DUSAGE \_ DYNAMIC. Durch Festlegen dieses Flags auf D3DUSAGE \_ RENDERTARGET wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll. Die Ressource kann dann an den *pNewRenderTarget-Parameter* der [**SetRenderTarget-Methode**](/windows/desktop/api) übergeben werden. Wenn entweder D3DUSAGE \_ RENDERTARGET oder D3DUSAGE angegeben ist, muss *Pool* auf D3DPOOL DEFAULT festgelegt \_ werden, und die Anwendung sollte überprüfen, ob das Gerät diesen Vorgang unterstützt, indem [**CheckDeviceFormat**](/windows/desktop/api)aufgerufen wird. D3DUSAGE \_ DYNAMIC gibt an, dass die Oberfläche dynamisch behandelt werden soll. Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Leistungsoptimierungen (Direct3D 9)](performance-optimizations.md)Mit dynamischen Texturen.

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Ein Member des [D3DFORMAT-Enumerationstyps,](d3dformat.md) der das angeforderte Pixelformat für die Textur beschreibt. Die zurückgegebene Textur hat möglicherweise ein anderes Format als das von *Format* angegebene Format. Anwendungen sollten das Format der zurückgegebenen Textur überprüfen. Wenn [D3DFMT \_ UNKNOWN](other-d3dx-constants.md)ist, wird das Format aus der Datei übernommen. Wenn D3DFMT \_ FROM \_ FILE verwendet wird, wird das Format genau wie in der Datei verwendet, und der Aufruf schlägt fehl, wenn dies gegen die Gerätefunktionen verstößt.

</dd> <dt>

*Pool* \[ In\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**D3DPOOL-Enumerationstyps,**](./d3dpool.md) der die Speicherklasse beschreibt, in der die Textur platziert werden soll.

</dd> <dt>

*Filterung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren [ \_ D3DX-FILTERN,](d3dx-filter.md) die steuern, wie das Bild gefiltert wird. Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht der Angabe von D3DX FILTER TRIANGLE \_ \_ \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren [ \_ D3DX-FILTERN,](d3dx-filter.md) die steuern, wie das Bild gefiltert wird. Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht der Angabe von D3DX FILTER \_ \_ BOX.

</dd> <dt>

*ColorKey* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR-Wert,**](d3dcolor.md) der durch transparentes Schwarz ersetzt werden soll, oder 0, um den Farbschlüssel zu deaktivieren. Dies ist immer eine 32-Bit-ARGB-Farbe, unabhängig vom Quellbildformat. Alpha ist von Bedeutung und sollte in der Regel für nicht transparente Farbschlüssel auf FF festgelegt werden. Daher wäre der Wert für nicht transparentes Schwarz gleich 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Zeiger auf eine [**D3DXIMAGE \_ INFO-Struktur,**](d3dximage-info.md) die mit einer Beschreibung der Daten in der Quellbilddatei gefüllt werden soll, oder **NULL.**

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Typ: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die eine 256-farbige Palette darstellt, die ausgefüllt werden soll, oder **NULL**.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die das erstellte Texturobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateTextureFromResourceExW aufgelöst. Andernfalls wird der Funktionsaufruf in D3DXCreateTextureFromResourceExA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.

Die geladene Ressource muss vom Typ RT \_ BITMAP oder RT \_ RCDATA sein. Der Ressourcentyp RT \_ RCDATA wird verwendet, um andere Formate als Bitmaps zu laden (z. B. TGA, .jpg und DDS).

Diese Funktion unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga. Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
</dt> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
