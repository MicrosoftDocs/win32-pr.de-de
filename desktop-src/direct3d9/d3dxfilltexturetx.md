---
description: Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language) zum Auffüllen der einzelnen texttabformationen einer Textur.
ms.assetid: 013660ce-865e-4acf-a1ea-670e70377ff5
title: D3DXFillTextureTX-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3605011f7967edec68d13405b4cabbd9c90d4c59
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050854"
---
# <a name="d3dxfilltexturetx-function"></a>D3DXFillTextureTX-Funktion

Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language) zum Auffüllen der einzelnen texttabformationen einer Textur.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptexture* \[ in, out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Objekt, das die zu füllende Textur darstellt.

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

Im folgenden finden Sie ein Beispiel für eine solche HLSL-Funktion:


```
float4 TextureGradientFill(
  float2 vTexCoord : POSITION, 
  float2 vTexelSize : PSIZE) : COLOR 
  {
    float r,g, b, xSq,ySq, a;
    xSq = 2.f*vTexCoord.x-1.f; xSq *= xSq;
    ySq = 2.f*vTexCoord.y-1.f; ySq *= ySq;
    a = sqrt(xSq+ySq);
    if (a > 1.0f) {
        a = 1.0f-(a-1.0f);
    }
    else if (a < 0.2f) {
        a = 0.2f;
    }
    r = 1-vTexCoord.x;
    g = 1-vTexCoord.y;
    b = vTexCoord.x;
    return float4(r, g, b, a);
    
  };
```



Beachten Sie, dass die Eingabeparameter in beliebiger Reihenfolge vorliegen können, aber beide Eingabe Semantik muss dargestellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> <dt>

[**D3DXFillVolumeTextureTX**](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
