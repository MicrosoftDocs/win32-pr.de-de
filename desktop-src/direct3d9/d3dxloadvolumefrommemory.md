---
description: Lädt ein Volume aus dem Arbeitsspeicher.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: D3DXLoadVolumeFromMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d6c3f1bdfe40f19eeb57b4f0d8a38c40a239404
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355781"
---
# <a name="d3dxloadvolumefrommemory-function"></a>D3DXLoadVolumeFromMemory-Funktion

Lädt ein Volume aus dem Arbeitsspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdestvolume* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Zeiger auf eine [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) -Schnittstelle. Gibt das Ziel Volume an, das das Abbild empfängt.

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

*psrcmemory* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Zeiger auf die linke obere Ecke des Quell Volumes im Arbeitsspeicher.

</dd> <dt>

*Srcformat* \[ in\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, das Pixel Format des Quell Volume.

</dd> <dt>

*Srcrowpitch* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Darstellung des Quell Bilds in Bytes. Bei DXT-Formaten (komprimierte Textur Formate) sollte diese Zahl die Größe einer Zellen Zelle in Bytes darstellen.

</dd> <dt>

*Srcslicepitch* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Darstellung des Quell Bilds in Bytes. Bei DXT-Formaten (komprimierte Textur Formate) sollte diese Zahl die Größe eines Slice von Zellen in Bytes darstellen.

</dd> <dt>

*psrcpalette* \[ in\]
</dt> <dd>

Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Quell Palette von 256 Farben oder **null**.

</dd> <dt>

*psrcbox* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***

Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur. Gibt das Quellfeld an. **Null** ist kein gültiger Wert für diesen Parameter.

</dd> <dt>

*Filter* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird. Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.

</dd> <dt>

*Colorkey* \[ in\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren. Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist. Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden. Daher wäre der Wert für den Wert "0xFF000000" gleich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Das Schreiben auf eine Oberfläche ohne Ebene der volumetextur bewirkt nicht, dass das geänderte Rechteck aktualisiert wird. Wenn **D3DXLoadVolumeFromMemory** aufgerufen wird und die Textur nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**IDirect3DVolumeTexture9:: adddirtybox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) explizit auf der volumetextur aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
