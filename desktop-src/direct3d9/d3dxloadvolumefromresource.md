---
description: Lädt ein Volume aus einer Ressource.
ms.assetid: 3fa1243b-5e31-4737-8d3c-08852d6528d9
title: D3DXLoadVolumeFromResource-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d57ce492db24ac9920662d4de5baed4650dd801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365070"
---
# <a name="d3dxloadvolumefromresource-function"></a>D3DXLoadVolumeFromResource-Funktion

Lädt ein Volume aus einer Ressource.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadVolumeFromResource(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       HMODULE           hSrcModule,
  _In_       LPCSTR            pSrcResource,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdestvolume* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Zeiger auf eine [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) -Schnittstelle. Gibt das Ziel Volume an.

</dd> <dt>

*pdestpalette* \[ in\]
</dt> <dd>

Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Ziel Palette von 256 Farben oder **null**.

</dd> <dt>

*pdestbox* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***

Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur. Gibt das Zielfeld an. Legen Sie diesen Parameter auf **null** fest, um das gesamte Volume anzugeben.

</dd> <dt>

*hsrcmodule* \[ in\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle für das Modul, in dem sich die Ressource befindet, oder **null** für das Modul, das dem Image zugeordnet ist, mit dem das Betriebssystem den aktuellen Prozess erstellt hat.

</dd> <dt>

*psrkresource* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ein Zeiger auf eine Zeichenfolge, die den Dateinamen des Quell Bilds angibt. Wenn Unicode oder \_ Unicode definiert ist, ist dieser Parametertyp LPCWSTR; andernfalls lautet der Typ LPCSTR.

</dd> <dt>

*psrcbox* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***

Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur. Gibt das Quellfeld an. Legen Sie diesen Parameter auf **null** fest, um das gesamte Volume anzugeben.

</dd> <dt>

*Filter* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md), um die Filterung des Bilds zu steuern. Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.

</dd> <dt>

*Colorkey* \[ in\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren. Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist. Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden. Daher wäre der Wert für den Wert "0xFF000000" gleich.

</dd> <dt>

*psrcinfo* \[ in\]
</dt> <dd>

Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***

Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei gefüllt werden soll, oder **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Die Ressource, die geladen wird, muss eine Bitmap-Ressource (RT \_ Bitmap) sein.

Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.

Das Schreiben auf eine Oberfläche ohne Ebene der volumetextur bewirkt nicht, dass das geänderte Rechteck aktualisiert wird. Wenn [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) aufgerufen wird und die Textur nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**IDirect3DVolumeTexture9:: adddirtybox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) explizit auf der volumetextur aufrufen.

Diese Funktion unterstützt sowohl Unicode-als auch ANSI-Zeichen folgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromFileInMemory**](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromMemory**](d3dxloadvolumefrommemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
