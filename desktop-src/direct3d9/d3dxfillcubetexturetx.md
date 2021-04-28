---
description: 'D3DXFillCubeTextureTX-Funktion: Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language), um jedes Texel jeder Mipmapebene einer Textur zu füllen.'
ms.assetid: a0c36967-57e6-4771-8e9f-f32949c12001
title: D3DXFillCubeTextureTX-Funktion (D3dx9tex.h)
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
ms.openlocfilehash: 95c6d054900f3f4c4710e22c54759161800137c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107668"
---
# <a name="d3dxfillcubetexturetx-function"></a><span data-ttu-id="b60b3-103">D3DXFillCubeTextureTX-Funktion</span><span class="sxs-lookup"><span data-stu-id="b60b3-103">D3DXFillCubeTextureTX function</span></span>

<span data-ttu-id="b60b3-104">Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language), um jedes Texel jeder Mipmapebene einer Textur zu füllen.</span><span class="sxs-lookup"><span data-stu-id="b60b3-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b60b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b60b3-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="b60b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b60b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b60b3-107">*pTexture* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b60b3-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b60b3-108">Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="b60b3-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="b60b3-109">Zeiger auf ein [**IDirect3DCubeTexture9-Objekt,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) das die zu füllende Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="b60b3-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="b60b3-110">*pTextureShader* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b60b3-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b60b3-111">Typ: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="b60b3-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="b60b3-112">Zeiger auf ein [**ID3DXTextureShader-Texturshader-Objekt.**](id3dxtextureshader.md)</span><span class="sxs-lookup"><span data-stu-id="b60b3-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b60b3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b60b3-113">Return value</span></span>

<span data-ttu-id="b60b3-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b60b3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b60b3-115">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b60b3-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b60b3-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b60b3-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b60b3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b60b3-117">Remarks</span></span>

<span data-ttu-id="b60b3-118">Das Texturziel muss eine HLSL-Funktion sein, die die folgende Semantik enthält:</span><span class="sxs-lookup"><span data-stu-id="b60b3-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="b60b3-119">Ein Eingabeparameter muss eine POSITION-Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="b60b3-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="b60b3-120">Ein Eingabeparameter muss eine PSIZE-Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="b60b3-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="b60b3-121">Die Funktion muss einen Parameter zurückgeben, der die COLOR-Semantik verwendet.</span><span class="sxs-lookup"><span data-stu-id="b60b3-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="b60b3-122">Die Eingabeparameter können in beliebiger Reihenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="b60b3-122">The input parameters can be in any order.</span></span> <span data-ttu-id="b60b3-123">Ein Beispiel finden Sie unter [ **D3DXFillTextureTX.**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="b60b3-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="b60b3-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b60b3-124">Requirements</span></span>



| <span data-ttu-id="b60b3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b60b3-125">Requirement</span></span> | <span data-ttu-id="b60b3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b60b3-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b60b3-127">Header</span><span class="sxs-lookup"><span data-stu-id="b60b3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b60b3-128"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="b60b3-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b60b3-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b60b3-129">Library</span></span><br/> | <dl> <span data-ttu-id="b60b3-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b60b3-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b60b3-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b60b3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b60b3-132">Texturfunktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b60b3-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="b60b3-133">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="b60b3-133">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
