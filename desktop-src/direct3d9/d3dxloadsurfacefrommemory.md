---
description: Lädt eine Oberfläche aus dem Arbeitsspeicher.
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: D3DXLoadSurfaceFromMemory-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: ffb7be05301ae807505242153be902ab30eecf14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050836"
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

*pdestsurface* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Zeiger auf eine [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle. Gibt die Ziel Oberfläche an, die das Bild empfängt.

</dd> <dt>

*pdestpalette* \[ in\]
</dt> <dd>

Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Ziel Palette von 256 Farben oder **null**.

</dd> <dt>

*pdestrect* \[ in\]
</dt> <dd>

Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur. Gibt das Ziel Rechteck an. Legen Sie diesen Parameter auf **null** fest, um die gesamte Oberfläche anzugeben.

</dd> <dt>

*psrcmemory* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Ein Zeiger auf die linke obere Ecke des Quell Bilds im Arbeitsspeicher.

</dd> <dt>

*Srcformat* \[ in\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, das Pixel Format des Quell Bilds.

</dd> <dt>

*Srcpitch* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Darstellung des Quell Bilds in Bytes. Bei DXT-Formaten sollte diese Zahl die Breite einer Zellen Zelle in Bytes darstellen.

</dd> <dt>

*psrcpalette* \[ in\]
</dt> <dd>

Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Quell Palette von 256 Farben oder **null**.

</dd> <dt>

*psrcrect* \[ in\]
</dt> <dd>

Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur. Gibt die Dimensionen des Quell Bilds im Arbeitsspeicher an. Dieser Wert darf nicht **null** sein.

</dd> <dt>

*Filter* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird. Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.

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

Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.

Das Schreiben in eine Oberfläche ohne Ebene bewirkt nicht, dass das geänderte Rechteck aktualisiert wird. Wenn **D3DXLoadSurfaceFromMemory** aufgerufen wird und die Oberfläche nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit auf der-Oberfläche aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
