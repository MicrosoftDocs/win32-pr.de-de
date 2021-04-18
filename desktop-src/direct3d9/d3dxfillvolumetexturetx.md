---
description: Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language) zum Auffüllen der einzelnen texttabformationen einer Textur.
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: D3DXFillVolumeTextureTX-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: de310ee6171924a5d2b61071d47c421739f15833
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354370"
---
# <a name="d3dxfillvolumetexturetx-function"></a>D3DXFillVolumeTextureTX-Funktion

Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language) zum Auffüllen der einzelnen texttabformationen einer Textur.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptexture* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Zeiger auf ein [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) -Objekt, das die zu füllende Textur darstellt.

</dd> <dt>

*ptextureshader* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

Zeiger auf ein [**ID3DXTextureShader**](id3dxtextureshader.md) Texture-Shader-Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Das Textur Ziel muss eine HLSL-Funktion sein, die die folgende Semantik enthält:

-   Ein Eingabeparameter muss eine Positions Semantik verwenden.
-   Ein Eingabeparameter muss eine Psize-Semantik verwenden.
-   Die Funktion muss einen Parameter zurückgeben, der die Farb Semantik verwendet.

Die Eingabeparameter können in beliebiger Reihenfolge angegeben werden. Ein Beispiel finden Sie unter [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillTextureTX**](d3dxfilltexturetx.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
