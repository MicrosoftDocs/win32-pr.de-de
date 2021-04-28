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
# <a name="d3dxfillvolumetexturetx-function"></a><span data-ttu-id="f9e86-103">D3DXFillVolumeTextureTX-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9e86-103">D3DXFillVolumeTextureTX function</span></span>

<span data-ttu-id="f9e86-104">Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language), um jeden Texel jeder Mipmapebene einer Textur zu füllen.</span><span class="sxs-lookup"><span data-stu-id="f9e86-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9e86-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9e86-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="f9e86-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9e86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9e86-107">*pTexture* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f9e86-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9e86-108">Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="f9e86-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="f9e86-109">Zeiger auf ein [**IDirect3DVolumeTexture9-Objekt,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) das die zu füllende Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="f9e86-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="f9e86-110">*pTextureShader* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f9e86-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9e86-111">Typ: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="f9e86-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="f9e86-112">Zeiger auf ein [**ID3DXTextureShader-Texturshaderobjekt.**](id3dxtextureshader.md)</span><span class="sxs-lookup"><span data-stu-id="f9e86-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9e86-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9e86-113">Return value</span></span>

<span data-ttu-id="f9e86-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f9e86-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f9e86-115">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f9e86-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f9e86-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f9e86-116">If the function fails, the return value can be one of the following:D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9e86-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9e86-117">Remarks</span></span>

<span data-ttu-id="f9e86-118">Das Texturziel muss eine HLSL-Funktion sein, die die folgende Semantik enthält:</span><span class="sxs-lookup"><span data-stu-id="f9e86-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="f9e86-119">Ein Eingabeparameter muss eine POSITION-Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9e86-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="f9e86-120">Ein Eingabeparameter muss eine PSIZE-Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9e86-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="f9e86-121">Die Funktion muss einen Parameter zurückgeben, der die COLOR-Semantik verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9e86-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="f9e86-122">Die Eingabeparameter können in beliebiger Reihenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f9e86-122">The input parameters can be in any order.</span></span> <span data-ttu-id="f9e86-123">Ein Beispiel finden Sie unter [ **D3DXFillTextureTX.**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="f9e86-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e86-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9e86-124">Requirements</span></span>



| <span data-ttu-id="f9e86-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9e86-125">Requirement</span></span> | <span data-ttu-id="f9e86-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f9e86-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e86-127">Header</span><span class="sxs-lookup"><span data-stu-id="f9e86-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f9e86-128"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="f9e86-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f9e86-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9e86-129">Library</span></span><br/> | <dl> <span data-ttu-id="f9e86-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9e86-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f9e86-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f9e86-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e86-132">Texturfunktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f9e86-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="f9e86-133">**D3DXFillTextureTX**</span><span class="sxs-lookup"><span data-stu-id="f9e86-133">**D3DXFillTextureTX**</span></span>](d3dxfilltexturetx.md)
</dt> <dt>

[<span data-ttu-id="f9e86-134">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="f9e86-134">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
