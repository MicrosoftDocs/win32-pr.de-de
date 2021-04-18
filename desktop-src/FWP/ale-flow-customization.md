---
title: Anpassung des ALE-Flows
description: Die Netzwerk Filterung auf der Ebene (Application Layer Enforcement, ALE) der Windows-Filter Plattform (WFP) kann durch Hinzufügen von Filtern mit bestimmten Klassifikations Optionen angepasst werden.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9843a60719f424403139885f24f165c0dd936b
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314368"
---
# <a name="ale-flow-customization"></a><span data-ttu-id="e83b5-103">Anpassung des ALE-Flows</span><span class="sxs-lookup"><span data-stu-id="e83b5-103">ALE Flow Customization</span></span>

<span data-ttu-id="e83b5-104">Die Netzwerk Filterung auf der Ebene (Application Layer Enforcement, ALE) der Windows-Filter Plattform (WFP) kann durch Hinzufügen von Filtern mit bestimmten Klassifikations Optionen angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="e83b5-104">Network filtering at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) can be customized by adding filters with specific classify options.</span></span>

## <a name="multicastbroadcast-traffic"></a><span data-ttu-id="e83b5-105">Multicast/Broadcast-Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="e83b5-105">Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="e83b5-106">Fügen Sie zum Blockieren von eingehendem Datenverkehr, der auf ausgehenden Multicast-oder Broadcast Zuständen basiert, einen Filter hinzu, der ausgehenden Multicast-und Broadcast Datenverkehr autorisiert, und für die die FWP-Option " [**\_ \_ \_ Multicast- \_ Status**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) " auf **FWP- \_ Option \_ Wert " \_ \_ Multicast \_ Status ablehnen**"</span><span class="sxs-lookup"><span data-stu-id="e83b5-106">To block inbound traffic based on outbound multicast or broadcast states, add a filter that authorizes outbound multicast and broadcast traffic and that has the [**FWP\_CLASSIFY\_OPTION\_MULTICAST\_STATE**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_DENY\_MULTICAST\_STATE**.</span></span>

## <a name="remote-peers"></a><span data-ttu-id="e83b5-107">Remote Peers</span><span class="sxs-lookup"><span data-stu-id="e83b5-107">Remote Peers</span></span>

<span data-ttu-id="e83b5-108">Fügen Sie einen Filter mit der Option FWP-klassifizieren, wenn die Option freie [**\_ \_ \_ \_ Quell \_ Zuordnung**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) **aktivieren auf FWP- \_ Option \_ Wert \_ \_ lose \_ Quell \_ Zuordnung aktivieren** festgelegt ist, um Antwort Pakete von unterschiedlichen Peers dem gleichen Datenfluss hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e83b5-108">To add response packets from different peers to the same ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_LOOSE\_SOURCE\_MAPPING**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_ENABLE\_LOOSE\_SOURCE\_MAPPING**.</span></span>

<span data-ttu-id="e83b5-109">Siehe [Verwenden von klassifizier Optionen](using-classify-options.md) für Codebeispiele.</span><span class="sxs-lookup"><span data-stu-id="e83b5-109">See [Using Classify Options](using-classify-options.md) for code sample.</span></span>

## <a name="ale-flow-lifetime"></a><span data-ttu-id="e83b5-110">ALE Fluss Lebensdauer</span><span class="sxs-lookup"><span data-stu-id="e83b5-110">ALE Flow Lifetime</span></span>

<span data-ttu-id="e83b5-111">Fügen Sie zum Ändern der Leerlauf Timeout Werte für einen ALE-Datenfluss einen Filter mit der Option [**FWP- \_ klassifizieren- \_ Option \_ mcast \_ Bcast \_ Lifetime**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) und/oder der Option **\_ \_ \_ \_ unicastlebensdauer für die FWP-klassifizier Option** auf den gewünschten Leerlauf Timeout Wert fest.</span><span class="sxs-lookup"><span data-stu-id="e83b5-111">To modify the idle timeout values for an ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_MCAST\_BCAST\_LIFETIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option and/or the **FWP\_CLASSIFY\_OPTION\_UNICAST\_LIFETIME** option set to the desired idle timeout value.</span></span>

<span data-ttu-id="e83b5-112">Siehe [Verwenden von klassifizier Optionen](using-classify-options.md) für ein Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="e83b5-112">See [Using Classify Options](using-classify-options.md) for a code sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e83b5-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e83b5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e83b5-114">Durchsetzung der Anwendungsschicht (ALE)</span><span class="sxs-lookup"><span data-stu-id="e83b5-114">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="e83b5-115">ALE Ebenen</span><span class="sxs-lookup"><span data-stu-id="e83b5-115">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="e83b5-116">Status behaftete ALE Filterung</span><span class="sxs-lookup"><span data-stu-id="e83b5-116">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="e83b5-117">ALE Multicast-/Broadcast Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="e83b5-117">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="e83b5-118">Erneute ALE-Autorisierung</span><span class="sxs-lookup"><span data-stu-id="e83b5-118">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="e83b5-119">Verwenden von klassifizier Optionen</span><span class="sxs-lookup"><span data-stu-id="e83b5-119">Using Classify Options</span></span>](using-classify-options.md)
</dt> </dl>

 

 




