---
description: Verwendet eine vom Benutzer bereitgestellte Funktion, um jedes Texel jeder Mip-Ebene einer bestimmten Volumentextur zu füllen.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: D3DXFillVolumeTexture-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e0ef21c3fb9b5443cc488a3b6fc953953cffee6e5d0dc417dee69969907f86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123290"
---
# <a name="d3dxfillvolumetexture-function"></a>D3DXFillVolumeTexture-Funktion

Verwendet eine vom Benutzer bereitgestellte Funktion, um jedes Texel jeder Mip-Ebene einer bestimmten Volumentextur zu füllen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Zeiger auf eine [**IDirect3DVolumeTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) die die gefüllte Textur darstellt.

</dd> <dt>

*pFunction* \[ In\]
</dt> <dd>

Typ: **[LPD3DXFILL3D](lpd3dxfill3d.md)**

Zeiger auf eine vom Benutzer bereitgestellte Auswertungsfunktion, die verwendet wird, um den Wert der einzelnen Texel zu berechnen. Die -Funktion folgt dem Prototyp von [LPD3DXFILL3D.](lpd3dxfill3d.md)

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen beliebigen Block benutzerdefinierter Daten. Dieser Zeiger wird an die funktion übergeben, die in *pFunction* bereitgestellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Wenn das Volume nicht dynamisch ist (da die Nutzung beim Erstellen auf 0 festgelegt ist) und sich im Videospeicher befindet (der Speicherpool ist auf D3DPOOL \_ DEFAULT festgelegt), schlägt **D3DXFillVolumeTexture** fehl, da das Volume nicht gesperrt werden kann.

In diesem Beispiel wird eine Funktion namens ColorVolumeFill erstellt, die auf D3DXFillVolumeTexture basiert.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
{
       return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
