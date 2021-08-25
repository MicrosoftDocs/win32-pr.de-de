---
description: Verwendet eine vom Benutzer bereitgestellte Funktion, um jedes Texel jeder MIP-Ebene einer bestimmten Textur zu füllen.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: D3DXFillTexture-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28df3b7396ea0c34c39a87d2285f565f25d6ff6dc89dcfb8613890e79c4c5cf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849770"
---
# <a name="d3dxfilltexture-function"></a>D3DXFillTexture-Funktion

Verwendet eine vom Benutzer bereitgestellte Funktion, um jedes Texel jeder MIP-Ebene einer bestimmten Textur zu füllen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die die gefüllte Textur darstellt.

</dd> <dt>

*pFunction* \[ In\]
</dt> <dd>

Typ: **[LPD3DXFILL2D](lpd3dxfill2d.md)**

Zeiger auf eine vom Benutzer bereitgestellte Auswertungsfunktion, die zum Berechnen des Werts der einzelnen Texel verwendet wird. Die Funktion folgt dem Prototyp von [LPD3DXFILL2D.](lpd3dxfill2d.md)

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen beliebigen Block benutzerdefinierter Daten. Dieser Zeiger wird an die in *pFunction bereitgestellte Funktion übergeben.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Hier ist ein Beispiel, in dem eine Funktion namens ColorFill erstellt wird, die auf D3DXFillTexture basiert.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
