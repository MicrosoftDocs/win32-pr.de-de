---
description: Normale Zuordnungs Konstanten für Zuordnungen.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37985456e81b20af9b3e4396d10045d5e58c9b7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338857"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="81363-103">D3DX \_ normalmap</span><span class="sxs-lookup"><span data-stu-id="81363-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="81363-104">Normale Zuordnungs Konstanten für Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="81363-104">Normal maps generation constants.</span></span>



|                                     |                                                                                                                                                                                                    |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81363-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="81363-105">\#define</span></span>                            | <span data-ttu-id="81363-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81363-106">Description</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="81363-107">D3DX \_ normalmap- \_ Spiegelung \_ U</span><span class="sxs-lookup"><span data-stu-id="81363-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="81363-108">Gibt an, dass Pixel außerhalb des Kanten der Textur auf der u-Achse gespiegelt, nicht umschließt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81363-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="81363-109">D3DX \_ normalmap- \_ Spiegelung \_ V</span><span class="sxs-lookup"><span data-stu-id="81363-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="81363-110">Gibt an, dass die Pixel am Rand der Textur auf der v-Achse gespiegelt und nicht umschließt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81363-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="81363-111">D3DX \_ normalmap- \_ Spiegelung</span><span class="sxs-lookup"><span data-stu-id="81363-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="81363-112">Identisch mit der Angabe von D3DX \_ normalmap- \_ Spiegelung \_ U \| D3DX \_ normalmap- \_ Spiegel \_ V.</span><span class="sxs-lookup"><span data-stu-id="81363-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="81363-113">D3DX \_ normalmap \_ invertsign</span><span class="sxs-lookup"><span data-stu-id="81363-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="81363-114">Kehrt die Richtung der einzelnen normalen um.</span><span class="sxs-lookup"><span data-stu-id="81363-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="81363-115">D3DX \_ normalmap \_ Compute- \_ oksion</span><span class="sxs-lookup"><span data-stu-id="81363-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="81363-116">Berechnet den pro-Pixel-Okklusions Begriff und codiert ihn in das Alpha.</span><span class="sxs-lookup"><span data-stu-id="81363-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="81363-117">Ein Alpha von 1 bedeutet, dass das Pixel in keiner Weise verdeckt wird, und ein Alpha von 0 bedeutet, dass das Pixel vollständig verdeckt ist.</span><span class="sxs-lookup"><span data-stu-id="81363-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="81363-118">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="81363-118">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="81363-119">Header</span><span class="sxs-lookup"><span data-stu-id="81363-119">Header</span></span>                   | <span data-ttu-id="81363-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="81363-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="81363-121">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="81363-121">Minimum operating system</span></span> | <span data-ttu-id="81363-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="81363-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="81363-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="81363-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81363-124">D3DX-Konstanten</span><span class="sxs-lookup"><span data-stu-id="81363-124">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="81363-125">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="81363-125">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



