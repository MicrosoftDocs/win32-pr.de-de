---
description: Lädt eine Oberfläche aus dem Arbeitsspeicher.
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: D3DXLoadSurfaceFromMemory-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1b2bcb98f5fd64da221f73bf2cee4222d8925797acd4c7e01914e8e068d6e381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123048"
---
# <a name="d3dxloadsurfacefrommemory-function"></a>D3DXLoadSurfaceFromMemory-Funktion

Lädt eine Oberfläche aus dem Arbeitsspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadSurfaceFromMemory(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPCVOID            pSrcMemory,
  _In_       D3DFORMAT          SrcFormat,
  _In_       UINT               SrcPitch,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDestSurface* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Zeiger auf eine [**IDirect3DSurface9-Schnittstelle.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) Gibt die Zieloberfläche an, die das Bild empfängt.

</dd> <dt>

*pDestPalette* \[ In\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die Zielpalette mit 256 Farben oder **NULL.**

</dd> <dt>

*pDestRect* \[ In\]
</dt> <dd>

Typ: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Zeiger auf eine [**RECT-Struktur.**](/previous-versions//dd162897(v=vs.85)) Gibt das Zielrechteck an. Legen Sie diesen Parameter auf **NULL fest,** um die gesamte Oberfläche anzugeben.

</dd> <dt>

*pSrcMemory* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf die linke obere Ecke des Quellbilds im Arbeitsspeicher.

</dd> <dt>

*SrcFormat* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [aufzählten D3DFORMAT-Typs,](d3dformat.md) das Pixelformat des Quellbilds.

</dd> <dt>

*SrcPitch* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Tonhöhe des Quellbilds in Bytes. Bei DXT-Formaten sollte diese Zahl die Breite einer Zellenzeile in Bytes darstellen.

</dd> <dt>

*pSrcPalette* \[ In\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die Quellpalette mit 256 Farben oder **NULL.**

</dd> <dt>

*pSrcRect* \[ In\]
</dt> <dd>

Typ: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Zeiger auf eine [**RECT-Struktur.**](/previous-versions//dd162897(v=vs.85)) Gibt die Dimensionen des Quellbilds im Arbeitsspeicher an. Dieser Wert darf nicht **NULL sein.**

</dd> <dt>

*Filter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus mindestens einem [D3DX-FILTER, \_ ](d3dx-filter.md) der steuert, wie das Bild gefiltert wird. Die Angabe von D3DX DEFAULT für diesen Parameter entspricht der Angabe von \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*ColorKey* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR-Wert,**](d3dcolor.md) der durch transparentes Schwarz ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren. Dies ist immer eine 32-Bit-ARGB-Farbe, unabhängig vom Quellbildformat. Alpha ist wichtig und sollte für nicht transparente Farbtasten in der Regel auf FF festgelegt werden. Daher wäre der Wert für opakes Schwarz gleich 0xFF000000.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Diese Funktion verarbeitet die Konvertierung in und aus komprimierten Texturformaten.

Das Schreiben auf eine Oberfläche ohne Ebene 0 (null) verursacht keine Aktualisierung des geänderten Rechtecks. Wenn **D3DXLoadSurfaceFromMemory** aufgerufen wird und die Oberfläche noch nicht angepasst wurde (dies ist in normalen Verwendungsszenarien unwahrscheinlich), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit auf der Oberfläche aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
