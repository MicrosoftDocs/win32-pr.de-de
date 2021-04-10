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
# <a name="d3dxfilltexturetx-function"></a><span data-ttu-id="2d3bb-103">D3DXFillTextureTX-Funktion</span><span class="sxs-lookup"><span data-stu-id="2d3bb-103">D3DXFillTextureTX function</span></span>

<span data-ttu-id="2d3bb-104">Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language) zum Auffüllen der einzelnen texttabformationen einer Textur.</span><span class="sxs-lookup"><span data-stu-id="2d3bb-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d3bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d3bb-105">Syntax</span></span>


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="2d3bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d3bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d3bb-107">*ptexture* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2d3bb-107">*pTexture* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d3bb-108">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="2d3bb-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="2d3bb-109">Zeiger auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Objekt, das die zu füllende Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="2d3bb-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="2d3bb-110">*ptextureshader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d3bb-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d3bb-111">Typ: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="2d3bb-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="2d3bb-112">Zeiger auf ein [**ID3DXTextureShader**](id3dxtextureshader.md) Texture-Shader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2d3bb-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d3bb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d3bb-113">Return value</span></span>

<span data-ttu-id="2d3bb-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d3bb-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d3bb-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2d3bb-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2d3bb-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="2d3bb-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d3bb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d3bb-117">Remarks</span></span>

<span data-ttu-id="2d3bb-118">Das Textur Ziel muss eine HLSL-Funktion sein, die die folgende Semantik enthält:</span><span class="sxs-lookup"><span data-stu-id="2d3bb-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="2d3bb-119">Ein Eingabeparameter muss eine Positions Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="2d3bb-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="2d3bb-120">Ein Eingabeparameter muss eine Psize-Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="2d3bb-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="2d3bb-121">Die Funktion muss einen Parameter zurückgeben, der die Farb Semantik verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d3bb-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="2d3bb-122">Im folgenden finden Sie ein Beispiel für eine solche HLSL-Funktion:</span><span class="sxs-lookup"><span data-stu-id="2d3bb-122">The following is an example of such an HLSL function:</span></span>


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



<span data-ttu-id="2d3bb-123">Beachten Sie, dass die Eingabeparameter in beliebiger Reihenfolge vorliegen können, aber beide Eingabe Semantik muss dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2d3bb-123">Note that the input parameters can be in any order, but both input semantics must be represented.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d3bb-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d3bb-124">Requirements</span></span>



| <span data-ttu-id="2d3bb-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d3bb-125">Requirement</span></span> | <span data-ttu-id="2d3bb-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2d3bb-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d3bb-127">Header</span><span class="sxs-lookup"><span data-stu-id="2d3bb-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2d3bb-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d3bb-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2d3bb-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2d3bb-129">Library</span></span><br/> | <dl> <span data-ttu-id="2d3bb-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d3bb-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2d3bb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d3bb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d3bb-132">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2d3bb-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="2d3bb-133">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="2d3bb-133">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> <dt>

[<span data-ttu-id="2d3bb-134">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="2d3bb-134">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
