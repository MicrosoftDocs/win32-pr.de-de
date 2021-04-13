---
title: IKE-/AuthIP-Ausnahmen
description: Internetschlüsselaustausch (IKE) und authentifiziertes Internetprotokoll (AuthIP) müssen den Netzwerk Datenverkehr von der IPSec-Filterung ausschließen, damit Sie funktionieren.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389932"
---
# <a name="ikeauthip-exemptions"></a><span data-ttu-id="bc0a5-103">IKE-/AuthIP-Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="bc0a5-103">IKE/AuthIP Exemptions</span></span>

<span data-ttu-id="bc0a5-104">Die IPSec (Internet Protocol Security)-Schlüssel Bindungs Internetschlüsselaustausch Module (Internet Protocol Security, IKE) und authentifiziertes Internetprotokoll (AuthIP) müssen den Netzwerk Datenverkehr von der IPSec-Filterung ausschließen, damit Sie funktionieren.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-104">The Internet Protocol security (IPsec) keying modules, Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP), in order to function, need to exempt their network traffic from the IPsec filtering.</span></span>

<span data-ttu-id="bc0a5-105">In der Windows-Filter Plattform (WFP) fügt das Basis Filtermodul (BFE) automatisch IKE-und AuthIP-Ausnahme Filter hinzu, wenn der erste IKE-oder AuthIP-hauptmodusrichtlinienfilter hinzugefügt wird, und löscht diese, wenn der letzte IKE-oder AuthIP mm-Richtlinien Filter gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-105">In Windows Filtering Platform (WFP) the Base Filtering Engine (BFE) automatically adds IKE and AuthIP exemption filters when the first IKE or AuthIP main mode (MM) policy filter is added and deletes them when the last IKE or AuthIP MM policy filter is deleted.</span></span> <span data-ttu-id="bc0a5-106">Auf diese Weise müssen die Richtlinien Anbieter nicht die IKE-und AuthIP-Filter Ausnahmen einzeln verwalten.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-106">This way, the policy providers do not have to manage IKE and AuthIP filtering exemptions individually.</span></span>

<span data-ttu-id="bc0a5-107">Ein IKE mm-Richtlinien Filter ist ein Filter in der-Engine-Schicht der [**swpm- \_ Schicht \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , die auf einen Anbieter Kontext vom Typ " [**swpm \_ IPSec \_ IKE \_ mm \_ context**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)" verweist.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-107">An IKE MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_IKE\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="bc0a5-108">Ein AuthIP mm-Richtlinien Filter ist ein Filter in der-Engine-Schicht der [**swpm- \_ Schicht \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , die auf einen Anbieter Kontext vom Typ " [**swpm \_ IPSec \_ AuthIP \_ mm \_ context**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)" verweist.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-108">An AuthIP MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="bc0a5-109">Ein IKE-oder AuthIP-Ausnahme Filter ist ein Filter in der-Engine-Schicht für den [**\_ eingehenden \_ \_ Transport \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) oder den **ausgehenden \_ \_ \_ Transport \_ v {4 \| 6** }, der sich im Bereich der [**\_ \_ \_ IKE- \_ Ausnahmen**](filter-weight-identifiers.md) für den Bereich für den schwere Bereich von swpm befindet.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-109">An IKE or AuthIP exemption filter is a filter in the engine layer [**FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}**](management-filtering-layer-identifiers-.md) or **FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}** auto-weighted in the [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md) weight range.</span></span>

<span data-ttu-id="bc0a5-110">Die von BFE implementierten IKE-und AuthIP-Ausnahmen lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-110">The IKE and AuthIP exemptions implemented by BFE are as follows.</span></span>

| <span data-ttu-id="bc0a5-111">IP-Version</span><span class="sxs-lookup"><span data-stu-id="bc0a5-111">IP version</span></span>      | <span data-ttu-id="bc0a5-112">Port</span><span class="sxs-lookup"><span data-stu-id="bc0a5-112">Port</span></span>                        | <span data-ttu-id="bc0a5-113">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="bc0a5-113">Exemption</span></span>                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0a5-114">IPv4</span><span class="sxs-lookup"><span data-stu-id="bc0a5-114">IPv4</span></span><br/> | <span data-ttu-id="bc0a5-115">UDP: 500 UDP: 4500</span><span class="sxs-lookup"><span data-stu-id="bc0a5-115">UDP:500 UDP:4500</span></span><br/> | <span data-ttu-id="bc0a5-116">Erlauben Sie IKE-und AuthIP-Datenverkehr auf der eingehenden Transportschicht und der ausgehenden Transportschicht.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-116">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="bc0a5-117">Hiermit wird der IKE-und AuthIP-Datenverkehr auf der ALE Empfangs-/Accept-und Connect-Schicht zugelassen, aber auf das lokale System beschränkt.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-117">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |
| <span data-ttu-id="bc0a5-118">IPv6</span><span class="sxs-lookup"><span data-stu-id="bc0a5-118">IPv6</span></span><br/> | <span data-ttu-id="bc0a5-119">UDP: 500</span><span class="sxs-lookup"><span data-stu-id="bc0a5-119">UDP:500</span></span><br/>          | <span data-ttu-id="bc0a5-120">Erlauben Sie IKE-und AuthIP-Datenverkehr auf der eingehenden Transportschicht und der ausgehenden Transportschicht.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-120">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="bc0a5-121">Hiermit wird der IKE-und AuthIP-Datenverkehr auf der ALE Empfangs-/Accept-und Connect-Schicht zugelassen, aber auf das lokale System beschränkt.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-121">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |



 

<span data-ttu-id="bc0a5-122">Die IKE-und AuthIP-Ausnahme Filter sind für alle Adressen offen.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-122">The IKE and AuthIP exemption filters are open to all addresses.</span></span> <span data-ttu-id="bc0a5-123">Zum Implementieren einer Firewall mit präziserer Kontrolle sollten Richtlinien Anbieter Filter in einem Gewichtungs Bereich hinzufügen, der höher als der [**fwpm- \_ Gewichtungs \_ Bereich von \_ IKE- \_ Ausnahmen**](filter-weight-identifiers.md)ist.</span><span class="sxs-lookup"><span data-stu-id="bc0a5-123">To implement a firewall with more granular control, policy providers should add filters in a weight range higher than [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc0a5-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc0a5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc0a5-125">IPSec-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="bc0a5-125">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="bc0a5-126">Filtergewichtungszuweisung</span><span class="sxs-lookup"><span data-stu-id="bc0a5-126">Filter Weight Assignment</span></span>](filter-weight-assignment.md)
</dt> </dl>

 

 





