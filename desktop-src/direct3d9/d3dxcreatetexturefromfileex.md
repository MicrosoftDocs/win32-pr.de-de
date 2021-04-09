---
description: Erstellt eine Textur aus einer Datei. Dies ist eine erweiterte Funktion als D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: D3DXCreateTextureFromFileEx-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: f4dba1424f98389a9282fdebf9dae55c7e1601f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870104"
---
# <a name="d3dxcreatetexturefromfileex-function"></a>D3DXCreateTextureFromFileEx-Funktion

Erstellt eine Textur aus einer Datei. Dies ist eine erweiterte Funktion als [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).

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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.

</dd> <dt>

*psrcfile* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der String-Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*Breite* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Breite in Pixel. Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen und auf eine Potenz von zwei aufgerundet. Wenn das Gerät eine nicht-Potenz von 2 Texturen unterstützt und [D3DX \_ Default \_ NONPOW2](other-d3dx-constants.md) angegeben ist, wird die Größe nicht gerundet.

</dd> <dt>

*Höhe* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Höhe in Pixel. Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen und auf eine Potenz von zwei aufgerundet. Wenn das Gerät eine nicht-Potenz von 2 Texturen und [D3DX \_ Standard \_ NONPOW2](other-d3dx-constants.md) unterstützt, wird die Größe nicht gerundet.

</dd> <dt>

*Miplevels* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der angeforderten Mip-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt. Wenn D3DX \_ from \_ File, wird die Größe genau so wie in der Datei erstellt, und der-Rückruf schlägt fehl, wenn dies gegen Gerätefunktionen verstößt.

</dd> <dt>

*Verwendung* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ renderTarget**](d3dusage.md)oder **D3DUSAGE \_ Dynamic**. Wenn dieses Flag auf **D3DUSAGE \_ renderTarget** festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll. Die Ressource kann dann an den *pnewrendertarget* -Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden. Wenn entweder **D3DUSAGE \_ renderTarget** oder **D3DUSAGE \_ Dynamic** angegeben ist, muss der *Pool* auf D3DPOOL Default festgelegt werden \_ , und die Anwendung sollte überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt. **D3DUSAGE \_ Dynamic** gibt an, dass die Oberfläche dynamisch behandelt werden soll. Siehe [Verwenden dynamischer Texturen](performance-optimizations.md).

</dd> <dt>

*Format* \[ in\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die Textur beschreibt. Die zurückgegebene Textur kann ein anderes Format aufweisen als das, das durch das *Format* angegeben wird. Anwendungen sollten das Format der zurückgegebenen Textur überprüfen. Wenn D3DFMT \_ Unknown ist, wird das Format aus der Datei entnommen. Wenn D3DFMT \_ from \_ File ist, wird das Format genau wie in der Datei erstellt, und der-Rückruf schlägt fehl, wenn dies die Gerätefunktionen verletzt.

</dd> <dt>

*Pool* \[ in\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Textur platziert werden soll.

</dd> <dt>

*Filter* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einer oder mehreren [D3DX \_ Filter](d3dx-filter.md) -Konstanten, die Steuern, wie das Bild gefiltert wird. Die Angabe von [D3DX \_ default](other-d3dx-constants.md) für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.

</dd> <dt>

*MipFilter* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einer oder mehreren [D3DX \_ Filter](d3dx-filter.md) -Konstanten, die Steuern, wie das Bild gefiltert wird. Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Box. Verwenden Sie außerdem Bits 27-31, um die Anzahl der MIP-Ebenen anzugeben, die (vom oberen Rand der MipMap-Kette) übersprungen werden sollen, wenn eine DDS-Textur in den Arbeitsspeicher geladen wird. Dies ermöglicht es Ihnen, bis zu 32 Ebenen zu überspringen.

</dd> <dt>

*Colorkey* \[ in\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Farbschlüssel zu deaktivieren. Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist. Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden. Daher wäre der Wert für den Wert "0xFF000000" gleich.

</dd> <dt>

*psrcinfo* \[ in, out\]
</dt> <dd>

Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***

Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei ausgefüllt werden soll, oder **null**.

</dd> <dt>

*pPalette* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine zu füllende 256-Farbpalette darstellt, oder **null**.

</dd> <dt>

*pptexture* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, D3DXERR \_ InvalidData, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateTextureFromFileExW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXCreateTextureFromFileExA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

Verwenden Sie [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) , um zu bestimmen, ob das Gerät die Textur unter Berücksichtigung des aktuellen Zustands unterstützen kann.

Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA. Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

Für mipzugeordnete Texturen ist jede Ebene automatisch mit der geladenen Textur gefüllt. Beim Laden von Bildern in mipzugeordnete Texturen können einige Geräte nicht zu einem 1 x1-Bild wechseln, und diese Funktion schlägt fehl. Wenn dies der Fall ist, müssen die Images manuell geladen werden.

Optimale Leistung bei der Verwendung von **D3DXCreateTextureFromFileEx**:

1.  Die Bildskalierung und die Formatkonvertierung zur Ladezeit können langsam sein. Speichern Sie Images im Format und in der Lösung, die Sie verwenden werden. Wenn die Zielhardware eine Potenz von 2 Dimensionen erfordert, erstellen und speichern Sie Images mit zwei Dimensionen.
2.  Filtern Sie zum Erstellen von MipMap-Bildern zur Ladezeit mithilfe des [D3DX \_ Filter \_ ](d3dx-filter.md)Felds. Ein Feld Filter ist viel schneller als andere Filtertypen, z \_ . b. D3DX Filter \_ Dreieck.
3.  Verwenden Sie ggf. DDS-Dateien. Da DDS-Dateien verwendet werden können, um ein beliebiges Direct3D 9-Textur Format darzustellen, sind Sie für D3DX sehr leicht lesbar. Außerdem können Sie MipMaps speichern, sodass alle MipMap-Generierungs Algorithmen zum Erstellen der Images verwendet werden können.

Wenn Sie MipMap-Ebenen beim Laden einer DDS-Datei überspringen, verwenden \_ Sie das Makro D3DX Skip \_ DDS \_ MIP \_ Levels, um den MipFilter-Wert zu generieren. Dieses Makro nimmt die Anzahl der zu über springenden Ebenen und den Filtertyp an und gibt den Filter Wert zurück, der dann an den MipFilter-Parameter übergeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
</dt> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
