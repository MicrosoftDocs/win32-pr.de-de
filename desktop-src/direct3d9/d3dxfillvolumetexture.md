---
description: Verwendet eine vom Benutzer bereitgestellte Funktion, um jedes texsebene jeder MIP-Ebene einer bestimmten volumetextur auszufüllen.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: D3DXFillVolumeTexture-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: d817470f0f0617001fd83054e24e8881ac9a3a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354857"
---
# <a name="d3dxfillvolumetexture-function"></a>D3DXFillVolumeTexture-Funktion

Verwendet eine vom Benutzer bereitgestellte Funktion, um jedes texsebene jeder MIP-Ebene einer bestimmten volumetextur auszufüllen.

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

*ptexture* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Zeiger auf eine [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) -Schnittstelle, die die gefüllte Textur darstellt.

</dd> <dt>

*pfunction* \[ in\]
</dt> <dd>

Typ: **[LPD3DXFILL3D](lpd3dxfill3d.md)**

Ein Zeiger auf eine vom Benutzer bereitgestellte Auswertungsfunktion, die verwendet wird, um den Wert der einzelnen Texttypen zu berechnen. Die-Funktion folgt dem Prototyp von [LPD3DXFILL3D](lpd3dxfill3d.md).

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen beliebigen Block von benutzerdefinierten Daten. Dieser Zeiger wird an die Funktion übergeben, die in *pfunction* bereitgestellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Wenn das Volume nicht dynamisch ist (weil die Verwendung bei der Erstellung auf 0 festgelegt ist) und sich im Videospeicher befindet (der auf D3DPOOL default festgelegte Speicherpool \_ ), schlägt **D3DXFillVolumeTexture** fehl, da das Volume nicht gesperrt werden kann.

In diesem Beispiel wird eine Funktion namens colorvolumefill erstellt, die auf D3DXFillVolumeTexture basiert.


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
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
