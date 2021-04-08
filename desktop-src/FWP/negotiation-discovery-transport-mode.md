---
title: Transport Modus für Aushandlungs Ermittlung
description: Das Szenario für das Aushandeln von Aushandlungs Ermittlungs-Transportmodus erfordert IPSec-Transportmodus für den gesamten eingehenden eingehenden Datenverkehr und fordert den IPSec-Schutz für den Abgleich des ausgehenden Datenverkehrs
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9477d18f2fe478f5c885c071f47d0bf2baaad8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858171"
---
# <a name="negotiation-discovery-transport-mode"></a><span data-ttu-id="a4879-103">Transport Modus für Aushandlungs Ermittlung</span><span class="sxs-lookup"><span data-stu-id="a4879-103">Negotiation Discovery Transport Mode</span></span>

<span data-ttu-id="a4879-104">Das Szenario für das Aushandeln von Aushandlungs Ermittlungs-Transportmodus erfordert IPSec-Transportmodus für den gesamten eingehenden eingehenden Datenverkehr und fordert den IPSec-Schutz für den Abgleich des ausgehenden Datenverkehrs</span><span class="sxs-lookup"><span data-stu-id="a4879-104">The Negotiation Discovery Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching inbound traffic, and requests IPsec protection for matching outbound traffic.</span></span> <span data-ttu-id="a4879-105">Daher können ausgehende Verbindungen auf Clear-Text zurückgreifen, wenn eingehende Verbindungen nicht bestehen.</span><span class="sxs-lookup"><span data-stu-id="a4879-105">Therefore, outbound connections are allowed to fallback to clear-text while inbound connections are not.</span></span>

<span data-ttu-id="a4879-106">Wenn der Host Computer mit dieser Richtlinie versucht, eine neue ausgehende Verbindung herzustellen, und keine IPSec-SA vorhanden ist, die mit dem Datenverkehr übereinstimmt, sendet der Host die Pakete gleichzeitig als Klartext und startet eine IKE-oder AuthIP-Aushandlung.</span><span class="sxs-lookup"><span data-stu-id="a4879-106">With this policy, when the host machine attempts a new outbound connection and there is no existing IPsec SA matching the traffic, the host simultaneously sends the packets in clear-text and starts an IKE or AuthIP negotiation.</span></span> <span data-ttu-id="a4879-107">Wenn die Aushandlung erfolgreich ist, wird die Verbindung auf IPSec-Protected aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a4879-107">If the negotiation succeeds, the connection is upgraded to IPsec-protected.</span></span> <span data-ttu-id="a4879-108">Andernfalls bleibt die Verbindung Klartext.</span><span class="sxs-lookup"><span data-stu-id="a4879-108">Otherwise, the connection stays in clear-text.</span></span> <span data-ttu-id="a4879-109">Wenn IPSec-geschützt ist, kann eine Verbindung nie auf Klartext herabgestuft werden.</span><span class="sxs-lookup"><span data-stu-id="a4879-109">Once IPsec-protected, a connection can never be downgraded to clear-text.</span></span>

<span data-ttu-id="a4879-110">Der Transport Modus für die Aushandlung von Aushandlungen wird in der Regel in Umgebungen verwendet, die IPsec-fähige und nicht-IPsec-fähige Computer enthalten.</span><span class="sxs-lookup"><span data-stu-id="a4879-110">Negotiation Discovery Transport Mode is typically used in environments that include both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="a4879-111">Ein Beispiel für ein mögliches Aushandlungs Ermittlungs-transportmodusszenario ist "Secure all Unicast Data Traffic, außer ICMP, Using IPSec Transport Mode und enable Aushandlung Discovery".</span><span class="sxs-lookup"><span data-stu-id="a4879-111">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, and enable negotiation discovery."</span></span>

<span data-ttu-id="a4879-112">Um dieses Beispielprogramm gesteuert zu implementieren, verwenden Sie die folgende WFP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a4879-112">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="a4879-113">**Auf der swpm- \_ Schicht \_ IKEEXT \_ V {4 \| 6} Einrichten der mm-Aushandlungs Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="a4879-113">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} set up MM negotiation policy**</span></span>  

1.  <span data-ttu-id="a4879-114">Fügen Sie einen oder beide der folgenden mm-Richtlinien Anbieter Kontexte hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4879-114">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="a4879-115">Für IKE ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ IKE \_ mm \_ context**".</span><span class="sxs-lookup"><span data-stu-id="a4879-115">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="a4879-116">Für AuthIP ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ AuthIP \_ mm \_ context**".</span><span class="sxs-lookup"><span data-stu-id="a4879-116">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="a4879-117">Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende mm-Richtlinie wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="a4879-117">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="a4879-118">AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a4879-118">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="a4879-119">Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4879-119">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="a4879-120">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4879-120">Filter property</span></span>        | <span data-ttu-id="a4879-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a4879-121">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="a4879-122">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="a4879-122">Filtering conditions</span></span>   | <span data-ttu-id="a4879-123">Leer.</span><span class="sxs-lookup"><span data-stu-id="a4879-123">Empty.</span></span> <span data-ttu-id="a4879-124">Der gesamte Datenverkehr entspricht dem Filter.</span><span class="sxs-lookup"><span data-stu-id="a4879-124">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="a4879-125">**providercontextkey**</span><span class="sxs-lookup"><span data-stu-id="a4879-125">**providerContextKey**</span></span> | <span data-ttu-id="a4879-126">GUID des in Schritt 1 hinzugefügten mm-Anbieter Kontexts.</span><span class="sxs-lookup"><span data-stu-id="a4879-126">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="a4879-127">**Auf der swpm- \_ Ebene \_ IPSec \_ V {4 \| 6} Einrichten der hoch skalierungsrichtlinie und der EM-Aushandlungs Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="a4879-127">**At FWPM\_LAYER\_IPSEC\_V{4\|6} set up QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="a4879-128">Fügen Sie einen oder beide der folgenden Einstellungen für den Transportmodus-Richtlinien Anbieter hinzu, und legen Sie die [**IPSec-Richtlinienflag \_ \_ \_ nd \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) fest.</span><span class="sxs-lookup"><span data-stu-id="a4879-128">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="a4879-129">Für IKE ein Richtlinien Anbieter Kontext vom Typ "WPM- \_ IPSec- \_ IKE- \_ Quadrat- \_ Transport Kontext" \_ .</span><span class="sxs-lookup"><span data-stu-id="a4879-129">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT.</span></span>
    -   <span data-ttu-id="a4879-130">Für AuthIP ein Richtlinien Anbieter Kontext vom Typ "swpm \_ IPSec \_ AuthIP \_ qm \_ Transport \_ context".</span><span class="sxs-lookup"><span data-stu-id="a4879-130">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT.</span></span> <span data-ttu-id="a4879-131">Dieser Kontext kann optional die Richtlinie "AuthIP Extended Mode" (EM) aushandeln enthalten.</span><span class="sxs-lookup"><span data-stu-id="a4879-131">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="a4879-132">Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende hoch Richtlinie wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="a4879-132">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="a4879-133">AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a4879-133">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="a4879-134">Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4879-134">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="a4879-135">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4879-135">Filter property</span></span>        | <span data-ttu-id="a4879-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a4879-136">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="a4879-137">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="a4879-137">Filtering conditions</span></span>   | <span data-ttu-id="a4879-138">Leer.</span><span class="sxs-lookup"><span data-stu-id="a4879-138">Empty.</span></span> <span data-ttu-id="a4879-139">Der gesamte Datenverkehr entspricht dem Filter.</span><span class="sxs-lookup"><span data-stu-id="a4879-139">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="a4879-140">**providercontextkey**</span><span class="sxs-lookup"><span data-stu-id="a4879-140">**providerContextKey**</span></span> | <span data-ttu-id="a4879-141">GUID des in Schritt 1 hinzugefügten ESDS-Anbieter Kontexts.</span><span class="sxs-lookup"><span data-stu-id="a4879-141">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="a4879-142">**Auf der WPM- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6} richten Sie eingehende Filterregeln pro Paket ein.**</span><span class="sxs-lookup"><span data-stu-id="a4879-142">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} set up inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="a4879-143">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4879-143">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="a4879-144">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4879-144">Filter property</span></span>                                                   | <span data-ttu-id="a4879-145">Wert</span><span class="sxs-lookup"><span data-stu-id="a4879-145">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="a4879-146">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="a4879-146">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="a4879-147">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="a4879-147">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="a4879-148">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="a4879-148">**action.type**</span></span>                                                   | <span data-ttu-id="a4879-149">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4879-149">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="a4879-150">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="a4879-150">**action.calloutKey**</span></span>                                             | <span data-ttu-id="a4879-151">**Swpm-Legende \_ \_ IPSec- \_ Eingangs \_ Transport \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="a4879-151">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="a4879-152">**rawcontext**</span><span class="sxs-lookup"><span data-stu-id="a4879-152">**rawContext**</span></span>                                                    | [<span data-ttu-id="a4879-153">**swpm-Kontext-IPSec-eingehende Beibehaltung der \_ \_ \_ \_ \_ Verbindungs \_ Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="a4879-153">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="a4879-154">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a4879-154">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="a4879-155">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4879-155">Filter property</span></span>                                                   | <span data-ttu-id="a4879-156">Wert</span><span class="sxs-lookup"><span data-stu-id="a4879-156">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="a4879-157">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="a4879-157">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a4879-158">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="a4879-158">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="a4879-159">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="a4879-159">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="a4879-160">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="a4879-160">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="a4879-161">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="a4879-161">**action.type**</span></span>                                                   | <span data-ttu-id="a4879-162">**f/a- \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="a4879-162">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="a4879-163">**weight**</span><span class="sxs-lookup"><span data-stu-id="a4879-163">**weight**</span></span>                                                        | [<span data-ttu-id="a4879-164">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4879-164">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="a4879-165">**Auf der WPM- \_ Schicht der \_ ausgehende \_ Transport \_ V {4 \| 6} richten Sie ausgehende Filterregeln pro Paket ein.**</span><span class="sxs-lookup"><span data-stu-id="a4879-165">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} set up outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="a4879-166">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4879-166">Add a filter with the following properties.</span></span>
    | <span data-ttu-id="a4879-167">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4879-167">Filter property</span></span>                                                   | <span data-ttu-id="a4879-168">Wert</span><span class="sxs-lookup"><span data-stu-id="a4879-168">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="a4879-169">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="a4879-169">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a4879-170">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="a4879-170">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="a4879-171">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="a4879-171">**action.type**</span></span>                                                   | <span data-ttu-id="a4879-172">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4879-172">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="a4879-173">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="a4879-173">**action.calloutKey**</span></span>                                             | <span data-ttu-id="a4879-174">**WPM-Legende \_ \_ IPSec- \_ ausgehenden \_ Transport \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="a4879-174">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="a4879-175">**rawcontext**</span><span class="sxs-lookup"><span data-stu-id="a4879-175">**rawContext**</span></span>                                                    | [<span data-ttu-id="a4879-176">**WPM- \_ Kontext- \_ IPSec \_ ausgehende \_ Aushandlungs Aushandlung \_ ermitteln**</span><span class="sxs-lookup"><span data-stu-id="a4879-176">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="a4879-177">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a4879-177">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="a4879-178">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4879-178">Filter property</span></span>                                                   | <span data-ttu-id="a4879-179">Wert</span><span class="sxs-lookup"><span data-stu-id="a4879-179">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="a4879-180">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="a4879-180">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a4879-181">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="a4879-181">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="a4879-182">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="a4879-182">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="a4879-183">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="a4879-183">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="a4879-184">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="a4879-184">**action.type**</span></span>                                                   | <span data-ttu-id="a4879-185">**f/a- \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="a4879-185">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="a4879-186">**weight**</span><span class="sxs-lookup"><span data-stu-id="a4879-186">**weight**</span></span>                                                        | <span data-ttu-id="a4879-187">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4879-187">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="a4879-188">**Legen Sie auf der swpm- \_ Schicht \_ ALE Authentifizierung \_ \_ \_ \_ V {4 \| 6} eingehende Filterregeln pro Verbindung fest.**</span><span class="sxs-lookup"><span data-stu-id="a4879-188">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} set up inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="a4879-189">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4879-189">Add a filter with the following properties.</span></span> <span data-ttu-id="a4879-190">Dieser Filter lässt nur eingehende Verbindungsversuche zu, wenn Sie durch IPSec gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="a4879-190">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 
    | <span data-ttu-id="a4879-191">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4879-191">Filter property</span></span>                                                   | <span data-ttu-id="a4879-192">Wert</span><span class="sxs-lookup"><span data-stu-id="a4879-192">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="a4879-193">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="a4879-193">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a4879-194">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="a4879-194">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="a4879-195">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="a4879-195">**action.type**</span></span>                                                   | <span data-ttu-id="a4879-196">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4879-196">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="a4879-197">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="a4879-197">**action.calloutKey**</span></span>                                             | <span data-ttu-id="a4879-198">**WPM-Legende \_ \_ IPSec \_ eingehende \_ Initiierung \_ Secure \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="a4879-198">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="a4879-199">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a4879-199">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="a4879-200">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4879-200">Filter property</span></span>                                                   | <span data-ttu-id="a4879-201">Wert</span><span class="sxs-lookup"><span data-stu-id="a4879-201">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="a4879-202">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="a4879-202">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a4879-203">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="a4879-203">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="a4879-204">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="a4879-204">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="a4879-205">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="a4879-205">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="a4879-206">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="a4879-206">**action.type**</span></span>                                                   | <span data-ttu-id="a4879-207">**f/a- \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="a4879-207">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="a4879-208">**weight**</span><span class="sxs-lookup"><span data-stu-id="a4879-208">**weight**</span></span>                                                        | <span data-ttu-id="a4879-209">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4879-209">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="a4879-210">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4879-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4879-211">Beispielcode: Verwenden des Transport Modus</span><span class="sxs-lookup"><span data-stu-id="a4879-211">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="a4879-212">ALE Ebenen</span><span class="sxs-lookup"><span data-stu-id="a4879-212">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="a4879-213">**Integrierte Legenden Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="a4879-213">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="a4879-214">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="a4879-214">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="a4879-215">**Filtern von ebenenbezeichgern**</span><span class="sxs-lookup"><span data-stu-id="a4879-215">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="a4879-216">**\_ACTION0**</span><span class="sxs-lookup"><span data-stu-id="a4879-216">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="a4879-217">**Kontexttyp des WPM- \_ Anbieters \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4879-217">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

