---
description: Lädt eine Oberfläche von einer anderen Oberfläche mit Farbkonvertierung.
ms.assetid: eddb420d-fd32-4c09-afec-435887c4e905
title: D3DXLoadSurfaceFromSurface-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28f239fb57ec0bccec120c5b2ea493a094e9cc6acc5b47fb19e9f7495ecde46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495310"
---
# <a name="d3dxloadsurfacefromsurface-function"></a>D3DXLoadSurfaceFromSurface-Funktion

Lädt eine Oberfläche von einer anderen Oberfläche mit Farbkonvertierung.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadSurfaceFromSurface(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPDIRECT3DSURFACE9 pSrcSurface,
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

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die Zielpalette mit 256 Farben oder **NULL**.

</dd> <dt>

*pDestRect* \[ In\]
</dt> <dd>

Typ: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Zeiger auf eine [**RECT-Struktur.**](/previous-versions//dd162897(v=vs.85)) Gibt das Zielrechteck an. Legen Sie diesen Parameter auf **NULL** fest, um die gesamte Oberfläche anzugeben.

</dd> <dt>

*pSrcSurface* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Zeiger auf eine [**IDirect3DSurface9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) die die Quelloberfläche darstellt.

</dd> <dt>

*pSrcPalette* \[ In\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die Quellpalette von 256 Farben oder **NULL**.

</dd> <dt>

*pSrcRect* \[ In\]
</dt> <dd>

Typ: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Zeiger auf eine [**RECT-Struktur.**](/previous-versions//dd162897(v=vs.85)) Gibt das Quellrechteck an. Legen Sie diesen Parameter auf **NULL** fest, um die gesamte Oberfläche anzugeben.

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

Diese Funktion verarbeitet die Konvertierung in und aus komprimierten Texturformaten.

Das Schreiben in eine Oberfläche ungleich null führt nicht dazu, dass das geänderte Rechteck aktualisiert wird. Wenn **D3DXLoadSurfaceFromSurface** aufgerufen wird und die Oberfläche nicht bereits geändert wurde (dies ist in normalen Verwendungsszenarien unwahrscheinlich), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit auf der Oberfläche aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
