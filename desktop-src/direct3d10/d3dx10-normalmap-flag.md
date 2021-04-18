---
description: Diese Flags werden verwendet, um zu steuern, wie D3DX10ComputeNormalMap normale Zuordnungen generiert. Eine beliebige Anzahl dieser Flags kann in beliebiger Kombination oder zusammengefasst werden.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: D3DX10_NORMALMAP_FLAG-Enumeration (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355025"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a><span data-ttu-id="7513c-104">D3dx10 \_ normalmap- \_ Flag-Enumeration</span><span class="sxs-lookup"><span data-stu-id="7513c-104">D3DX10\_NORMALMAP\_FLAG enumeration</span></span>

<span data-ttu-id="7513c-105">Diese Flags werden verwendet, um zu steuern, wie [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) normale Zuordnungen generiert.</span><span class="sxs-lookup"><span data-stu-id="7513c-105">These flags are used to control how [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) generates normal maps.</span></span> <span data-ttu-id="7513c-106">Eine beliebige Anzahl dieser Flags kann in beliebiger Kombination oder zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="7513c-106">Any number of these flags may be OR'd together in any combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="7513c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7513c-107">Syntax</span></span>


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="7513c-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="7513c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7513c-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3dx10 \_ normalmap- \_ Spiegelung \_ U**</span><span class="sxs-lookup"><span data-stu-id="7513c-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="7513c-110">Gibt an, dass die Pixel außerhalb des Kanten der Textur auf der U-Achse gespiegelt und nicht mit wvergewaltigt versehen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7513c-110">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="7513c-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3dx10 \_ normalmap- \_ Spiegelung \_ V**</span><span class="sxs-lookup"><span data-stu-id="7513c-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="7513c-112">Gibt an, dass die Pixel außerhalb des Kanten der Textur auf der V-Achse gespiegelt und nicht mit wvergewaltigt versehen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7513c-112">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="7513c-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3dx10 \_ normalmap- \_ Spiegelung**</span><span class="sxs-lookup"><span data-stu-id="7513c-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="7513c-114">Identisch mit d3dx10 \_ normalmap- \_ Spiegelung \_ U \| d3dx10 \_ normmap- \_ Spiegelung \_ V.</span><span class="sxs-lookup"><span data-stu-id="7513c-114">Same as D3DX10\_NORMALMAP\_MIRROR\_U \| D3DX10\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="7513c-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3dx10 \_ normalmap \_ invertsign**</span><span class="sxs-lookup"><span data-stu-id="7513c-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="7513c-116">Kehrt die Richtung der einzelnen normalen um.</span><span class="sxs-lookup"><span data-stu-id="7513c-116">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="7513c-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3dx10 \_ normalmap \_ Compute- \_ oksion**</span><span class="sxs-lookup"><span data-stu-id="7513c-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="7513c-118">Berechnet den Okklusions Begriff pro Pixel und codiert ihn in das Alpha.</span><span class="sxs-lookup"><span data-stu-id="7513c-118">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="7513c-119">Ein Alpha von 1 bedeutet, dass das Pixel in keiner Weise verdeckt wird, und ein Alpha von 0 bedeutet, dass das Pixel vollständig verdeckt ist.</span><span class="sxs-lookup"><span data-stu-id="7513c-119">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7513c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7513c-120">Requirements</span></span>



| <span data-ttu-id="7513c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7513c-121">Requirement</span></span> | <span data-ttu-id="7513c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7513c-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7513c-123">Header</span><span class="sxs-lookup"><span data-stu-id="7513c-123">Header</span></span><br/> | <dl> <span data-ttu-id="7513c-124"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="7513c-124"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7513c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7513c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7513c-126">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="7513c-126">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




