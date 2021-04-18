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
# <a name="d3dxfillvolumetexturetx-function"></a><span data-ttu-id="87b35-103">D3DXFillVolumeTextureTX-Funktion</span><span class="sxs-lookup"><span data-stu-id="87b35-103">D3DXFillVolumeTextureTX function</span></span>

<span data-ttu-id="87b35-104">Verwendet eine kompilierte HLSL-Funktion (High-Level Shader Language) zum Auffüllen der einzelnen texttabformationen einer Textur.</span><span class="sxs-lookup"><span data-stu-id="87b35-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="87b35-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87b35-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="87b35-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87b35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87b35-107">*ptexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87b35-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87b35-108">Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="87b35-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="87b35-109">Zeiger auf ein [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) -Objekt, das die zu füllende Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="87b35-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="87b35-110">*ptextureshader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87b35-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87b35-111">Typ: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="87b35-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="87b35-112">Zeiger auf ein [**ID3DXTextureShader**](id3dxtextureshader.md) Texture-Shader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="87b35-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87b35-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87b35-113">Return value</span></span>

<span data-ttu-id="87b35-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87b35-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87b35-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="87b35-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="87b35-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="87b35-116">If the function fails, the return value can be one of the following:D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="87b35-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87b35-117">Remarks</span></span>

<span data-ttu-id="87b35-118">Das Textur Ziel muss eine HLSL-Funktion sein, die die folgende Semantik enthält:</span><span class="sxs-lookup"><span data-stu-id="87b35-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="87b35-119">Ein Eingabeparameter muss eine Positions Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="87b35-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="87b35-120">Ein Eingabeparameter muss eine Psize-Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="87b35-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="87b35-121">Die Funktion muss einen Parameter zurückgeben, der die Farb Semantik verwendet.</span><span class="sxs-lookup"><span data-stu-id="87b35-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="87b35-122">Die Eingabeparameter können in beliebiger Reihenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="87b35-122">The input parameters can be in any order.</span></span> <span data-ttu-id="87b35-123">Ein Beispiel finden Sie unter [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="87b35-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="87b35-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87b35-124">Requirements</span></span>



| <span data-ttu-id="87b35-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87b35-125">Requirement</span></span> | <span data-ttu-id="87b35-126">Wert</span><span class="sxs-lookup"><span data-stu-id="87b35-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87b35-127">Header</span><span class="sxs-lookup"><span data-stu-id="87b35-127">Header</span></span><br/>  | <dl> <span data-ttu-id="87b35-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="87b35-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="87b35-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="87b35-129">Library</span></span><br/> | <dl> <span data-ttu-id="87b35-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87b35-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="87b35-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87b35-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b35-132">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="87b35-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="87b35-133">**D3DXFillTextureTX**</span><span class="sxs-lookup"><span data-stu-id="87b35-133">**D3DXFillTextureTX**</span></span>](d3dxfilltexturetx.md)
</dt> <dt>

[<span data-ttu-id="87b35-134">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="87b35-134">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
