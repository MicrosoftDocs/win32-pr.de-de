---
description: Lädt ein Volume aus dem Arbeitsspeicher.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: D3DXLoadVolumeFromMemory-Funktion (D3dx9tex.h)
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
ms.openlocfilehash: c473d5194a20a7de7e20d76fbde18d0a974ff8f314dc93822f57bfef2a4a6a5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122964"
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

*pDestVolume* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Zeiger auf eine [**IDirect3DVolume9-Schnittstelle.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) Gibt das Zielvolume an, das das Image empfängt.

</dd> <dt>

*pDestPalette* \[ In\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die Zielpalette mit 256 Farben oder **NULL**.

</dd> <dt>

*pDestBox* \[ In\]
</dt> <dd>

Typ: **const [**D3DBOX**](d3dbox.md) \***

Zeiger auf eine [**D3DBOX-Struktur.**](d3dbox.md) Gibt das Zielfeld an. Legen Sie diesen Parameter auf **NULL** fest, um das gesamte Volume anzugeben.

</dd> <dt>

*pSrcMemory* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf die linke obere Ecke des Quellvolumes im Arbeitsspeicher.

</dd> <dt>

*SrcFormat* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT-Enumerationstyps,](d3dformat.md) das Pixelformat des Quellvolumes.

</dd> <dt>

*SrcRowPitch* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Tonhöhe des Quellbilds in Bytes. Bei DXT-Formaten (komprimierte Texturformate) sollte diese Zahl die Größe einer Zellenzeile in Bytes darstellen.

</dd> <dt>

*SrcSlicePitch* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Tonhöhe des Quellbilds in Bytes. Bei DXT-Formaten (komprimierte Texturformate) sollte diese Zahl die Größe eines Zellensegments in Bytes darstellen.

</dd> <dt>

*pSrcPalette* \[ In\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die Quellpalette von 256 Farben oder **NULL**.

</dd> <dt>

*pSrcBox* \[ In\]
</dt> <dd>

Typ: **const [**D3DBOX**](d3dbox.md) \***

Zeiger auf eine [**D3DBOX-Struktur.**](d3dbox.md) Gibt das Quellfeld an. **NULL** ist kein gültiger Wert für diesen Parameter.

</dd> <dt>

*Filterung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren [ \_ D3DX-FILTERN,](d3dx-filter.md) die steuern, wie das Bild gefiltert wird. Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht der Angabe von D3DX FILTER TRIANGLE \_ \_ \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*ColorKey* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR-Wert,**](d3dcolor.md) der durch transparentes Schwarz ersetzt werden soll, oder 0, um den Farbschlüssel zu deaktivieren. Dies ist immer eine 32-Bit-ARGB-Farbe, unabhängig vom Quellbildformat. Alpha ist von Bedeutung und sollte in der Regel für nicht transparente Farbschlüssel auf FF festgelegt werden. Daher wäre der Wert für nicht transparentes Schwarz gleich 0xFF000000.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Das Schreiben in eine Oberfläche ungleich 0 (null) der Volumentextur führt nicht dazu, dass das geänderte Rechteck aktualisiert wird. Wenn **D3DXLoadVolumeFromMemory** aufgerufen wird und die Textur nicht bereits geändert wurde (dies ist in normalen Verwendungsszenarien unwahrscheinlich), muss die Anwendung [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) explizit für die Volumetextur aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
