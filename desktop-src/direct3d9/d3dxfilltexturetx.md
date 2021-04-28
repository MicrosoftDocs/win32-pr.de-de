---
description: 'D3DXFillTextureTX-Funktion: Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language), um jeden Texel jeder Mipmapebene einer Textur aufzufüllen.'
ms.assetid: 013660ce-865e-4acf-a1ea-670e70377ff5
title: D3DXFillTextureTX-Funktion (D3dx9tex.h)
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
ms.openlocfilehash: 419dc0e7b4266a2fe32557c52ed4323b51a25843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107638"
---
# <a name="d3dxfilltexturetx-function"></a><span data-ttu-id="5ce3b-103">D3DXFillTextureTX-Funktion</span><span class="sxs-lookup"><span data-stu-id="5ce3b-103">D3DXFillTextureTX function</span></span>

<span data-ttu-id="5ce3b-104">Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language), um jeden Texel jeder Mipmapebene einer Textur zu füllen.</span><span class="sxs-lookup"><span data-stu-id="5ce3b-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce3b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ce3b-105">Syntax</span></span>


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="5ce3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ce3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ce3b-107">*pTexture* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5ce3b-107">*pTexture* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ce3b-108">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="5ce3b-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="5ce3b-109">Zeiger auf ein [**IDirect3DTexture9-Objekt,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) das die zu füllende Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="5ce3b-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="5ce3b-110">*pTextureShader* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ce3b-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ce3b-111">Typ: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="5ce3b-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="5ce3b-112">Zeiger auf ein [**ID3DXTextureShader-Texturshaderobjekt.**](id3dxtextureshader.md)</span><span class="sxs-lookup"><span data-stu-id="5ce3b-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ce3b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ce3b-113">Return value</span></span>

<span data-ttu-id="5ce3b-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ce3b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ce3b-115">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ce3b-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5ce3b-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5ce3b-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ce3b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ce3b-117">Remarks</span></span>

<span data-ttu-id="5ce3b-118">Das Texturziel muss eine HLSL-Funktion sein, die die folgende Semantik enthält:</span><span class="sxs-lookup"><span data-stu-id="5ce3b-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="5ce3b-119">Ein Eingabeparameter muss eine POSITION-Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ce3b-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="5ce3b-120">Ein Eingabeparameter muss eine PSIZE-Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ce3b-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="5ce3b-121">Die Funktion muss einen Parameter zurückgeben, der die COLOR-Semantik verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ce3b-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="5ce3b-122">Im Folgenden finden Sie ein Beispiel für eine solche HLSL-Funktion:</span><span class="sxs-lookup"><span data-stu-id="5ce3b-122">The following is an example of such an HLSL function:</span></span>


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



<span data-ttu-id="5ce3b-123">Beachten Sie, dass die Eingabeparameter in beliebiger Reihenfolge sein können, aber beide Eingabesemantiken dargestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5ce3b-123">Note that the input parameters can be in any order, but both input semantics must be represented.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ce3b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ce3b-124">Requirements</span></span>



| <span data-ttu-id="5ce3b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ce3b-125">Requirement</span></span> | <span data-ttu-id="5ce3b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5ce3b-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce3b-127">Header</span><span class="sxs-lookup"><span data-stu-id="5ce3b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5ce3b-128"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="5ce3b-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5ce3b-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5ce3b-129">Library</span></span><br/> | <dl> <span data-ttu-id="5ce3b-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ce3b-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5ce3b-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5ce3b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ce3b-132">Texturfunktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="5ce3b-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="5ce3b-133">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="5ce3b-133">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> <dt>

[<span data-ttu-id="5ce3b-134">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="5ce3b-134">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
