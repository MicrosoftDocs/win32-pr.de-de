---
title: Einheitliche Speicherarchitektur
description: Die Abfrage, ob eine einheitliche Speicherarchitektur (UMA) unterstützt wird, kann Ihnen dabei helfen zu bestimmen, wie einige Ressourcen behandelt werden.
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baeab51838b9b3382884a681ec9b579fa700a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947467"
---
# <a name="unified-memory-architecture"></a><span data-ttu-id="c5da4-103">Einheitliche Speicherarchitektur</span><span class="sxs-lookup"><span data-stu-id="c5da4-103">Unified Memory Architecture</span></span>

<span data-ttu-id="c5da4-104">Die Abfrage, ob eine einheitliche Speicherarchitektur (UMA) unterstützt wird, kann Ihnen dabei helfen zu bestimmen, wie einige Ressourcen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c5da4-104">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span>

<span data-ttu-id="c5da4-105">Ein boolescher Wert, der vom Treiber festgelegt wird, kann aus der [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) -Struktur gelesen werden, um zu bestimmen, ob die Hardware "Uma" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5da4-105">A boolean, set by the driver, can be read from the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure to determine if the hardware supports UMA.</span></span>

<span data-ttu-id="c5da4-106">Anwendungen, die in einer anderen Sprache ausgeführt werden, benötigen möglicherweise mehr Ressourcen mit aktiviertem CPU-Zugriff, als wenn Sie nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c5da4-106">Applications running on UMA may want to have more resources with CPU access enabled than if it is not available.</span></span> <span data-ttu-id="c5da4-107">Mit Uma können Anwendungen nicht mehr Ressourcen Daten kopieren, sondern nur für nicht-Uma-Grafikadapter.</span><span class="sxs-lookup"><span data-stu-id="c5da4-107">UMA enables applications to avoiding copying resource data around, instead of staying efficient solely for non-UMA graphics adapters.</span></span> [<span data-ttu-id="c5da4-108">Direct3D 11,3-Features</span><span class="sxs-lookup"><span data-stu-id="c5da4-108">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)

## <a name="related-topics"></a><span data-ttu-id="c5da4-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5da4-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5da4-110">Direct3D 11,3-Features</span><span class="sxs-lookup"><span data-stu-id="c5da4-110">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




