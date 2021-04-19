---
title: Transport Modus für die Aushandlung von Aushandlungen im Begrenzungs Modus
description: Der Transportmodus für die Aushandlung-Ermittlung im Richtlinien-IPSec-Richtlinien Szenario fordert IPSec-Transportmodus für den gesamten übereinstimmenden Datenverkehr an
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9869be61923bff1c392c5abe2bd98099a0c3c89f
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314593"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a><span data-ttu-id="57812-103">Transport Modus für die Aushandlung von Aushandlungen im Begrenzungs Modus</span><span class="sxs-lookup"><span data-stu-id="57812-103">Negotiation Discovery Transport Mode in Boundary Mode</span></span>

<span data-ttu-id="57812-104">Der Transportmodus für die Aushandlung-Ermittlung im Richtlinien-IPSec-Richtlinien Szenario fordert IPSec-Transportmodus für den gesamten übereinstimmenden Datenverkehr an</span><span class="sxs-lookup"><span data-stu-id="57812-104">The Negotiation Discovery Transport Mode in Boundary Mode IPsec policy scenario requests IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="57812-105">Wenn die IKE-/AuthIP-Aushandlung fehlschlägt, können eingehende und ausgehende Verbindungen auf Klartext zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="57812-105">If the IKE/AuthIP negotiation fails, both inbound and outbound connections are allowed to fallback to clear-text .</span></span>

<span data-ttu-id="57812-106">Diese IPSec-Richtlinie wird in der Regel auf Computern verwendet, auf die sowohl IPsec-fähige als auch nicht-IPsec-fähige Computer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="57812-106">This IPsec policy is typically used on machines that are accessed by both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="57812-107">Ein Beispiel für ein mögliches Aushandlungs Ermittlungs-transportmodusszenario ist "Secure all Unicast Data Traffic, außer ICMP, Using IPSec Transport Mode and enable Aushandlung Discovery in Border Mode".</span><span class="sxs-lookup"><span data-stu-id="57812-107">An example of a potential Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode and enable negotiation discovery in boundary mode."</span></span>

<span data-ttu-id="57812-108">Um dieses Beispielprogramm gesteuert zu implementieren, verwenden Sie die folgende WFP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="57812-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="57812-109">**Auf der swpm- \_ Schicht \_ IKEEXT \_ V {4 \| 6} Einrichten der mm-Aushandlungs Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="57812-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="57812-110">Fügen Sie einen oder beide der folgenden mm-Richtlinien Anbieter Kontexte hinzu.</span><span class="sxs-lookup"><span data-stu-id="57812-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="57812-111">Für IKE ein Richtlinien Anbieter Kontext vom Typ "swpm \_ IPSec \_ IKE \_ mm \_ context".</span><span class="sxs-lookup"><span data-stu-id="57812-111">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="57812-112">Für AuthIP ein Richtlinien Anbieter Kontext vom Typ "swpm \_ IPSec \_ AuthIP \_ mm \_ context".</span><span class="sxs-lookup"><span data-stu-id="57812-112">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="57812-113">Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende mm-Richtlinie wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="57812-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="57812-114">AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="57812-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="57812-115">Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="57812-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="57812-116">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="57812-116">Filter property</span></span>        | <span data-ttu-id="57812-117">Wert</span><span class="sxs-lookup"><span data-stu-id="57812-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="57812-118">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="57812-118">Filtering conditions</span></span>   | <span data-ttu-id="57812-119">Leer.</span><span class="sxs-lookup"><span data-stu-id="57812-119">Empty.</span></span> <span data-ttu-id="57812-120">Der gesamte Datenverkehr entspricht dem Filter.</span><span class="sxs-lookup"><span data-stu-id="57812-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="57812-121">**providercontextkey**</span><span class="sxs-lookup"><span data-stu-id="57812-121">**providerContextKey**</span></span> | <span data-ttu-id="57812-122">GUID des in Schritt 1 hinzugefügten mm-Anbieter Kontexts.</span><span class="sxs-lookup"><span data-stu-id="57812-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="57812-123">**Auf der swpm- \_ Ebene \_ IPSec \_ V {4 \| 6} Setup-und EM-Aushandlungs Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="57812-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="57812-124">Fügen Sie einen oder beide der folgenden Einstellungen für den Transportmodus-Richtlinien Anbieter hinzu, und legen Sie das Richtlinienflag der [**IPSec- \_ Richtlinie \_ \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) fest.</span><span class="sxs-lookup"><span data-stu-id="57812-124">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_BOUNDARY**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="57812-125">Für IKE ein Richtlinien Anbieter Kontext vom Typ " **WPM- \_ IPSec- \_ IKE- \_ Quadrat- \_ Transport \_ Kontext**".</span><span class="sxs-lookup"><span data-stu-id="57812-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="57812-126">Für AuthIP ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ AuthIP \_ qm \_ Transport \_ context**".</span><span class="sxs-lookup"><span data-stu-id="57812-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="57812-127">Dieser Kontext kann optional die Richtlinie "AuthIP Extended Mode" (EM) aushandeln enthalten.</span><span class="sxs-lookup"><span data-stu-id="57812-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="57812-128">Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende hoch Richtlinie wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="57812-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="57812-129">AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="57812-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="57812-130">Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="57812-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="57812-131">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="57812-131">Filter property</span></span>        | <span data-ttu-id="57812-132">Wert</span><span class="sxs-lookup"><span data-stu-id="57812-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="57812-133">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="57812-133">Filtering conditions</span></span>   | <span data-ttu-id="57812-134">Leer.</span><span class="sxs-lookup"><span data-stu-id="57812-134">Empty.</span></span> <span data-ttu-id="57812-135">Der gesamte Datenverkehr entspricht dem Filter.</span><span class="sxs-lookup"><span data-stu-id="57812-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="57812-136">**providercontextkey**</span><span class="sxs-lookup"><span data-stu-id="57812-136">**providerContextKey**</span></span> | <span data-ttu-id="57812-137">GUID des in Schritt 1 hinzugefügten ESDS-Anbieter Kontexts.</span><span class="sxs-lookup"><span data-stu-id="57812-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="57812-138">**Auf der swpm- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6} einrichten eingehender Filterregeln pro Paket**</span><span class="sxs-lookup"><span data-stu-id="57812-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="57812-139">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="57812-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="57812-140">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="57812-140">Filter property</span></span>                                                   | <span data-ttu-id="57812-141">Wert</span><span class="sxs-lookup"><span data-stu-id="57812-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="57812-142">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="57812-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="57812-143">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="57812-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="57812-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="57812-144">**action.type**</span></span>                                                   | <span data-ttu-id="57812-145">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57812-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="57812-146">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="57812-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="57812-147">**Swpm-Legende \_ \_ IPSec- \_ Eingangs \_ Transport \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="57812-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="57812-148">**rawcontext**</span><span class="sxs-lookup"><span data-stu-id="57812-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="57812-149">**swpm-Kontext-IPSec-eingehende Beibehaltung der \_ \_ \_ \_ \_ Verbindungs \_ Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="57812-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="57812-150">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="57812-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="57812-151">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="57812-151">Filter property</span></span>                                                   | <span data-ttu-id="57812-152">Wert</span><span class="sxs-lookup"><span data-stu-id="57812-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="57812-153">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="57812-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="57812-154">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="57812-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="57812-155">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="57812-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="57812-156">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="57812-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="57812-157">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="57812-157">**action.type**</span></span>                                                   | <span data-ttu-id="57812-158">f/a- \_ Aktion \_ zulassen</span><span class="sxs-lookup"><span data-stu-id="57812-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="57812-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="57812-159">**weight**</span></span>                                                        | [<span data-ttu-id="57812-160">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57812-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="57812-161">**Bei der WPM- \_ Schicht \_ ausgehende \_ Transport \_ V {4 \| 6} Einrichten von ausgehenden Regeln pro Paket Filtern**</span><span class="sxs-lookup"><span data-stu-id="57812-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="57812-162">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="57812-162">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="57812-163">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="57812-163">Filter property</span></span>                                                   | <span data-ttu-id="57812-164">Wert</span><span class="sxs-lookup"><span data-stu-id="57812-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="57812-165">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="57812-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="57812-166">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="57812-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="57812-167">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="57812-167">**action.type**</span></span>                                                   | <span data-ttu-id="57812-168">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57812-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="57812-169">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="57812-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="57812-170">**WPM-Legende \_ \_ IPSec- \_ ausgehenden \_ Transport \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="57812-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="57812-171">**rawcontext**</span><span class="sxs-lookup"><span data-stu-id="57812-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="57812-172">**WPM- \_ Kontext- \_ IPSec \_ ausgehende \_ Aushandlungs Aushandlung \_ ermitteln**</span><span class="sxs-lookup"><span data-stu-id="57812-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="57812-173">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="57812-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="57812-174">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="57812-174">Filter property</span></span>                                                   | <span data-ttu-id="57812-175">Wert</span><span class="sxs-lookup"><span data-stu-id="57812-175">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="57812-176">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="57812-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="57812-177">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="57812-177">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="57812-178">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="57812-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="57812-179">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="57812-179">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="57812-180">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="57812-180">**action.type**</span></span>                                                   | <span data-ttu-id="57812-181">**f/a- \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="57812-181">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="57812-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="57812-182">**weight**</span></span>                                                        | <span data-ttu-id="57812-183">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57812-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

> [!Note]  
> <span data-ttu-id="57812-184">Im Gegensatz zum Transportmodus für die Aushandlungs Ermittlung ist für den Transportmodus für die Aushandlung von Aushandlungs Modus in der Richtlinie für den Begrenzungs Modus kein Filter auf der **fwpm- \_ Schicht der Ebene " \_ \_ \_ \_ Accept \_ v {4 \| 6}** " erforderlich, da diese Richtlinie eingehende ungeschützte Clear-Text-Verbindungen zulässt.</span><span class="sxs-lookup"><span data-stu-id="57812-184">As opposed to Negotiation Discovery Transport Mode, for Negotiation Discovery Transport Mode in Boundary Mode policy there is no need to add a filter at the **FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}** layers because this policy allows inbound unprotected clear-text connections.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="57812-185">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57812-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57812-186">Beispielcode: Verwenden des Transport Modus</span><span class="sxs-lookup"><span data-stu-id="57812-186">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="57812-187">ALE Ebenen</span><span class="sxs-lookup"><span data-stu-id="57812-187">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="57812-188">**Integrierte Legenden Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="57812-188">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="57812-189">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="57812-189">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="57812-190">**Filtern von ebenenbezeichgern**</span><span class="sxs-lookup"><span data-stu-id="57812-190">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="57812-191">**\_ACTION0**</span><span class="sxs-lookup"><span data-stu-id="57812-191">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="57812-192">**Kontexttyp des WPM- \_ Anbieters \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57812-192">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

