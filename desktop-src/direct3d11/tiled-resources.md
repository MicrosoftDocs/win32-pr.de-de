---
title: Gekachelte Ressourcen
description: Gekachelte Ressourcen können sich als große logische Ressourcen vorstellen, die kleine Mengen an physischem Arbeitsspeicher verwenden.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c7e6aaf60f58f55274c9d7a135b9107933f640
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855548"
---
# <a name="tiled-resources"></a><span data-ttu-id="f6ba3-103">Gekachelte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f6ba3-103">Tiled resources</span></span>

<span data-ttu-id="f6ba3-104">Gekachelte Ressourcen können sich als große logische Ressourcen vorstellen, die kleine Mengen an physischem Arbeitsspeicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6ba3-104">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span>

<span data-ttu-id="f6ba3-105">In diesem Abschnitt wird beschrieben, warum Kachel Ressourcen benötigt werden und wie Sie gekachelte Ressourcen erstellen und verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6ba3-105">This section describes why tiled resources are needed and how you create and use tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f6ba3-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f6ba3-106">In this section</span></span>



| <span data-ttu-id="f6ba3-107">Thema</span><span class="sxs-lookup"><span data-stu-id="f6ba3-107">Topic</span></span>                                                                                   | <span data-ttu-id="f6ba3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6ba3-108">Description</span></span>                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6ba3-109">Warum werden Kachel Ressourcen benötigt?</span><span class="sxs-lookup"><span data-stu-id="f6ba3-109">Why are tiled resources needed?</span></span>](why-are-tiled-resources-needed-.md)<br/>       | <span data-ttu-id="f6ba3-110">Gekachelte Ressourcen werden benötigt, sodass weniger GPU-Speicher (Graphics Processing Unit) verschwendet wird, um Bereiche von Oberflächen zu speichern, auf die die Anwendung keinen Zugriff hat, und die Hardware weiß, wie Sie über angrenzende Kacheln filtern kann.</span><span class="sxs-lookup"><span data-stu-id="f6ba3-110">Tiled resources are needed so less graphics processing unit (GPU) memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span><br/>     |
| [<span data-ttu-id="f6ba3-111">Erstellen von Kachel Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f6ba3-111">Creating tiled resources</span></span>](creating-tiled-resources.md)<br/>                     | <span data-ttu-id="f6ba3-112">Gekachelte Ressourcen werden erstellt, indem beim Erstellen einer Ressource das [**D3D11 \_ Resource \_ misc- \_ Kachel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Kennzeichen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f6ba3-112">Tiled resources are created by specifying the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag when you create a resource.</span></span><br/>                                                                                          |
| [<span data-ttu-id="f6ba3-113">Ressourcen-APIs mit Kachel</span><span class="sxs-lookup"><span data-stu-id="f6ba3-113">Tiled Resource APIs</span></span>](tiled-resource-apis.md)<br/>                               | <span data-ttu-id="f6ba3-114">Die in diesem Abschnitt beschriebenen APIs funktionieren mit gekachelten Ressourcen und einem Kachel Pool.</span><span class="sxs-lookup"><span data-stu-id="f6ba3-114">The APIs described in this section work with tiled resources and tile pool.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="f6ba3-115">Pipeline Zugriff auf gekachelte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f6ba3-115">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)<br/> | <span data-ttu-id="f6ba3-116">Gekachelte Ressourcen können in Shader-Ressourcen Ansichten (SRV), renderzielsichten (RTV), Datenquellen Sichten (Datenquellen Sicht) und unsortierter Zugriffs Ansichten (UAV) sowie einigen Bindungs Punkten verwendet werden, bei denen Sichten nicht verwendet werden, wie z. b. Vertex-Puffer Bindungen.</span><span class="sxs-lookup"><span data-stu-id="f6ba3-116">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <br/> |
| [<span data-ttu-id="f6ba3-117">Tarife der Kachel "Ressourcen"</span><span class="sxs-lookup"><span data-stu-id="f6ba3-117">Tiled resources features tiers</span></span>](tiled-resources-features-tiers.md)<br/>         | <span data-ttu-id="f6ba3-118">Direct3D 11,2 macht Unterstützung für gekachelte Ressourcen in zwei Stufen mit den Werten der [**D3D11- \_ Kachel \_ Ressourcen \_ Ebene**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f6ba3-118">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span> <br/>                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="f6ba3-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6ba3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6ba3-120">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f6ba3-120">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





