---
description: 'D3DXComputeNormalMap-Funktion: Konvertiert eine Höhenkarte in eine normale Karte. Die (x,y,z)-Komponenten jedes Normals werden den (r,g,b)-Kanälen der Ausgabetextur zugeordnet.'
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
ms.openlocfilehash: 920ad763f478a2e6bcb9fbe98cc7e2a677ebe783
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105228"
---
# <a name="d3dxcomputenormalmap-function"></a>D3DXComputeNormalMap-Funktion

Konvertiert eine Höhenkarte in eine normale Karte. Die (x,y,z)-Komponenten jedes Normals werden den (r,g,b)-Kanälen der Ausgabetextur zugeordnet.

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

Zeiger auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die die Textur der Quellhöhenzuordnung darstellt.

</dd> <dt>

*pSrcPalette* \[ In\]
</dt> <dd>

Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Zeiger auf einen [**PALETTEENTRY-Typ,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) der die Quellpalette mit 256 Farben oder **NULL enthält.**

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Mindestens ein [D3DX \_ NORMALMAP-Flag,](d3dx-normalmap.md) das die Generierung normaler Karten kontrolliert.

</dd> <dt>

*Kanal* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Ein [D3DX \_ CHANNEL-Flag,](d3dx-channel.md) das die Quelle der Höheninformationen an gibt.

</dd> <dt>

*Amplitude* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Konstanter Wertmultiplikator, der die Werte in der normalen Zuordnung erhöht (oder verringert). Höhere Werte machen Bumps in der Regel sichtbarer, niedrigere Werte machen Bumps in der Regel weniger sichtbar.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Wert sein: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Bemerkungen

Diese Methode berechnet die Normalität mithilfe des zentralen Unterschieds mit einer Kernelgröße von 3x3. Der zentrale differenzierende Nenner ist 2.0. RGB-Kanäle im Ziel enthalten voreingenommene (x,y,z)-Komponenten der Normalen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
