---
title: D3DX11_NORMALMAP_FLAG-Enumeration (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Normale Karten Optionen. Sie können eine beliebige Anzahl dieser Flags mit einer bitweisen OR-Operation kombinieren.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- D3DX11_NORMALMAP_FLAG-Enumeration Direct3D 11
- LPD3DX11_NORMALMAP_FLAG enumerationszeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219700"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a><span data-ttu-id="91c6f-107">Bibliothek d3dx11 \_ normalmap- \_ Flag-Enumeration</span><span class="sxs-lookup"><span data-stu-id="91c6f-107">D3DX11\_NORMALMAP\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="91c6f-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91c6f-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="91c6f-109">Normale Karten Optionen.</span><span class="sxs-lookup"><span data-stu-id="91c6f-109">Normal map options.</span></span> <span data-ttu-id="91c6f-110">Sie können eine beliebige Anzahl dieser Flags mit einer bitweisen OR-Operation kombinieren.</span><span class="sxs-lookup"><span data-stu-id="91c6f-110">You can combine any number of these flags by using a bitwise OR operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c6f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="91c6f-111">Syntax</span></span>


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="91c6f-112">Konstanten</span><span class="sxs-lookup"><span data-stu-id="91c6f-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="91c6f-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**Bibliothek d3dx11 \_ normalmap- \_ Spiegelung \_ U**</span><span class="sxs-lookup"><span data-stu-id="91c6f-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="91c6f-114">Gibt an, dass die Pixel außerhalb des Kanten der Textur auf der U-Achse gespiegelt und nicht mit wvergewaltigt versehen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="91c6f-114">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="91c6f-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**Bibliothek d3dx11 \_ normalmap- \_ Spiegelung \_ V**</span><span class="sxs-lookup"><span data-stu-id="91c6f-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="91c6f-116">Gibt an, dass die Pixel außerhalb des Kanten der Textur auf der V-Achse gespiegelt und nicht mit wvergewaltigt versehen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="91c6f-116">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="91c6f-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**Bibliothek d3dx11 \_ normalmap- \_ Spiegelung**</span><span class="sxs-lookup"><span data-stu-id="91c6f-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="91c6f-118">Identisch mit Bibliothek d3dx11 \_ normalmap- \_ Spiegelung \_ U \| Bibliothek d3dx11 \_ normmap- \_ Spiegelung \_ V.</span><span class="sxs-lookup"><span data-stu-id="91c6f-118">Same as D3DX11\_NORMALMAP\_MIRROR\_U \| D3DX11\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="91c6f-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**Bibliothek d3dx11 \_ normalmap \_ invertsign**</span><span class="sxs-lookup"><span data-stu-id="91c6f-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="91c6f-120">Kehrt die Richtung der einzelnen normalen um.</span><span class="sxs-lookup"><span data-stu-id="91c6f-120">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="91c6f-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**Bibliothek d3dx11 \_ normalmap \_ Compute- \_ oksion**</span><span class="sxs-lookup"><span data-stu-id="91c6f-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="91c6f-122">Berechnet den Okklusions Begriff pro Pixel und codiert ihn in das Alpha.</span><span class="sxs-lookup"><span data-stu-id="91c6f-122">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="91c6f-123">Ein Alpha von 1 bedeutet, dass das Pixel in keiner Weise verdeckt wird, und ein Alpha von 0 bedeutet, dass das Pixel vollständig verdeckt ist.</span><span class="sxs-lookup"><span data-stu-id="91c6f-123">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91c6f-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91c6f-124">Remarks</span></span>

<span data-ttu-id="91c6f-125">Diese Flags werden von [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="91c6f-125">These flags are used by [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91c6f-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="91c6f-126">Requirements</span></span>



| <span data-ttu-id="91c6f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91c6f-127">Requirement</span></span> | <span data-ttu-id="91c6f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="91c6f-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91c6f-129">Header</span><span class="sxs-lookup"><span data-stu-id="91c6f-129">Header</span></span><br/> | <dl> <span data-ttu-id="91c6f-130"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="91c6f-130"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91c6f-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="91c6f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c6f-132">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="91c6f-132">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





