---
description: Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language) zum Auffüllen der einzelnen texttabformationen einer Textur.
ms.assetid: a0c36967-57e6-4771-8e9f-f32949c12001
title: D3DXFillCubeTextureTX-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 37a831ef95d50f9b0389be0f1c9937e46748f6d3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762048"
---
# <a name="d3dxfillcubetexturetx-function"></a>D3DXFillCubeTextureTX-Funktion

Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language) zum Auffüllen der einzelnen texttabformationen einer Textur.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptexture* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Zeiger auf ein [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Objekt, das die zu füllende Textur darstellt.

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

[**D3DXFillVolumeTextureTX**](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
