---
description: Erstellt eine Cubetextur aus einer Datei. Dies ist eine erweiterte Funktion als D3DXCreateCubeTextureFromFile.
ms.assetid: 77e64b33-9282-42fa-978c-a93fa9ba11fc
title: D3DXCreateCubeTextureFromFileEx-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d526e4737774f04e46f5c8aae9cda11a4d4693dee3eb1506ef42d1268625a5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027780"
---
# <a name="d3dxcreatecubetexturefromfileex-function"></a>D3DXCreateCubeTextureFromFileEx-Funktion

Erstellt eine Cubetextur aus einer Datei. Dies ist eine erweiterte Funktion als [**D3DXCreateCubeTextureFromFile.**](d3dxcreatecubetexturefromfile.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateCubeTextureFromFileEx(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _In_  DWORD                  Filter,
  _In_  DWORD                  MipFilter,
  _In_  D3DCOLOR               ColorKey,
  _Out_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_ PALETTEENTRY           *pPalette,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Cubetextur zugeordnet werden soll.

</dd> <dt>

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*Größe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Breite und Höhe der Cubetextur in Pixel. Wenn es sich bei der Cubetextur beispielsweise um einen Cube mit 8 x 8 Pixeln handelt, sollte der Wert für diesen Parameter 8 sein. Wenn dieser Wert 0 oder D3DX \_ DEFAULT ist, werden die Dimensionen aus der Datei übernommen.

</dd> <dt>

*MipLevels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der angeforderten MIP-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, wird eine vollständige Mipmapkette erstellt.

</dd> <dt>

*Nutzung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0 oder D3DUSAGE \_ RENDERTARGET oder D3DUSAGE \_ DYNAMIC. Durch Festlegen dieses Flags auf D3DUSAGE \_ RENDERTARGET wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll. Die Ressource kann dann an den *pNewRenderTarget-Parameter* der [**SetRenderTarget-Methode**](/windows/desktop/api) übergeben werden. Wenn D3DUSAGE \_ RENDERTARGET angegeben ist, sollte die Anwendung überprüfen, ob das Gerät diesen Vorgang unterstützt, indem [**sie CheckDeviceFormat aufruft.**](/windows/desktop/api) D3DUSAGE \_ DYNAMIC gibt an, dass die Oberfläche dynamisch behandelt werden soll. Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen.](performance-optimizations.md)

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT-Enumerationstyps,](d3dformat.md) der das angeforderte Pixelformat für die Cubetextur beschreibt. Die zurückgegebene Cubetextur hat möglicherweise ein anderes Format als das von *Format* angegebene Format. Anwendungen sollten das Format der zurückgegebenen Cubetextur überprüfen. Wenn [D3DFMT \_ UNKNOWN](other-d3dx-constants.md)ist, wird das Format aus der Datei übernommen. Wenn D3DFMT \_ FROM \_ FILE verwendet wird, wird das Format genau wie in der Datei verwendet, und der Aufruf schlägt fehl, wenn dies gegen die Gerätefunktionen verstößt.

</dd> <dt>

*Pool* \[ In\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**D3DPOOL-Enumerationstyps,**](./d3dpool.md) der die Speicherklasse beschreibt, in der die Cubetextur platziert werden soll.

</dd> <dt>

*Filterung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einer oder mehreren [D3DX-FILTER-Konstanten, \_ ](d3dx-filter.md) die steuern, wie das Bild gefiltert wird. Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht der Angabe von D3DX FILTER TRIANGLE \_ \_ \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einer oder mehreren [D3DX-FILTER-Konstanten, \_ ](d3dx-filter.md) die steuern, wie das Bild gefiltert wird. Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht der Angabe von D3DX FILTER \_ \_ BOX. Verwenden Sie außerdem die Bits 27 bis 31, um die Anzahl der Mip-Ebenen anzugeben, die übersprungen werden sollen (von oben in der Mipmapkette), wenn eine DDS-Textur in den Arbeitsspeicher geladen wird. Dadurch können Sie bis zu 32 Ebenen überspringen.

</dd> <dt>

*ColorKey* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR-Wert,**](d3dcolor.md) der durch transparentes Schwarz ersetzt werden soll, oder 0, um den Farbschlüssel zu deaktivieren. Dies ist immer eine 32-Bit-ARGB-Farbe, unabhängig vom Quellbildformat. Alpha ist von Bedeutung und sollte in der Regel für nicht transparente Farbschlüssel auf FF festgelegt werden. Daher wäre der Wert für nicht transparentes Schwarz gleich 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ out\]
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Zeiger auf eine [**D3DXIMAGE \_ INFO-Struktur,**](d3dximage-info.md) die mit einer Beschreibung der Daten in der Quellbilddatei gefüllt werden soll, oder **NULL.**

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Typ: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die eine zu füllende 256-Farbpalette darstellt, oder **NULL.**

</dd> <dt>

*ppCubeTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) die das erstellte Cubetexturobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in **D3DXCreateCubeTextureFromFileExW** aufgelöst. Andernfalls wird der Funktionsaufruf in **D3DXCreateCubeTextureFromFileExA** aufgelöst, da ANSI-Zeichenfolgen verwendet werden.

Diese Funktion unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga. Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Cubetexturen unterscheiden sich von anderen Oberflächen darin, dass sie Auflistungen von Oberflächen sind. Um [**SetRenderTarget**](/windows/desktop/api) mit einer Cubetextur aufzurufen, müssen Sie mit [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) ein einzelnes Gesicht auswählen und die resultierende Oberfläche an **SetRenderTarget** übergeben.

**D3DXCreateCubeTextureFromFileEx** verwendet das DDS-Dateiformat (DirectDraw Surface). Mit dem DirectX-Textur-Editor (Dxtex.exe) können Sie eine Cubezuordnung aus anderen Dateiformaten generieren und im DDS-Dateiformat speichern. Sie können Dxtex.exe abrufen und sich über das DirectX SDK darüber informieren. Informationen zum DirectX SDK finden Sie unter [Wo befindet sich das DirectX SDK?](../directx-sdk--august-2009-.md).

Wenn Sie Mipmapebenen beim Laden einer DDS-Datei überspringen, verwenden Sie das D3DX \_ SKIP \_ DDS \_ MIP \_ LEVELS-Makro, um den MipFilter-Wert zu generieren. Dieses Makro verwendet die Anzahl der zu überspringenden Ebenen und den Filtertyp und gibt den Filterwert zurück, der dann an den MipFilter-Parameter übergeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md)
</dt> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
