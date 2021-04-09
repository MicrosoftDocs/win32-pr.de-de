---
description: Erstellt eine cubetextur aus einer Datei im Arbeitsspeicher. Dies ist eine erweiterte Funktion als D3DXCreateCubeTextureFromFileInMemory.
ms.assetid: 598016eb-9ea9-4dca-a297-5708a957da6a
title: D3DXCreateCubeTextureFromFileInMemoryEx-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7813d4532bbde18a5fc7fd7d1d090dc72eccd61f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050920"
---
# <a name="d3dxcreatecubetexturefromfileinmemoryex-function"></a>D3DXCreateCubeTextureFromFileInMemoryEx-Funktion

Erstellt eine cubetextur aus einer Datei im Arbeitsspeicher. Dies ist eine erweiterte Funktion als [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    LPCVOID                pSrcData,
  _In_    UINT                   SrcDataSize,
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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der cubetextur zugeordnet werden soll.

</dd> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Ein Zeiger auf die Datei im Arbeitsspeicher, von der die cubetextur erstellt werden soll. Siehe Hinweise.

</dd> <dt>

*Srcdatasize* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Größe der Datei im Arbeitsspeicher in Bytes.

</dd> <dt>

*Größe* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Breite (oder Höhe) in Pixel. Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen.

</dd> <dt>

*Miplevels* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der angeforderten Mip-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.

</dd> <dt>

*Verwendung* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ renderTarget oder D3DUSAGE \_ Dynamic. Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll. Die Ressource kann dann an den *pnewrendertarget* -Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden. Wenn D3DUSAGE \_ renderTarget angegeben ist, muss die Anwendung überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt. Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen](performance-optimizations.md).

</dd> <dt>

*Format* \[ in\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die cubetextur beschreibt. Die zurückgegebene Textur kann ein anderes Format aufweisen als das, das durch das *Format* angegeben wird. Anwendungen sollten das Format der zurückgegebenen Textur überprüfen. Wenn [D3DFMT \_ Unknown](other-d3dx-constants.md)ist, wird das Format aus der Datei entnommen. Wenn D3DFMT \_ from \_ File ist, wird das Format genau wie in der Datei erstellt, und der-Rückruf schlägt fehl, wenn dies die Gerätefunktionen verletzt.

</dd> <dt>

*Pool* \[ in\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Cubestruktur platziert werden soll.

</dd> <dt>

*Filter* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird. Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.

</dd> <dt>

*MipFilter* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird. Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Box. Verwenden Sie außerdem Bits 27-31, um die Anzahl der MIP-Ebenen anzugeben, die (vom oberen Rand der MipMap-Kette) übersprungen werden sollen, wenn eine DDS-Textur in den Arbeitsspeicher geladen wird. Dies ermöglicht es Ihnen, bis zu 32 Ebenen zu überspringen.

</dd> <dt>

*Colorkey* \[ in\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren. Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist. Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden. Daher wäre der Wert für den Wert "0xFF000000" gleich.

</dd> <dt>

*psrcinfo* \[ in, out\]
</dt> <dd>

Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***

Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei gefüllt werden soll, oder **null**.

</dd> <dt>

*pPalette* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine zu füllende 256-Farbpalette darstellt, oder **null**. Siehe Hinweise.

</dd> <dt>

*ppcubetexture* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die das erstellte Cube-Textur Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, D3DXERR \_ InvalidData, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA. Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

Cube-Texturen unterscheiden sich von anderen Oberflächen darin, dass es sich um Auflistungen von Um "*" mit einer cubetextur aufzurufen, müssen Sie ein einzelnes Gesicht [**mithilfe von "**](/windows/desktop/api) [**getcubemapsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) " auswählen und die resultierende Oberfläche an " **strendertarget** " übergeben.

Diese Methode ist für das Laden von Bilddateien konzipiert, die als RT \_ RCDATA gespeichert werden. Dies ist eine Anwendungs definierte Ressource (Rohdaten). Andernfalls schlägt diese Methode fehl.

Ausführliche Informationen zu [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)finden Sie unter Platform SDK. Beachten Sie, dass der Member "Peer Flags" der **PaletteEntry** -Struktur ab DirectX 8,0 nicht wie im Platform SDK dokumentiert funktioniert. Der peflags-Member ist nun der Alphakanal für 8-Bit-Paletten-Formate.

**D3DXCreateCubeTextureFromFileInMemoryEx** verwendet das DDS-Dateiformat (DirectDraw Surface). Mit dem DirectX-Textur-Editor (Dxtex.exe) können Sie eine cubemap aus anderen Dateiformaten generieren und im DDS-Dateiformat speichern. Sie erhalten Dxtex.exe und erfahren mehr über das DirectX SDK. Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

Wenn Sie MipMap-Ebenen beim Laden einer DDS-Datei überspringen, verwenden \_ Sie das Makro D3DX Skip \_ DDS \_ MIP \_ Levels, um den MipFilter-Wert zu generieren. Dieses Makro nimmt die Anzahl der zu über springenden Ebenen und den Filtertyp an und gibt den Filter Wert zurück, der dann an den MipFilter-Parameter übergeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
