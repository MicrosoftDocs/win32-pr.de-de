---
description: Verwendet eine vom Benutzer bereitgestellte Funktion, um die einzelnen texttaten der MIP-Ebene einer angegebenen cubetextur auszufüllen.
ms.assetid: 0390a1b6-6675-42e1-bc45-65dd7b2d83c5
title: D3DXFillCubeTexture-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9fda70aa42d6982c40eb1ec926b6823e7ac7d997
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351950"
---
# <a name="d3dxfillcubetexture-function"></a>D3DXFillCubeTexture-Funktion

Verwendet eine vom Benutzer bereitgestellte Funktion, um die einzelnen texttaten der MIP-Ebene einer angegebenen cubetextur auszufüllen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFillCubeTexture(
  _Out_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D           pFunction,
  _In_  LPVOID                 pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptexture* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Zeiger auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die die gefüllte Textur darstellt.

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

Im folgenden Beispiel wird eine Funktion namens colorcubefill erstellt, die auf D3DXFillCubeTexture basiert.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorCubeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill the texture using D3DXFillCubeTexture
if (FAILED (hr = D3DXFillCubeTexture (m_pTexture, ColorCubeFill, NULL)))
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

 

 
