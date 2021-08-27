---
description: Erstellt eine Volumetextur aus einer Datei. Dies ist eine erweiterte Funktion als D3DXCreateVolumeTextureFromFileInMemory.
ms.assetid: 1a43f906-1826-40a3-a7a9-a0536c977164
title: D3DXCreateVolumeTextureFromFileInMemoryEx-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8e273cbdb8e65d751cad4679e7c8a38ec5de2ea2e7e6a62f59d396d44ead24a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119240"
---
# <a name="d3dxcreatevolumetexturefromfileinmemoryex-function"></a>D3DXCreateVolumeTextureFromFileInMemoryEx-Funktion

Erstellt eine Volumetextur aus einer Datei. Dies ist eine erweiterte Funktion als [**D3DXCreateVolumeTextureFromFileInMemory.**](d3dxcreatevolumetexturefromfileinmemory.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCVOID                  pSrcData,
  _In_    UINT                     SrcDataSize,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
  _In_    D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Textur zugeordnet werden soll.

</dd> <dt>

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf die Datei im Arbeitsspeicher, aus der die Volumetextur erstellt werden soll.

</dd> <dt>

*SrcDataSize* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Größe der Datei im Arbeitsspeicher in Bytes.

</dd> <dt>

*Breite* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Breite in Pixel. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, werden die Dimensionen aus der Datei übernommen. Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), finden Sie in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Höhe in Pixel. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, werden die Dimensionen aus der Datei übernommen. Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), finden Sie in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*Tiefe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Tiefe in Pixel. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, werden die Dimensionen aus der Datei übernommen. Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), finden Sie in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*MipLevels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der angeforderten MIP-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, wird eine vollständige Mipmapkette erstellt.

</dd> <dt>

*Verwendung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET oder D3DUSAGE \_ DYNAMIC. Das Festlegen dieses Flags auf D3DUSAGE RENDERTARGET gibt an, dass die Oberfläche \_ als Renderziel verwendet werden soll. Die Ressource kann dann an den *pNewRenderTarget-Parameter* der [**SetRenderTarget-Methode übergeben**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) werden. Wenn entweder D3DUSAGE RENDERTARGET oder D3DUSAGE DYNAMIC angegeben ist, muss Pool auf D3DPOOL DEFAULT festgelegt werden, und die Anwendung sollte überprüfen, ob das Gerät diesen Vorgang unterstützt, indem \_ \_  \_ [**CheckDeviceFormat aufruft.**](/windows/desktop/api) D3DUSAGE \_ DYNAMIC gibt an, dass die Oberfläche dynamisch behandelt werden soll. Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden von dynamischen Texturen.](performance-optimizations.md)

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [aufzählten D3DFORMAT-Typs,](d3dformat.md) der das angeforderte Pixelformat für die Textur beschreibt. Die zurückgegebene Textur hat möglicherweise ein anderes Format als das von *Format angegebene* Format. Anwendungen sollten das Format der zurückgegebenen Textur überprüfen. Wenn [D3DFMT \_ UNKNOWN](other-d3dx-constants.md)ist, wird das Format aus der Datei übernommen. Wenn D3DFMT FROM FILE, wird das Format genau wie in der Datei verwendet, und der Aufruf ist nicht möglich, wenn dies die \_ \_ Gerätefunktionen verletzt.

</dd> <dt>

*Pool* \[ In\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**aufzählten D3DPOOL-Typs,**](./d3dpool.md) der die Speicherklasse beschreibt, in der die Textur platziert werden soll.

</dd> <dt>

*Filter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus mindestens einem [D3DX-FILTER, \_ ](d3dx-filter.md) der steuert, wie das Bild gefiltert wird. Die Angabe von D3DX DEFAULT für diesen Parameter entspricht der Angabe von \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus mindestens einem [D3DX-FILTER, \_ ](d3dx-filter.md) der steuert, wie das Bild gefiltert wird. Die Angabe von D3DX DEFAULT für diesen Parameter entspricht der Angabe von \_ D3DX \_ FILTER \_ BOX. Verwenden Sie außerdem die Bits 27-31, um die Anzahl der MIP-Ebenen anzugeben, die übersprungen werden sollen (vom oberen Ende der Mipmap-Kette), wenn eine DDS-Textur in den Arbeitsspeicher geladen wird. Dadurch können Sie bis zu 32 Ebenen überspringen.

</dd> <dt>

*ColorKey* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR-Wert,**](d3dcolor.md) der durch transparentes Schwarz ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren. Dies ist immer eine 32-Bit-ARGB-Farbe, unabhängig vom Quellbildformat. Alpha ist wichtig und sollte für nicht transparente Farbtasten in der Regel auf FF festgelegt werden. Für nicht transparentes Schwarz wäre der Wert also gleich 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Zeiger auf eine [**D3DXIMAGE \_ INFO-Struktur,**](d3dximage-info.md) die mit einer Beschreibung der Daten in der Quellbilddatei aufgefüllt werden soll, oder **NULL.**

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Typ: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die eine zu füllende 256-Farbpalette darstellt, oder **NULL.**

</dd> <dt>

*ppVolumeTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DVolumeTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) die das erstellte Texturobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einen der folgenden Werte haben: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga. Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Wenn Sie Mipmapebenen beim Laden einer DDS-Datei überspringen, verwenden Sie das D3DX SKIP DDS MIP LEVELS-Makro, um den \_ \_ \_ \_ *MipFilter-Wert zu* generieren. Dieses Makro verwendet die Anzahl der zu überspringenden Ebenen und den Filtertyp und gibt den Filterwert zurück, der dann an den *MipFilter-Parameter übergeben* wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3DXCreateVolumeTextureFromFile**](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileEx**](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
