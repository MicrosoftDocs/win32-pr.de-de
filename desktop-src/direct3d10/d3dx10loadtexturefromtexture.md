---
description: Lädt eine Textur aus einer Textur.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: D3DX10LoadTextureFromTexture-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e8dc65c9bff78484f09c355f8eb3d9626372b9b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354436"
---
# <a name="d3dx10loadtexturefromtexture-function"></a><span data-ttu-id="c45e7-103">D3DX10LoadTextureFromTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="c45e7-103">D3DX10LoadTextureFromTexture function</span></span>

<span data-ttu-id="c45e7-104">Lädt eine Textur aus einer Textur.</span><span class="sxs-lookup"><span data-stu-id="c45e7-104">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c45e7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c45e7-105">Syntax</span></span>


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="c45e7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c45e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c45e7-107">*psrctexture*</span><span class="sxs-lookup"><span data-stu-id="c45e7-107">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="c45e7-108">Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="c45e7-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="c45e7-109">Ein Zeiger auf die Quell Textur.</span><span class="sxs-lookup"><span data-stu-id="c45e7-109">Pointer to the source texture.</span></span> <span data-ttu-id="c45e7-110">Siehe [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="c45e7-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="c45e7-111">*ploadinfo*</span><span class="sxs-lookup"><span data-stu-id="c45e7-111">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c45e7-112">Type: **[ **d3dx10 \_ Texture \_ Load \_ Info**](d3dx10-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c45e7-112">Type: **[**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md)\***</span></span>

<span data-ttu-id="c45e7-113">Zeiger auf Textur Lade Parameter.</span><span class="sxs-lookup"><span data-stu-id="c45e7-113">Pointer to texture loading parameters.</span></span> <span data-ttu-id="c45e7-114">Weitere Informationen finden Sie unter [**d3dx10 \_ Texture \_ Load \_ Info**](d3dx10-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="c45e7-114">See [**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="c45e7-115">*pdsttexture*</span><span class="sxs-lookup"><span data-stu-id="c45e7-115">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="c45e7-116">Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="c45e7-116">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="c45e7-117">Ein Zeiger auf die Ziel Textur.</span><span class="sxs-lookup"><span data-stu-id="c45e7-117">Pointer to the destination texture.</span></span> <span data-ttu-id="c45e7-118">Siehe [**ID3D10Resource-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="c45e7-118">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c45e7-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c45e7-119">Return value</span></span>

<span data-ttu-id="c45e7-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c45e7-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c45e7-121">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="c45e7-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c45e7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c45e7-122">Requirements</span></span>



| <span data-ttu-id="c45e7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c45e7-123">Requirement</span></span> | <span data-ttu-id="c45e7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c45e7-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c45e7-125">Header</span><span class="sxs-lookup"><span data-stu-id="c45e7-125">Header</span></span><br/> | <dl> <span data-ttu-id="c45e7-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c45e7-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c45e7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c45e7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c45e7-128">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="c45e7-128">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




