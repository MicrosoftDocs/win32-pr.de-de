---
title: ALE Multicast-/Broadcast Datenverkehr
description: Alle eingehenden Multicast-und Broadcast Datenverkehr auf der Ebene (Application Layer Enforcement) werden einem globalen ALE-Datenfluss zugeordnet.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309895"
---
# <a name="ale-multicastbroadcast-traffic"></a><span data-ttu-id="8f0d8-103">ALE Multicast-/Broadcast Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="8f0d8-103">ALE Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="8f0d8-104">Alle eingehenden Multicast-und Broadcast Datenverkehr auf der Ebene (Application Layer Enforcement) werden einem globalen [ALE](ale-stateful-filtering.md)-Datenfluss zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-104">All inbound multicast and broadcast traffic at the Application Layer Enforcement (ALE) layers is mapped to one global [ALE flow](ale-stateful-filtering.md).</span></span> <span data-ttu-id="8f0d8-105">Der Antwort Datenverkehr für eingehende Multicast-und Broadcast Pakete wird auf der Ebene der Ebene der Ebene der swpm-Layer-Authentifizierung (x [**\_ \_ \_ \_ \_ {4 \| 6}**](management-filtering-layer-identifiers-.md) ) klassifiziert, und für jede Antwort werden separate ALE-Flows erstellt.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-105">Response traffic for inbound multicast and broadcast packets is classified at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and separate ALE flows are created for each response.</span></span>

<span data-ttu-id="8f0d8-106">Ausgehender Multicast-und Broadcast Datenverkehr auf der ALE-Ebene erstellt einen 4-Sekunden-ALE Datenfluss.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-106">Outbound multicast and broadcast traffic at the ALE layers creates a 4-second ALE flow.</span></span> <span data-ttu-id="8f0d8-107">Standardmäßig lässt die Autorisierung eines ausgehenden Multicast-oder Broadcast-ALE-Pakets eingehenden Datenverkehr, ob Unicast, Multicast oder Broadcast, von einer beliebigen Remote Adresse bis zu 4 Sekunden zu.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-107">By default, the authorization of an outbound multicast or broadcast ALE packet will permit inbound traffic, whether unicast, multicast, or broadcast, from any remote address for up to 4 seconds.</span></span> <span data-ttu-id="8f0d8-108">Ein solcher ALE Datenfluss kann nur durch nachfolgenden ausgehenden Datenverkehr, der mit dem Datenfluss übereinstimmt, aktualisiert oder aufrechterhalten werden.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-108">Such an ALE flow can only be refreshed or kept alive by subsequent outbound traffic that matches the ALE flow.</span></span>

> [!Note]  
> <span data-ttu-id="8f0d8-109">Die 4-Sekunden-Lebensdauer wird durch die integrierte Legenden-Legenden Optionen zum Festlegen der abrufsschout- [**\_ \_ \_ Optionen \_ auth \_ Connect \_ Layer \_ V {4 \| 6}**](built-in-callout-identifiers.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-109">The 4-second lifetime is specified by the built-in callout [**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}**](built-in-callout-identifiers.md).</span></span> <span data-ttu-id="8f0d8-110">Um die Standard Lebensdauer von 4 Sekunden zu ändern, fügen Sie einen Filter hinzu, der auf die **fwpm-Legenden \_ Set- \_ \_ Optionen \_ auth \_ Connect \_ Layer \_ V {4 \| 6}** Legende verweist.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-110">To alter the 4-second default lifetime, add a filter that references the **FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}** callout.</span></span> <span data-ttu-id="8f0d8-111">Weitere Informationen finden Sie unter [ALE Fluss Anpassung](ale-flow-customization.md) .</span><span class="sxs-lookup"><span data-stu-id="8f0d8-111">See [ALE Flow Customization](ale-flow-customization.md) for more information.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8f0d8-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f0d8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f0d8-113">Durchsetzung der Anwendungsschicht (ALE)</span><span class="sxs-lookup"><span data-stu-id="8f0d8-113">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="8f0d8-114">ALE Ebenen</span><span class="sxs-lookup"><span data-stu-id="8f0d8-114">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="8f0d8-115">Status behaftete ALE Filterung</span><span class="sxs-lookup"><span data-stu-id="8f0d8-115">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="8f0d8-116">Erneute ALE-Autorisierung</span><span class="sxs-lookup"><span data-stu-id="8f0d8-116">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="8f0d8-117">Anpassung des ALE-Flows</span><span class="sxs-lookup"><span data-stu-id="8f0d8-117">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 




