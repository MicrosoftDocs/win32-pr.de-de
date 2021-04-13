---
title: Transportmodus
description: Im Transportmodus-IPSec-Richtlinien Szenario ist der IPSec-Transportmodus für den gesamten übereinstimmenden Datenverkehr erforderlich
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb927aff1b3f0e3c7fd13a192f0fcb18fc3ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390229"
---
# <a name="transport-mode"></a><span data-ttu-id="e0050-103">Transportmodus</span><span class="sxs-lookup"><span data-stu-id="e0050-103">Transport Mode</span></span>

<span data-ttu-id="e0050-104">Im Transportmodus-IPSec-Richtlinien Szenario ist der IPSec-Transportmodus für den gesamten übereinstimmenden Datenverkehr erforderlich</span><span class="sxs-lookup"><span data-stu-id="e0050-104">The Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="e0050-105">Alle übereinstimmenden Klartext-Datenverkehr wird gelöscht, bis die IKE-oder AuthIP-Aushandlung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e0050-105">Any matching clear text traffic is dropped until the IKE or AuthIP negotiation has completed successfully.</span></span> <span data-ttu-id="e0050-106">Wenn die Aushandlung fehlschlägt, bleibt die Konnektivität mit der entsprechenden IP-Adresse beschädigt.</span><span class="sxs-lookup"><span data-stu-id="e0050-106">If the negotiation fails, connectivity with the corresponding IP address will remain broken.</span></span>

<span data-ttu-id="e0050-107">Ein Beispiel für ein mögliches transportmodusszenario ist "Secure all Unicast Data Traffic, außer ICMP, Using IPSec Transport Mode".</span><span class="sxs-lookup"><span data-stu-id="e0050-107">An example of a possible Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode."</span></span>

<span data-ttu-id="e0050-108">Um dieses Beispielprogramm gesteuert zu implementieren, verwenden Sie die folgende WFP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e0050-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="e0050-109">**Auf der swpm- \_ Schicht \_ IKEEXT \_ V {4 \| 6} Einrichten der mm-Aushandlungs Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="e0050-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="e0050-110">Fügen Sie einen oder beide der folgenden mm-Richtlinien Anbieter Kontexte hinzu.</span><span class="sxs-lookup"><span data-stu-id="e0050-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="e0050-111">Für IKE ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ IKE \_ mm \_ context**".</span><span class="sxs-lookup"><span data-stu-id="e0050-111">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="e0050-112">Für AuthIP ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ AuthIP \_ mm \_ context**".</span><span class="sxs-lookup"><span data-stu-id="e0050-112">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="e0050-113">Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende mm-Richtlinie wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="e0050-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="e0050-114">AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e0050-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="e0050-115">Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="e0050-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="e0050-116">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e0050-116">Filter property</span></span>        | <span data-ttu-id="e0050-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e0050-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="e0050-118">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="e0050-118">Filtering conditions</span></span>   | <span data-ttu-id="e0050-119">Leer.</span><span class="sxs-lookup"><span data-stu-id="e0050-119">Empty.</span></span> <span data-ttu-id="e0050-120">Der gesamte Datenverkehr entspricht dem Filter.</span><span class="sxs-lookup"><span data-stu-id="e0050-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="e0050-121">**providercontextkey**</span><span class="sxs-lookup"><span data-stu-id="e0050-121">**providerContextKey**</span></span> | <span data-ttu-id="e0050-122">GUID des in Schritt 1 hinzugefügten mm-Anbieter Kontexts.</span><span class="sxs-lookup"><span data-stu-id="e0050-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="e0050-123">**Auf der swpm- \_ Ebene \_ IPSec \_ V {4 \| 6} Setup-und EM-Aushandlungs Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="e0050-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="e0050-124">Fügen Sie einen oder beide der folgenden Einstellungen für den Transportmodus-Richtlinien Anbieter des-Transportmodus hinzu</span><span class="sxs-lookup"><span data-stu-id="e0050-124">Add one or both of the following QM transport mode policy provider contexts.</span></span>  
    -   <span data-ttu-id="e0050-125">Für IKE ein Richtlinien Anbieter Kontext vom Typ " **WPM- \_ IPSec- \_ IKE- \_ Quadrat- \_ Transport \_ Kontext**".</span><span class="sxs-lookup"><span data-stu-id="e0050-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="e0050-126">Für AuthIP ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ AuthIP \_ qm \_ Transport \_ context**".</span><span class="sxs-lookup"><span data-stu-id="e0050-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="e0050-127">Dieser Kontext kann optional die Richtlinie "AuthIP Extended Mode" (EM) aushandeln enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0050-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="e0050-128">Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende hoch Richtlinie wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="e0050-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="e0050-129">AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e0050-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="e0050-130">Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="e0050-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="e0050-131">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e0050-131">Filter property</span></span>        | <span data-ttu-id="e0050-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e0050-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="e0050-133">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="e0050-133">Filtering conditions</span></span>   | <span data-ttu-id="e0050-134">Leer.</span><span class="sxs-lookup"><span data-stu-id="e0050-134">Empty.</span></span> <span data-ttu-id="e0050-135">Der gesamte Datenverkehr entspricht dem Filter.</span><span class="sxs-lookup"><span data-stu-id="e0050-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="e0050-136">**providercontextkey**</span><span class="sxs-lookup"><span data-stu-id="e0050-136">**providerContextKey**</span></span> | <span data-ttu-id="e0050-137">GUID des in Schritt 1 hinzugefügten ESDS-Anbieter Kontexts.</span><span class="sxs-lookup"><span data-stu-id="e0050-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="e0050-138">**Auf der swpm- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6} einrichten eingehender Filterregeln pro Paket**</span><span class="sxs-lookup"><span data-stu-id="e0050-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="e0050-139">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="e0050-139">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="e0050-140">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e0050-140">Filter property</span></span>                                                   | <span data-ttu-id="e0050-141">Wert</span><span class="sxs-lookup"><span data-stu-id="e0050-141">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="e0050-142">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="e0050-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="e0050-143">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="e0050-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="e0050-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="e0050-144">**action.type**</span></span>                                                   | <span data-ttu-id="e0050-145">aufrufende f- \_ Aktions Legende \_ \_</span><span class="sxs-lookup"><span data-stu-id="e0050-145">FWP\_ACTION\_CALLOUT\_TERMINATING</span></span>                             |
    | <span data-ttu-id="e0050-146">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="e0050-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="e0050-147">Swpm-Legende \_ \_ IPSec- \_ Eingangs \_ Transport \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="e0050-147">FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>             |

        
2.  <span data-ttu-id="e0050-148">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e0050-148">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="e0050-149">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e0050-149">Filter property</span></span>                                                  | <span data-ttu-id="e0050-150">Wert</span><span class="sxs-lookup"><span data-stu-id="e0050-150">Value</span></span>                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | <span data-ttu-id="e0050-151">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="e0050-151">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="e0050-152">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="e0050-152">NlatUnicast</span></span>                                                               |
    | <span data-ttu-id="e0050-153">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="e0050-153">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>            | <span data-ttu-id="e0050-154">Ipproto \_ ICMP {V6} diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="e0050-154">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/>    |
    | <span data-ttu-id="e0050-155">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="e0050-155">**action.type**</span></span>                                                  | <span data-ttu-id="e0050-156">f/a- \_ Aktion \_ zulassen</span><span class="sxs-lookup"><span data-stu-id="e0050-156">FWP\_ACTION\_PERMIT</span></span>                                                       |
    | <span data-ttu-id="e0050-157">**weight**</span><span class="sxs-lookup"><span data-stu-id="e0050-157">**weight**</span></span>                                                       | [<span data-ttu-id="e0050-158">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e0050-158">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md) |

        

<span data-ttu-id="e0050-159">**Bei der WPM- \_ Schicht \_ ausgehende \_ Transport \_ V {4 \| 6} Einrichten von ausgehenden Regeln pro Paket Filtern**</span><span class="sxs-lookup"><span data-stu-id="e0050-159">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="e0050-160">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="e0050-160">Add a filter with the following properties.</span></span>
    | <span data-ttu-id="e0050-161">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e0050-161">Filter property</span></span>                                                   | <span data-ttu-id="e0050-162">Wert</span><span class="sxs-lookup"><span data-stu-id="e0050-162">Value</span></span>                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | <span data-ttu-id="e0050-163">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="e0050-163">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="e0050-164">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="e0050-164">NlatUnicast</span></span>                                        |
    | <span data-ttu-id="e0050-165">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="e0050-165">**action.type**</span></span>                                                   | <span data-ttu-id="e0050-166">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e0050-166">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>              |
    | <span data-ttu-id="e0050-167">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="e0050-167">**action.calloutKey**</span></span>                                             | <span data-ttu-id="e0050-168">WPM-Legende \_ \_ IPSec- \_ ausgehenden \_ Transport \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="e0050-168">FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span> |

        
2.  <span data-ttu-id="e0050-169">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e0050-169">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="e0050-170">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e0050-170">Filter property</span></span>                                                   | <span data-ttu-id="e0050-171">Wert</span><span class="sxs-lookup"><span data-stu-id="e0050-171">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="e0050-172">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="e0050-172">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="e0050-173">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="e0050-173">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="e0050-174">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="e0050-174">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="e0050-175">Ipproto \_ ICMP {V6} diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="e0050-175">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="e0050-176">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="e0050-176">**action.type**</span></span>                                                   | <span data-ttu-id="e0050-177">f/a- \_ Aktion \_ zulassen</span><span class="sxs-lookup"><span data-stu-id="e0050-177">FWP\_ACTION\_PERMIT</span></span>                                                    |
    | <span data-ttu-id="e0050-178">**weight**</span><span class="sxs-lookup"><span data-stu-id="e0050-178">**weight**</span></span>                                                        | <span data-ttu-id="e0050-179">IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_</span><span class="sxs-lookup"><span data-stu-id="e0050-179">FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="e0050-180">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0050-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0050-181">Beispielcode: Verwenden des Transport Modus</span><span class="sxs-lookup"><span data-stu-id="e0050-181">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="e0050-182">**Filtern von ebenenbezeichgern**</span><span class="sxs-lookup"><span data-stu-id="e0050-182">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="e0050-183">**Anbieter Kontext Typen**</span><span class="sxs-lookup"><span data-stu-id="e0050-183">**Provider Context Types**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[<span data-ttu-id="e0050-184">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="e0050-184">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="e0050-185">**\_ACTION0**</span><span class="sxs-lookup"><span data-stu-id="e0050-185">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="e0050-186">**Integrierte Legenden Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="e0050-186">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> </dl>

 

