---
description: Lädt eine Oberfläche aus einer Datei.
ms.assetid: cbd360b6-6cee-418b-8c45-506e190eb2f6
title: D3DXLoadSurfaceFromFile-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44c06f0d88558fcb7692218cfe5aa98a2483fd1881dcab2f1d75f2c251bffb91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123058"
---
# <a name="d3dxloadsurfacefromfile-function"></a>D3DXLoadSurfaceFromFile-Funktion

Lädt eine Oberfläche aus einer Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadSurfaceFromFile(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCTSTR            pSrcFile,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
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

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*pSrcRect* \[ In\]
</dt> <dd>

Typ: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Zeiger auf eine [**RECT-Struktur.**](/previous-versions//dd162897(v=vs.85)) Gibt das Quellrechteck an. Legen Sie diesen Parameter auf **NULL** fest, um das gesamte Bild anzugeben.

</dd> <dt>

*Filterung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren [ \_ D3DX-FILTERN,](d3dx-filter.md) die steuern, wie das Bild gefiltert wird. Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht der Angabe von D3DX FILTER TRIANGLE \_ \_ \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*ColorKey* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR-Wert,**](d3dcolor.md) der durch transparentes Schwarz ersetzt werden soll, oder 0, um den Farbschlüssel zu deaktivieren. Dies ist immer eine 32-Bit-ARGB-Farbe, unabhängig vom Quellbildformat. Alpha ist von Bedeutung und sollte in der Regel für nicht transparente Farbschlüssel auf FF festgelegt werden. Bei opakem Schwarz ist der Wert also gleich 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Zeiger auf eine [**D3DXIMAGE \_ INFO-Struktur,**](d3dximage-info.md) die mit einer Beschreibung der Daten in der Quellbilddatei gefüllt werden soll, oder **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXLoadSurfaceFromFileW aufgelöst. Andernfalls wird der Funktionsaufruf in D3DXLoadSurfaceFromFileA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.

Diese Funktion verarbeitet die Konvertierung in und aus komprimierten Texturformaten und unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga. Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Das Schreiben in eine Oberfläche ungleich null führt nicht dazu, dass das geänderte Rechteck aktualisiert wird. Wenn **D3DXLoadSurfaceFromFile** aufgerufen wird und die Oberfläche noch nicht geändert wurde (dies ist in normalen Verwendungsszenarien unwahrscheinlich), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit auf der Oberfläche aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
