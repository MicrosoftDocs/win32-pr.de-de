---
description: Normal ordnet Generierungskonstanten zu.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4263237cedf92a5e322f2fe139e9afe2297f6b9b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342855"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="f7098-103">D3DX \_ NORMALMAP</span><span class="sxs-lookup"><span data-stu-id="f7098-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="f7098-104">Normal ordnet Generierungskonstanten zu.</span><span class="sxs-lookup"><span data-stu-id="f7098-104">Normal maps generation constants.</span></span>



| <span data-ttu-id="f7098-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="f7098-105">\#define</span></span>                            | <span data-ttu-id="f7098-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7098-106">Description</span></span>                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7098-107">D3DX \_ NORMALMAP \_ MIRROR \_ U</span><span class="sxs-lookup"><span data-stu-id="f7098-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="f7098-108">Gibt an, dass Pixel außerhalb des Texturrands auf der U-Achse gespiegelt und nicht umschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7098-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="f7098-109">D3DX \_ NORMALMAP \_ MIRROR \_ V</span><span class="sxs-lookup"><span data-stu-id="f7098-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="f7098-110">Gibt an, dass Pixel außerhalb des Texturrands auf der V-Achse gespiegelt und nicht umschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7098-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="f7098-111">D3DX \_ NORMALMAP \_ MIRROR</span><span class="sxs-lookup"><span data-stu-id="f7098-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="f7098-112">Entspricht der Angabe von D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.</span><span class="sxs-lookup"><span data-stu-id="f7098-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="f7098-113">D3DX \_ NORMALMAP \_ INVERTSIGN</span><span class="sxs-lookup"><span data-stu-id="f7098-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="f7098-114">Umkehrt die Richtung der einzelnen Normalitäten.</span><span class="sxs-lookup"><span data-stu-id="f7098-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="f7098-115">D3DX \_ NORMALMAP \_ COMPUTE \_ OCCLUSION</span><span class="sxs-lookup"><span data-stu-id="f7098-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="f7098-116">Berechnet den Verdeckungsbegriff pro Pixel und codiert ihn in das Alpha.</span><span class="sxs-lookup"><span data-stu-id="f7098-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="f7098-117">Ein Alpha von 1 bedeutet, dass das Pixel in keiner Weise verdeckt wird, und ein Alpha von 0 bedeutet, dass das Pixel vollständig verdeckt ist.</span><span class="sxs-lookup"><span data-stu-id="f7098-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="f7098-118">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="f7098-118">Constant Information</span></span>



| <span data-ttu-id="f7098-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7098-119">Requirement</span></span>                         | <span data-ttu-id="f7098-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f7098-120">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="f7098-121">Header</span><span class="sxs-lookup"><span data-stu-id="f7098-121">Header</span></span>                   | <span data-ttu-id="f7098-122">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="f7098-122">d3dx9tex.h</span></span> |
| <span data-ttu-id="f7098-123">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="f7098-123">Minimum operating system</span></span> | <span data-ttu-id="f7098-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f7098-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f7098-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7098-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7098-126">D3DX-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f7098-126">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="f7098-127">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="f7098-127">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



