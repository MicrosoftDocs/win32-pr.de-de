---
title: Tarife der Kachel "Ressourcen"
description: Direct3D 11,2 macht Unterstützung für gekachelte Ressourcen in zwei Stufen mit den Werten der D3D11- \_ Kachel \_ Ressourcen \_ Ebene verfügbar.
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2282cde1dfc8c4249672d18e303a4529338d4fbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947470"
---
# <a name="tiled-resources-features-tiers"></a><span data-ttu-id="7630f-103">Tarife der Kachel "Ressourcen"</span><span class="sxs-lookup"><span data-stu-id="7630f-103">Tiled resources features tiers</span></span>

<span data-ttu-id="7630f-104">Direct3D 11,2 macht Unterstützung für gekachelte Ressourcen in zwei Stufen mit den Werten der [**D3D11- \_ Kachel \_ Ressourcen \_ Ebene**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7630f-104">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span>

<span data-ttu-id="7630f-105">Um abzufragen, ob die Hardware und der Treiber gekachelte Ressourcen unterstützen und auf welcher Ebene, übergeben Sie den Wert [**D3D11 \_ Feature \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) an den *Funktions* Parameter von [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="7630f-105">To query whether the hardware and driver support tiled resources and at what tier level, pass the [**D3D11\_FEATURE\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) value to the *Feature* parameter of [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span></span> <span data-ttu-id="7630f-106">Übergeben Sie außerdem einen Zeiger an die [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) -Struktur an den *pfeaturesupportdata* -Parameter, und übergeben Sie die Größe der **D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS1** -Struktur an den Parameter " *featuresupportdatasize* ".</span><span class="sxs-lookup"><span data-stu-id="7630f-106">Also, pass a pointer to the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) structure to the *pFeatureSupportData* parameter, and pass the size of the **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1** structure to the *FeatureSupportDataSize* parameter.</span></span> <span data-ttu-id="7630f-107">**Checkfeaturesupport** gibt die Ebene der Ebene als Wert der [**D3D11- \_ Kachel \_ Ressourcen \_ Ebene**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) im **tiledresourcestier** -Member von **D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS1** zurück.</span><span class="sxs-lookup"><span data-stu-id="7630f-107">**CheckFeatureSupport** returns the tier level as a [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) value in the **TiledResourcesTier** member of **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**.</span></span>

<span data-ttu-id="7630f-108">In diesem Abschnitt werden diese beiden Ebenen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7630f-108">This section describes these two tiers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7630f-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7630f-109">In this section</span></span>



| <span data-ttu-id="7630f-110">Thema</span><span class="sxs-lookup"><span data-stu-id="7630f-110">Topic</span></span>                           | <span data-ttu-id="7630f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7630f-111">Description</span></span>                                       |
|---------------------------------|---------------------------------------------------|
| [<span data-ttu-id="7630f-112">Ebene 1</span><span class="sxs-lookup"><span data-stu-id="7630f-112">Tier 1</span></span>](tier-1.md)<br/> | <span data-ttu-id="7630f-113">In diesem Abschnitt wird die Unterstützung für Ebene 1 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7630f-113">This section describes tier 1 support.</span></span><br/> |
| [<span data-ttu-id="7630f-114">Ebene 2</span><span class="sxs-lookup"><span data-stu-id="7630f-114">Tier 2</span></span>](tier-2.md)<br/> | <span data-ttu-id="7630f-115">In diesem Abschnitt wird die Unterstützung der Ebene 2 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7630f-115">This section describes tier 2 support.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="7630f-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7630f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7630f-117">Gekachelte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7630f-117">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

 





