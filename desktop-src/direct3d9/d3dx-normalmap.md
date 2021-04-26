---
description: Normale Kartengenerierungskonst constants.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f76b6afe6eb68e8ddbc3ca28085861a518effc
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996327"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="39bf5-103">D3DX \_ NORMALMAP</span><span class="sxs-lookup"><span data-stu-id="39bf5-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="39bf5-104">Normale Kartengenerierungskonst constants.</span><span class="sxs-lookup"><span data-stu-id="39bf5-104">Normal maps generation constants.</span></span>



| <span data-ttu-id="39bf5-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="39bf5-105">\#define</span></span>                            | <span data-ttu-id="39bf5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39bf5-106">Description</span></span>                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39bf5-107">D3DX \_ NORMALMAP \_ MIRROR \_ U</span><span class="sxs-lookup"><span data-stu-id="39bf5-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="39bf5-108">Gibt an, dass Pixel vom Rand der Textur auf der U-Achse gespiegelt und nicht umschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39bf5-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="39bf5-109">D3DX \_ NORMALMAP \_ MIRROR \_ V</span><span class="sxs-lookup"><span data-stu-id="39bf5-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="39bf5-110">Gibt an, dass Pixel vom Rand der Textur auf der V-Achse gespiegelt und nicht umschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39bf5-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="39bf5-111">D3DX \_ NORMALMAP \_ MIRROR</span><span class="sxs-lookup"><span data-stu-id="39bf5-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="39bf5-112">Identisch mit der Angabe von D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.</span><span class="sxs-lookup"><span data-stu-id="39bf5-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="39bf5-113">D3DX \_ NORMALMAP \_ INVERTSIGN</span><span class="sxs-lookup"><span data-stu-id="39bf5-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="39bf5-114">Invertiert die Richtung der einzelnen Normalen.</span><span class="sxs-lookup"><span data-stu-id="39bf5-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="39bf5-115">D3DX \_ NORMALMAP \_ COMPUTE \_ OCCLUSION</span><span class="sxs-lookup"><span data-stu-id="39bf5-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="39bf5-116">Berechnet den Occlusion-Begriff pro Pixel und codiert ihn in das Alpha.</span><span class="sxs-lookup"><span data-stu-id="39bf5-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="39bf5-117">Ein Alphawert von 1 bedeutet, dass das Pixel nicht verdeckt wird, und ein Alphawert von 0 bedeutet, dass das Pixel vollständig verdeckt ist.</span><span class="sxs-lookup"><span data-stu-id="39bf5-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="39bf5-118">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="39bf5-118">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="39bf5-119">Header</span><span class="sxs-lookup"><span data-stu-id="39bf5-119">Header</span></span>                   | <span data-ttu-id="39bf5-120">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="39bf5-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="39bf5-121">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="39bf5-121">Minimum operating system</span></span> | <span data-ttu-id="39bf5-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="39bf5-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="39bf5-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39bf5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39bf5-124">D3DX-Konstanten</span><span class="sxs-lookup"><span data-stu-id="39bf5-124">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="39bf5-125">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="39bf5-125">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



