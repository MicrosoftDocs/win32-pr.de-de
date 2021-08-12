---
description: Erstellt eine Textur aus einer Datei. Dies ist eine erweiterte Funktion als D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: D3DXCreateTextureFromFileEx-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5964f7f466dac135d08958ef66c12a1dfe2e61a19180eb45072c5489f9f4a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299245"
---
# <a name="d3dxcreatetexturefromfileex-function"></a>D3DXCreateTextureFromFileEx-Funktion

Erstellt eine Textur aus einer Datei. Dies ist eine erweiterte Funktion als [**D3DXCreateTextureFromFile.**](d3dxcreatetexturefromfile.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
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

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen. Siehe Hinweise.

</dd> <dt>

*Breite* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Breite in Pixel. Wenn dieser Wert 0 (null) oder D3DX DEFAULT ist, werden die Dimensionen aus der Datei übernommen und auf eine \_ Zweierleistung aufgerundet. Wenn das Gerät nicht die Leistung von 2 Texturen unterstützt und [D3DX \_ DEFAULT \_ NONPOW2](other-d3dx-constants.md) angegeben ist, wird die Größe nicht gerundet.

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Höhe in Pixel. Wenn dieser Wert 0 (null) oder D3DX DEFAULT ist, werden die Dimensionen aus der Datei übernommen und auf eine \_ Zweierleistung aufgerundet. Wenn das Gerät nicht die Leistung von 2 Texturen unterstützt und [D3DX \_ DEFAULT \_ NONPOW2](other-d3dx-constants.md) getrennt ist, wird die Größe nicht gerundet.

</dd> <dt>

*MipLevels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der angeforderten MIP-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, wird eine vollständige Mipmapkette erstellt. Wenn D3DX FROM FILE verwendet wird, wird die Größe genau wie in der Datei verwendet, und der Aufruf ist nicht möglich, wenn dies die \_ \_ Gerätefunktionen verletzt.

</dd> <dt>

*Nutzung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)oder **D3DUSAGE \_ DYNAMIC**. Das Festlegen dieses Flags **auf D3DUSAGE \_ RENDERTARGET gibt** an, dass die Oberfläche als Renderziel verwendet werden soll. Die Ressource kann dann an den *pNewRenderTarget-Parameter* der [**SetRenderTarget-Methode übergeben**](/windows/desktop/api) werden. Wenn **entweder D3DUSAGE \_ RENDERTARGET** oder **D3DUSAGE \_ DYNAMIC** angegeben ist, muss *Pool* auf D3DPOOL DEFAULT festgelegt werden, und die Anwendung sollte überprüfen, ob das Gerät diesen Vorgang unterstützt, indem \_ [**CheckDeviceFormat aufruft.**](/windows/desktop/api) **D3DUSAGE \_ DYNAMIC** gibt an, dass die Oberfläche dynamisch behandelt werden soll. Weitere Informationen [finden Sie unter Verwenden dynamischer Texturen.](performance-optimizations.md)

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [aufzählten D3DFORMAT-Typs,](d3dformat.md) der das angeforderte Pixelformat für die Textur beschreibt. Die zurückgegebene Textur hat möglicherweise ein anderes Format als das von *Format angegebene* Format. Anwendungen sollten das Format der zurückgegebenen Textur überprüfen. Wenn D3DFMT \_ UNKNOWN, wird das Format aus der Datei übernommen. Wenn D3DFMT FROM FILE, wird das Format genau wie in der Datei verwendet, und der Aufruf ist nicht möglich, wenn dies die \_ \_ Gerätefunktionen verletzt.

</dd> <dt>

*Pool* \[ In\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**aufzählten D3DPOOL-Typs,**](./d3dpool.md) der die Speicherklasse beschreibt, in der die Textur platziert werden soll.

</dd> <dt>

*Filter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus mindestens einer [D3DX \_ FILTER-Konstante,](d3dx-filter.md) die steuert, wie das Bild gefiltert wird. Die Angabe [von D3DX \_ DEFAULT](other-d3dx-constants.md) für diesen Parameter entspricht der Angabe von D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus mindestens einer [D3DX \_ FILTER-Konstante,](d3dx-filter.md) die steuert, wie das Bild gefiltert wird. Die Angabe von D3DX DEFAULT für diesen Parameter entspricht der Angabe von \_ D3DX \_ FILTER \_ BOX. Verwenden Sie darüber hinaus die Bits 27 bis 31, um die Anzahl der Mip-Ebenen anzugeben, die übersprungen werden sollen (von oben in der Mipmap-Kette), wenn eine DDS-Textur in den Arbeitsspeicher geladen wird. Dadurch können Sie bis zu 32 Ebenen überspringen.

</dd> <dt>

*ColorKey* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR-Wert,**](d3dcolor.md) der durch transparentes Schwarz ersetzt werden soll, oder 0 zum Deaktivieren des Farbschlüssels. Dies ist immer eine 32-Bit-ARGB-Farbe, unabhängig vom Quellbildformat. Alpha ist wichtig und sollte für nicht transparente Farbtasten in der Regel auf FF festgelegt werden. Daher wäre der Wert für opakes Schwarz gleich 0xFF000000.

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

*ppTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die das erstellte Texturobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateTextureFromFileExWauflös. Andernfalls wird der Funktionsaufruf in D3DXCreateTextureFromFileExAauflöset, da ANSI-Zeichenfolgen verwendet werden.

Verwenden [**Sie D3DXCheckTextureRequirements,**](d3dxchecktexturerequirements.md) um zu bestimmen, ob Ihr Gerät die Textur mit dem aktuellen Zustand unterstützen kann.

Diese Funktion unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga. Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Bei Mipmappentexturen wird jede Ebene automatisch mit der geladenen Textur gefüllt. Beim Laden von Bildern in mipmapped-Texturen können einige Geräte nicht zu einem 1x1-Bild wechseln, und diese Funktion wird fehlschlagen. In diesem Fall müssen die Images manuell geladen werden.

Für die beste Leistung bei Verwendung **von D3DXCreateTextureFromFileEx:**

1.  Die Bildskalierung und Formatkonvertierung zur Ladezeit kann langsam sein. Store Bilder in dem Format und der Auflösung, in dem sie verwendet werden. Wenn die Zielhardware eine Leistung von 2 Dimensionen erfordert, erstellen und speichern Sie Images mit einer Leistung von zwei Dimensionen.
2.  Filtern Sie für die Erstellung von Mipmap-Bildern zur Ladezeit mithilfe von [D3DX \_ FILTER \_ BOX](d3dx-filter.md). Ein Feldfilter ist viel schneller als andere Filtertypen wie D3DX \_ FILTER \_ TRIANGLE.
3.  Erwägen Sie die Verwendung von DDS-Dateien. Da DDS-Dateien zur Darstellung eines beliebigen Direct3D 9-Texturformats verwendet werden können, sind sie für D3DX sehr einfach zu lesen. Außerdem können sie Mipmaps speichern, sodass alle Algorithmen zur Mipmap-Generierung zum Erstellen der Bilder verwendet werden können.

Wenn Sie Mipmapebenen beim Laden einer DDS-Datei überspringen, verwenden Sie das D3DX SKIP DDS MIP LEVELS-Makro, um den \_ \_ \_ \_ MipFilter-Wert zu generieren. Dieses Makro verwendet die Anzahl der zu überspringenden Ebenen und den Filtertyp und gibt den Filterwert zurück, der dann an den MipFilter-Parameter übergeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
</dt> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
