---
description: 'D3DXFillVolumeTextureTX-Funktion: Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language), um jeden Texel jeder Mipmapebene einer Textur aufzufüllen.'
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: D3DXFillVolumeTextureTX-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30aac53aa6451885bbd4ae2cac63050b01157974
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107628"
---
# <a name="d3dxfillvolumetexturetx-function"></a>D3DXFillVolumeTextureTX-Funktion

Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language), um jeden Texel jeder Mipmapebene einer Textur zu füllen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Zeiger auf ein [**IDirect3DVolumeTexture9-Objekt,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) das die zu füllende Textur darstellt.

</dd> <dt>

*pTextureShader* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

Zeiger auf ein [**ID3DXTextureShader-Texturshaderobjekt.**](id3dxtextureshader.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Bemerkungen

Das Texturziel muss eine HLSL-Funktion sein, die die folgende Semantik enthält:

-   Ein Eingabeparameter muss eine POSITION-Semantik verwenden.
-   Ein Eingabeparameter muss eine PSIZE-Semantik verwenden.
-   Die Funktion muss einen Parameter zurückgeben, der die COLOR-Semantik verwendet.

Die Eingabeparameter können in beliebiger Reihenfolge angegeben werden. Ein Beispiel finden Sie unter [ **D3DXFillTextureTX.**](d3dxfilltexturetx.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillTextureTX**](d3dxfilltexturetx.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
