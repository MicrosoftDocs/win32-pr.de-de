---
title: Garantierte Verschlüsselung
description: Das Szenario für die garantierte Verschlüsselung der IPSec-Richtlinie erfordert IPSec-Verschlüsselung für den gesamten übereinstimmenden Diese Richtlinie muss in Verbindung mit einer der Richtlinien Optionen für den Transportmodus angegeben werden.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbffa3d78a9e178850f3afaa4d6b7fa9831be875
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314643"
---
# <a name="guaranteed-encryption"></a><span data-ttu-id="b3579-104">Garantierte Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="b3579-104">Guaranteed Encryption</span></span>

<span data-ttu-id="b3579-105">Das Szenario für die garantierte Verschlüsselung der IPSec-Richtlinie erfordert IPSec-Verschlüsselung für den gesamten übereinstimmenden</span><span class="sxs-lookup"><span data-stu-id="b3579-105">The Guaranteed Encryption IPsec policy scenario requires IPsec encryption for all matching traffic.</span></span> <span data-ttu-id="b3579-106">Diese Richtlinie muss in Verbindung mit einer der Richtlinien Optionen für den Transportmodus angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b3579-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="b3579-107">Die garantierte Verschlüsselung wird normalerweise verwendet, um sensiblen Datenverkehr auf Anwendungs Basis zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="b3579-107">Guaranteed Encryption is typically used to encrypt sensitive traffic on a per application basis.</span></span>

<span data-ttu-id="b3579-108">Ein Beispiel für ein mögliches verschlüsseltes Verschlüsselungs Szenario ist "Secure all Unicast Data Traffic, außer ICMP, Using IPSec Transport Mode, Enable Aushandlung Discovery, and require eine garantierte Verschlüsselung für den gesamten Unicastdatenverkehr gemäß TCP-Port 5555."</span><span class="sxs-lookup"><span data-stu-id="b3579-108">An example of a possible Guaranteed Encryption scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and require guaranteed encryption for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="b3579-109">Um dieses Beispielprogramm gesteuert zu implementieren, verwenden Sie die folgende WFP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b3579-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="b3579-110">**Auf der swpm- \_ Schicht \_ IKEEXT \_ V {4 \| 6} Einrichten der mm-Aushandlungs Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="b3579-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="b3579-111">Fügen Sie einen oder beide der folgenden mm-Richtlinien Anbieter Kontexte hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3579-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="b3579-112">Für IKE ein Richtlinien Anbieter Kontext vom Typ "swpm \_ IPSec \_ IKE \_ mm \_ context".</span><span class="sxs-lookup"><span data-stu-id="b3579-112">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="b3579-113">Für AuthIP ein Richtlinien Anbieter Kontext vom Typ "swpm \_ IPSec \_ AuthIP \_ mm \_ context".</span><span class="sxs-lookup"><span data-stu-id="b3579-113">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="b3579-114">Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende mm-Richtlinie wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="b3579-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="b3579-115">AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b3579-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="b3579-116">Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3579-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="b3579-117">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b3579-117">Filter property</span></span>        | <span data-ttu-id="b3579-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b3579-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="b3579-119">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="b3579-119">Filtering conditions</span></span>   | <span data-ttu-id="b3579-120">Leer.</span><span class="sxs-lookup"><span data-stu-id="b3579-120">Empty.</span></span> <span data-ttu-id="b3579-121">Der gesamte Datenverkehr entspricht dem Filter.</span><span class="sxs-lookup"><span data-stu-id="b3579-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="b3579-122">**providercontextkey**</span><span class="sxs-lookup"><span data-stu-id="b3579-122">**providerContextKey**</span></span> | <span data-ttu-id="b3579-123">GUID des in Schritt 1 hinzugefügten mm-Anbieter Kontexts.</span><span class="sxs-lookup"><span data-stu-id="b3579-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="b3579-124">**Auf der swpm- \_ Ebene \_ IPSec \_ V {4 \| 6} Setup-und EM-Aushandlungs Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="b3579-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="b3579-125">Fügen Sie einen oder beide der folgenden Einstellungen für den Transportmodus-Richtlinien Anbieter hinzu, und legen Sie die [**IPSec-Richtlinienflag \_ \_ \_ nd \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) fest.</span><span class="sxs-lookup"><span data-stu-id="b3579-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="b3579-126">Für IKE ein Richtlinien Anbieter Kontext vom Typ " **WPM- \_ IPSec- \_ IKE- \_ Quadrat- \_ Transport \_ Kontext**".</span><span class="sxs-lookup"><span data-stu-id="b3579-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="b3579-127">Für AuthIP ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ AuthIP \_ qm \_ Transport \_ context**".</span><span class="sxs-lookup"><span data-stu-id="b3579-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="b3579-128">Dieser Kontext kann optional die Richtlinie "AuthIP Extended Mode" (EM) aushandeln enthalten.</span><span class="sxs-lookup"><span data-stu-id="b3579-128">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="b3579-129">Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende hoch Richtlinie wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="b3579-129">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="b3579-130">AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b3579-130">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="b3579-131">Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3579-131">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="b3579-132">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b3579-132">Filter property</span></span>        | <span data-ttu-id="b3579-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b3579-133">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="b3579-134">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="b3579-134">Filtering conditions</span></span>   | <span data-ttu-id="b3579-135">Leer.</span><span class="sxs-lookup"><span data-stu-id="b3579-135">Empty.</span></span> <span data-ttu-id="b3579-136">Der gesamte Datenverkehr entspricht dem Filter.</span><span class="sxs-lookup"><span data-stu-id="b3579-136">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="b3579-137">**providercontextkey**</span><span class="sxs-lookup"><span data-stu-id="b3579-137">**providerContextKey**</span></span> | <span data-ttu-id="b3579-138">GUID des in Schritt 1 hinzugefügten ESDS-Anbieter Kontexts.</span><span class="sxs-lookup"><span data-stu-id="b3579-138">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="b3579-139">**Auf der swpm- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6} einrichten eingehender Filterregeln pro Paket**</span><span class="sxs-lookup"><span data-stu-id="b3579-139">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="b3579-140">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3579-140">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="b3579-141">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b3579-141">Filter property</span></span>                                               | <span data-ttu-id="b3579-142">Wert</span><span class="sxs-lookup"><span data-stu-id="b3579-142">Value</span></span>                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="b3579-143">Bedingung zum \_ Filtern von \_ lokalen IP- \_ \_ Adress \_ Typen für die Bedingung</span><span class="sxs-lookup"><span data-stu-id="b3579-143">FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE filtering condition</span></span> | [<span data-ttu-id="b3579-144">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="b3579-144">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="b3579-145">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="b3579-145">**action.type**</span></span>                                               | <span data-ttu-id="b3579-146">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3579-146">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="b3579-147">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="b3579-147">**action.calloutKey**</span></span>                                         | <span data-ttu-id="b3579-148">**Swpm-Legende \_ \_ IPSec- \_ Eingangs \_ Transport \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="b3579-148">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="b3579-149">**rawcontext**</span><span class="sxs-lookup"><span data-stu-id="b3579-149">**rawContext**</span></span>                                                | [<span data-ttu-id="b3579-150">**swpm-Kontext-IPSec-eingehende Beibehaltung der \_ \_ \_ \_ \_ Verbindungs \_ Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="b3579-150">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="b3579-151">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b3579-151">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="b3579-152">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b3579-152">Filter property</span></span>                                                   | <span data-ttu-id="b3579-153">Wert</span><span class="sxs-lookup"><span data-stu-id="b3579-153">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="b3579-154">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="b3579-154">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b3579-155">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="b3579-155">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="b3579-156">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="b3579-156">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="b3579-157">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="b3579-157">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="b3579-158">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="b3579-158">**action.type**</span></span>                                                   | <span data-ttu-id="b3579-159">**f/a- \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="b3579-159">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="b3579-160">**weight**</span><span class="sxs-lookup"><span data-stu-id="b3579-160">**weight**</span></span>                                                        | [<span data-ttu-id="b3579-161">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3579-161">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="b3579-162">**Bei der WPM- \_ Schicht \_ ausgehende \_ Transport \_ V {4 \| 6} Einrichten von ausgehenden Regeln pro Paket Filtern**</span><span class="sxs-lookup"><span data-stu-id="b3579-162">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="b3579-163">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3579-163">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="b3579-164">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b3579-164">Filter property</span></span>                                                   | <span data-ttu-id="b3579-165">Wert</span><span class="sxs-lookup"><span data-stu-id="b3579-165">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="b3579-166">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="b3579-166">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b3579-167">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="b3579-167">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="b3579-168">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="b3579-168">**action.type**</span></span>                                                   | <span data-ttu-id="b3579-169">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3579-169">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="b3579-170">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="b3579-170">**action.calloutKey**</span></span>                                             | <span data-ttu-id="b3579-171">**WPM-Legende \_ \_ IPSec- \_ ausgehenden \_ Transport \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="b3579-171">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="b3579-172">**rawcontext**</span><span class="sxs-lookup"><span data-stu-id="b3579-172">**rawContext**</span></span>                                                    | [<span data-ttu-id="b3579-173">**WPM- \_ Kontext- \_ IPSec \_ ausgehende \_ Aushandlungs Aushandlung \_ ermitteln**</span><span class="sxs-lookup"><span data-stu-id="b3579-173">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="b3579-174">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b3579-174">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="b3579-175">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b3579-175">Filter property</span></span>                                                   | <span data-ttu-id="b3579-176">Wert</span><span class="sxs-lookup"><span data-stu-id="b3579-176">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="b3579-177">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="b3579-177">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b3579-178">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="b3579-178">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="b3579-179">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="b3579-179">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="b3579-180">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="b3579-180">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="b3579-181">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="b3579-181">**action.type**</span></span>                                                   | <span data-ttu-id="b3579-182">**f/a- \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="b3579-182">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="b3579-183">**weight**</span><span class="sxs-lookup"><span data-stu-id="b3579-183">**weight**</span></span>                                                        | <span data-ttu-id="b3579-184">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3579-184">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="b3579-185">**Auf dem swpm-Schicht-e/a-Abbild \_ \_ \_ \_ \_ akzeptieren \_ V {4 \| 6} eingehende Filterregeln für eingehende Verbindungen pro Verbindung**</span><span class="sxs-lookup"><span data-stu-id="b3579-185">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="b3579-186">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3579-186">Add a filter with the following properties.</span></span> <span data-ttu-id="b3579-187">Dieser Filter lässt nur eingehende Verbindungsversuche zu, wenn Sie durch IPSec gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="b3579-187">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="b3579-188">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b3579-188">Filter property</span></span>                                                   | <span data-ttu-id="b3579-189">Wert</span><span class="sxs-lookup"><span data-stu-id="b3579-189">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="b3579-190">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="b3579-190">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b3579-191">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="b3579-191">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="b3579-192">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="b3579-192">**action.type**</span></span>                                                   | <span data-ttu-id="b3579-193">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3579-193">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="b3579-194">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="b3579-194">**action.calloutKey**</span></span>                                             | <span data-ttu-id="b3579-195">**WPM-Legende \_ \_ IPSec \_ eingehende \_ Initiierung \_ Secure \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="b3579-195">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="b3579-196">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b3579-196">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="b3579-197">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b3579-197">Filter property</span></span>                                                   | <span data-ttu-id="b3579-198">Wert</span><span class="sxs-lookup"><span data-stu-id="b3579-198">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="b3579-199">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="b3579-199">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b3579-200">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="b3579-200">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="b3579-201">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="b3579-201">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="b3579-202">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="b3579-202">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="b3579-203">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="b3579-203">**action.type**</span></span>                                                   | <span data-ttu-id="b3579-204">**f/a- \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="b3579-204">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="b3579-205">**weight**</span><span class="sxs-lookup"><span data-stu-id="b3579-205">**weight**</span></span>                                                        | <span data-ttu-id="b3579-206">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3579-206">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="b3579-207">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3579-207">Add a filter with the following properties.</span></span> <span data-ttu-id="b3579-208">Dieser Filter lässt nur eingehende Verbindungen mit dem TCP-Port 5555 zu, wenn Sie verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="b3579-208">This filter will only permit inbound connections to TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="b3579-209">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b3579-209">Filter property</span></span>                                                   | <span data-ttu-id="b3579-210">Wert</span><span class="sxs-lookup"><span data-stu-id="b3579-210">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="b3579-211">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="b3579-211">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b3579-212">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="b3579-212">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="b3579-213">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="b3579-213">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="b3579-214">**Ipproto \_ TCP**: diese Konstante ist in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="b3579-214">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="b3579-215">"F" **\_ Bedingung für die \_ \_ lokale \_ Port** Filterung der Bedingung</span><span class="sxs-lookup"><span data-stu-id="b3579-215">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="b3579-216">5555</span><span class="sxs-lookup"><span data-stu-id="b3579-216">5555</span></span>                                                                                                  |
    | <span data-ttu-id="b3579-217">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="b3579-217">**action.type**</span></span>                                                   | <span data-ttu-id="b3579-218">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3579-218">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="b3579-219">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="b3579-219">**action.calloutKey**</span></span>                                             | <span data-ttu-id="b3579-220">**WPM-Legende \_ \_ IPSec \_ eingehende \_ Initiierung \_ Secure \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="b3579-220">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>                                          |
    | <span data-ttu-id="b3579-221">**rawcontext**</span><span class="sxs-lookup"><span data-stu-id="b3579-221">**rawContext**</span></span>                                                    | [<span data-ttu-id="b3579-222">**WPM-Kontext-o- \_ \_ Set- \_ \_ Verbindung \_ erfordert \_ IPSec- \_ Verschlüsselung**</span><span class="sxs-lookup"><span data-stu-id="b3579-222">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

        

<span data-ttu-id="b3579-223">**Bei der Einrichtung der swpm- \_ Ebene ALE-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6} richten Sie ausgehende Filterregeln pro Verbindung ein.**</span><span class="sxs-lookup"><span data-stu-id="b3579-223">**At FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6} setup outbound per-connection filtering rules**</span></span>

-   <span data-ttu-id="b3579-224">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3579-224">Add a filter with the following properties.</span></span> <span data-ttu-id="b3579-225">Mit diesem Filter werden nur ausgehende Verbindungen von TCP-Port 5555 zugelassen, wenn Sie verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="b3579-225">This filter will only permit outbound connections from TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="b3579-226">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b3579-226">Filter property</span></span>                                                   | <span data-ttu-id="b3579-227">Wert</span><span class="sxs-lookup"><span data-stu-id="b3579-227">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="b3579-228">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="b3579-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b3579-229">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="b3579-229">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="b3579-230">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="b3579-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="b3579-231">**Ipproto \_ TCP**: diese Konstante ist in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="b3579-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="b3579-232">"F" **\_ Bedingung für die \_ \_ lokale \_ Port** Filterung der Bedingung</span><span class="sxs-lookup"><span data-stu-id="b3579-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="b3579-233">5555</span><span class="sxs-lookup"><span data-stu-id="b3579-233">5555</span></span>                                                                                                  |
    | <span data-ttu-id="b3579-234">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="b3579-234">**action.type**</span></span>                                                   | <span data-ttu-id="b3579-235">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3579-235">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="b3579-236">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="b3579-236">**action.calloutKey**</span></span>                                             | <span data-ttu-id="b3579-237">**WPM-Legende \_ \_ IPSec- \_ ALE \_ Connect \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="b3579-237">**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V{4\|6}**</span></span>                                                       |
    | <span data-ttu-id="b3579-238">**rawcontext**</span><span class="sxs-lookup"><span data-stu-id="b3579-238">**rawContext**</span></span>                                                    | [<span data-ttu-id="b3579-239">**WPM-Kontext-o- \_ \_ Set- \_ \_ Verbindung \_ erfordert \_ IPSec- \_ Verschlüsselung**</span><span class="sxs-lookup"><span data-stu-id="b3579-239">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

      

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="b3579-240">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3579-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3579-241">Beispielcode: Verwenden des Transport Modus</span><span class="sxs-lookup"><span data-stu-id="b3579-241">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="b3579-242">ALE Ebenen</span><span class="sxs-lookup"><span data-stu-id="b3579-242">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="b3579-243">**Integrierte Legenden Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="b3579-243">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="b3579-244">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="b3579-244">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="b3579-245">**Filtern von ebenenbezeichgern**</span><span class="sxs-lookup"><span data-stu-id="b3579-245">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="b3579-246">**\_ACTION0**</span><span class="sxs-lookup"><span data-stu-id="b3579-246">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="b3579-247">**Kontexttyp des WPM- \_ Anbieters \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3579-247">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

