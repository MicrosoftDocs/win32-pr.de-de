---
description: Lädt ein Volume von einem anderen Volume.
ms.assetid: bc162f91-feb7-4571-ae4a-abaa5e7953f6
title: D3DXLoadVolumeFromVolume-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromVolume
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 634d455a0611faabd9005d674af920d1fccd67534eedd2dedba68d08678f9b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525321"
---
# <a name="d3dxloadvolumefromvolume-function"></a>D3DXLoadVolumeFromVolume-Funktion

Lädt ein Volume von einem anderen Volume.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadVolumeFromVolume(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPDIRECT3DVOLUME9 pSrcVolume,
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

*pSrcVolume* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Ein Zeiger auf eine [**IDirect3DVolume9-Schnittstelle.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) Gibt das Quellvolume an.

</dd> <dt>

*pSrcPalette* \[ In\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die Quellpalette von 256 Farben oder **NULL**.

</dd> <dt>

*pSrcBox* \[ In\]
</dt> <dd>

Typ: **const [**D3DBOX**](d3dbox.md) \***

Zeiger auf eine [**D3DBOX-Struktur.**](d3dbox.md) Gibt das Quellfeld an. Legen Sie diesen Parameter auf **NULL** fest, um das gesamte Volume anzugeben.

</dd> <dt>

*Filterung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren [ \_ D3DX-FILTERN,](d3dx-filter.md)die steuern, wie das Bild gefiltert wird. Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht der Angabe von D3DX FILTER TRIANGLE \_ \_ \| D3DX \_ FILTER \_ DITHER.

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

Das Schreiben in eine Oberfläche ungleich 0 (null) der Volumentextur führt nicht dazu, dass das geänderte Rechteck aktualisiert wird. Wenn **D3DXLoadVolumeFromVolume** aufgerufen wird und die Oberfläche noch nicht geändert wurde (dies ist in normalen Verwendungsszenarien unwahrscheinlich), muss die Anwendung [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) explizit auf der Oberfläche aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromFileInMemory**](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromMemory**](d3dxloadvolumefrommemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
