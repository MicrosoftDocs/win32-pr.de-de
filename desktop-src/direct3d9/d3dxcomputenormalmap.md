---
description: 'D3DXComputeNormalMap-Funktion: Konvertiert eine Höhenkarte in eine normale Karte. Die (x,y,z)-Komponenten jeder Normalen werden den (r,g,b)-Kanälen der Ausgabetextur zugeordnet.'
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: D3DXComputeNormalMap-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b561189c0aaafa42cc877246bb5a666ac26853133c227aa6c7a4f8beb1f23a28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299364"
---
# <a name="d3dxcomputenormalmap-function"></a>D3DXComputeNormalMap-Funktion

Konvertiert eine Höhenkarte in eine normale Karte. Die (x,y,z)-Komponenten jeder Normalen werden den (r,g,b)-Kanälen der Ausgabetextur zugeordnet.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die die Zieltextur darstellt.

</dd> <dt>

*pSrcTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die die Quelltextur der Höhenkarte darstellt.

</dd> <dt>

*pSrcPalette* \[ In\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf einen [**PALETTEENTRY-Typ,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) der die Quellpalette von 256 Farben oder **NULL** enthält.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Mindestens ein [D3DX \_ NORMALMAP-Flag,](d3dx-normalmap.md) das die Generierung normaler Zuordnungen steuert.

</dd> <dt>

*Kanal* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Ein [D3DX \_ CHANNEL-Flag,](d3dx-channel.md) das die Quelle der Höheninformationen angibt.

</dd> <dt>

*Amplitude* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Konstanter Wertmultiplikator, der die Werte in der normalen Zuordnung erhöht (oder verringert). Höhere Werte machen Bumps in der Regel sichtbarer, niedrigere Werte machen Bumps in der Regel weniger sichtbar.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Wert sein: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Diese Methode berechnet die Normalität mithilfe des zentralen Unterschieds mit einer Kernelgröße von 3x3. Der zentrale differenzierende Nenner ist 2.0. RGB-Kanäle im Ziel enthalten voreingenommene (x,y,z)-Komponenten der Normalen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
