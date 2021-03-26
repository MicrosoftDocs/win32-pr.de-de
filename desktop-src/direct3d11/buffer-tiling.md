---
title: Pufferanordnung
description: Eine Puffer Ressource ist in Kacheln mit 64 KB unterteilt, wobei ein Leerzeichen in der letzten Kachel leer ist, wenn die Größe kein Vielfaches von 64 KB ist.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fafa009e554499822c90c8fb6c0c8f34e47f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858286"
---
# <a name="buffer-tiling"></a><span data-ttu-id="bbd9a-103">Pufferanordnung</span><span class="sxs-lookup"><span data-stu-id="bbd9a-103">Buffer tiling</span></span>

<span data-ttu-id="bbd9a-104">Eine [Puffer](overviews-direct3d-11-resources-buffers.md) Ressource ist in Kacheln mit 64 KB unterteilt, wobei ein Leerzeichen in der letzten Kachel leer ist, wenn die Größe kein Vielfaches von 64 KB ist.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-104">A [Buffer](overviews-direct3d-11-resources-buffers.md) resource is divided into 64KB tiles, with some empty space in the last tile if the size is not a multiple of 64KB.</span></span>

<span data-ttu-id="bbd9a-105">Für strukturierte Puffer ist keine Einschränkung auf dem STRIDE erforderlich, um gekachelt zu werden.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-105">Structured buffers must have no constraint on the stride to be tiled.</span></span> <span data-ttu-id="bbd9a-106">Aber mögliche Leistungsoptimierungen in der Hardware für die Verwendung von [**structuredbuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) können durch das Anordnen der Kacheln an erster Stelle geopfert werden.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-106">But possible performance optimizations in hardware for using [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) can be sacrificed by making them tiled in the first place.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbd9a-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbd9a-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbd9a-108">Kacheln eines gekachelten Ressourcenbereichs</span><span class="sxs-lookup"><span data-stu-id="bbd9a-108">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 