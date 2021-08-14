---
description: Lädt ein Volume aus einer Datei im Arbeitsspeicher.
ms.assetid: d450b652-3a74-45ea-9506-e05da87821d7
title: D3DXLoadVolumeFromFileInMemory-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d24a550e4f07d0c82e6c114cb70eadf496b3bc3db312c27492b94112a8ca27c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525627"
---
# <a name="d3dxloadvolumefromfileinmemory-function"></a>D3DXLoadVolumeFromFileInMemory-Funktion

Lädt ein Volume aus einer Datei im Arbeitsspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadVolumeFromFileInMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcData,
  _In_       UINT              SrcDataSize,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDestVolume* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Zeiger auf eine [**IDirect3DVolume9-Schnittstelle.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) Gibt das Zielvolume an.

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

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf die Datei im Arbeitsspeicher, aus der das Volume geladen werden soll.

</dd> <dt>

*SrcDataSize* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Größe der Datei im Arbeitsspeicher in Bytes.

</dd> <dt>

*pSrcBox* \[ In\]
</dt> <dd>

Typ: **const [**D3DBOX**](d3dbox.md) \***

Zeiger auf eine [**D3DBOX-Struktur.**](d3dbox.md) Gibt das Quellfeld an. Legen Sie diesen Parameter auf **NULL** fest, um das gesamte Volume anzugeben.

</dd> <dt>

*Filterung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren [ \_ D3DX-FILTERN,](d3dx-filter.md)die steuern, wie das Bild gefiltert wird. Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht der Angabe von D3DX FILTER TRIANGLE \_ \_ \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*ColorKey* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR-Wert,**](d3dcolor.md) der durch transparentes Schwarz ersetzt werden soll, oder 0, um den Farbschlüssel zu deaktivieren. Dies ist immer eine 32-Bit-ARGB-Farbe, unabhängig vom Quellbildformat. Alpha ist von Bedeutung und sollte in der Regel für nicht transparente Farbschlüssel auf FF festgelegt werden. Daher wäre der Wert für nicht transparentes Schwarz gleich 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ In\]
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Zeiger auf eine [**D3DXIMAGE \_ INFO-Struktur,**](d3dximage-info.md) die mit einer Beschreibung der Daten in der Quellbilddatei gefüllt werden soll, oder **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Diese Funktion verarbeitet die Konvertierung in und aus komprimierten Texturformaten und unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga. Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Das Schreiben in eine Oberfläche ungleich 0 (null) der Volumentextur führt nicht dazu, dass das geänderte Rechteck aktualisiert wird. Wenn **D3DXLoadVolumeFromFileInMemory** aufgerufen wird und die Textur noch nicht geändert wurde (dies ist in normalen Verwendungsszenarien unwahrscheinlich), muss die Anwendung [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) explizit für die Volumetextur aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromMemory**](d3dxloadvolumefrommemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
