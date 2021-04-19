---
title: Remote Identitäts Autorisierung
description: Das Szenario der IPSec-Richtlinie für die Remote Identitäts Autorisierung erfordert, dass eingehende Verbindungen von einem bestimmten Satz von Remote Sicherheits Prinzipale stammen, die in einer Zugriffs Steuerungs Liste (ACL) der Windows-Sicherheits Beschreibung (SD) angegeben sind.
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57287a0dd9af4686b1a2dab162677912213559a7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314833"
---
# <a name="remote-identity-authorization"></a><span data-ttu-id="4d8a5-103">Remote Identitäts Autorisierung</span><span class="sxs-lookup"><span data-stu-id="4d8a5-103">Remote Identity Authorization</span></span>

<span data-ttu-id="4d8a5-104">Das Szenario der IPSec-Richtlinie für die Remote Identitäts Autorisierung erfordert, dass eingehende Verbindungen von einem bestimmten Satz von Remote Sicherheits Prinzipale stammen, die in einer Zugriffs Steuerungs Liste (ACL) der Windows-Sicherheits Beschreibung (SD) angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-104">The Remote Identity Authorization IPsec policy scenario requires that inbound connections come from a specific set of remote security principals which are specified in a Windows security descriptor (SD) access control list (ACL).</span></span> <span data-ttu-id="4d8a5-105">Wenn die Remote Identität (wie von IPSec festgelegt) nicht mit der Gruppe zulässiger Identitäten identisch ist, wird die Verbindung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-105">If the remote identity (as determined by IPsec) does not match the set of allowed identities, the connection will be dropped.</span></span> <span data-ttu-id="4d8a5-106">Diese Richtlinie muss in Verbindung mit einer der Richtlinien Optionen für den Transportmodus angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="4d8a5-107">Wenn AuthIP aktiviert ist, können zwei Sicherheits Deskriptoren angegeben werden: eine, die dem AuthIP-Hauptmodus entspricht, und die andere, die dem erweiterten AuthIP-Modus entspricht.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-107">If AuthIP is enabled, two security descriptors can be specified, one corresponding to AuthIP main mode, and the other corresponding to AuthIP extended mode.</span></span>

<span data-ttu-id="4d8a5-108">Ein Beispiel für einen möglichen Aushandlungs Ermittlungs-transportmodusszenario ist "Secure all Unicast Data Traffic, mit Ausnahme von ICMP, der IPSec-Transport Modus, die Aushandlung von Aushandlungen aktivieren und den eingehenden Zugriff auf Remote Identitäten beschränken, die gemäß dem IKE/AuthIP-Hauptmodus und dem Sicherheits Deskriptor SD2 (entsprechend dem erweiterten AuthIP-Modus) zulässig sind, gilt für sämtlichen Unicastdatenverkehr, der dem lokalen TCP-Port 5555 entspricht.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-108">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and restrict inbound access to remote identities allowed as per security descriptor SD1 (corresponding to IKE/AuthIP main mode) and security descriptor SD2 (corresponding to AuthIP extended mode), for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="4d8a5-109">Um dieses Beispielprogramm gesteuert zu implementieren, verwenden Sie die folgende WFP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="4d8a5-110">**Auf der swpm- \_ Schicht \_ IKEEXT \_ V {4 \| 6} Einrichten der mm-Aushandlungs Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="4d8a5-111">Fügen Sie einen oder beide der folgenden mm-Richtlinien Anbieter Kontexte hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="4d8a5-112">Für IKE ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ IKE \_ mm \_ context**".</span><span class="sxs-lookup"><span data-stu-id="4d8a5-112">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="4d8a5-113">Für AuthIP ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ AuthIP \_ mm \_ context**".</span><span class="sxs-lookup"><span data-stu-id="4d8a5-113">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="4d8a5-114">Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende mm-Richtlinie wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="4d8a5-115">AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="4d8a5-116">Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="4d8a5-117">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d8a5-117">Filter property</span></span>        | <span data-ttu-id="4d8a5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8a5-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="4d8a5-119">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="4d8a5-119">Filtering conditions</span></span>   | <span data-ttu-id="4d8a5-120">Leer.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-120">Empty.</span></span> <span data-ttu-id="4d8a5-121">Der gesamte Datenverkehr entspricht dem Filter.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="4d8a5-122">**providercontextkey**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-122">**providerContextKey**</span></span> | <span data-ttu-id="4d8a5-123">GUID des in Schritt 1 hinzugefügten mm-Anbieter Kontexts.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="4d8a5-124">**Auf der swpm- \_ Ebene \_ IPSec \_ V {4 \| 6} Setup-und EM-Aushandlungs Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="4d8a5-125">Fügen Sie einen oder beide der folgenden Einstellungen für den Transportmodus-Richtlinien Anbieter hinzu, und legen Sie die [**IPSec-Richtlinienflag \_ \_ \_ nd \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) fest.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="4d8a5-126">Für IKE ein Richtlinien Anbieter Kontext vom Typ " **WPM- \_ IPSec- \_ IKE- \_ Quadrat- \_ Transport \_ Kontext**".</span><span class="sxs-lookup"><span data-stu-id="4d8a5-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="4d8a5-127">Für AuthIP ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ AuthIP \_ qm \_ Transport \_ context** ", der die Richtlinie für die Richtlinie "AuthIP Extended Mode (EM)" enthält.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT** that contains the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="4d8a5-128">Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende hoch Richtlinie wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="4d8a5-129">AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="4d8a5-130">Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="4d8a5-131">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d8a5-131">Filter property</span></span>        | <span data-ttu-id="4d8a5-132">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8a5-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="4d8a5-133">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="4d8a5-133">Filtering conditions</span></span>   | <span data-ttu-id="4d8a5-134">Leer.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-134">Empty.</span></span> <span data-ttu-id="4d8a5-135">Der gesamte Datenverkehr entspricht dem Filter.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="4d8a5-136">**providercontextkey**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-136">**providerContextKey**</span></span> | <span data-ttu-id="4d8a5-137">GUID des in Schritt 1 hinzugefügten ESDS-Anbieter Kontexts.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="4d8a5-138">**Auf der swpm- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6} einrichten eingehender Filterregeln pro Paket**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="4d8a5-139">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="4d8a5-140">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d8a5-140">Filter property</span></span>                                                   | <span data-ttu-id="4d8a5-141">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8a5-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="4d8a5-142">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="4d8a5-143">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="4d8a5-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="4d8a5-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-144">**action.type**</span></span>                                                   | <span data-ttu-id="4d8a5-145">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="4d8a5-146">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="4d8a5-147">**Swpm-Legende \_ \_ IPSec- \_ Eingangs \_ Transport \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="4d8a5-148">**rawcontext**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="4d8a5-149">**swpm-Kontext-IPSec-eingehende Beibehaltung der \_ \_ \_ \_ \_ Verbindungs \_ Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="4d8a5-150">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="4d8a5-151">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d8a5-151">Filter property</span></span>                                                   | <span data-ttu-id="4d8a5-152">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8a5-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="4d8a5-153">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4d8a5-154">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="4d8a5-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="4d8a5-155">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="4d8a5-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="4d8a5-156">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="4d8a5-157">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-157">**action.type**</span></span>                                                   | <span data-ttu-id="4d8a5-158">f/a- \_ Aktion \_ zulassen</span><span class="sxs-lookup"><span data-stu-id="4d8a5-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="4d8a5-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-159">**weight**</span></span>                                                        | [<span data-ttu-id="4d8a5-160">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="4d8a5-161">**Bei der WPM- \_ Schicht \_ ausgehende \_ Transport \_ V {4 \| 6} Einrichten von ausgehenden Regeln pro Paket Filtern**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="4d8a5-162">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-162">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="4d8a5-163">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d8a5-163">Filter property</span></span>                                                   | <span data-ttu-id="4d8a5-164">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8a5-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="4d8a5-165">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4d8a5-166">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="4d8a5-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="4d8a5-167">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-167">**action.type**</span></span>                                                   | <span data-ttu-id="4d8a5-168">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="4d8a5-169">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="4d8a5-170">**WPM-Legende \_ \_ IPSec- \_ ausgehenden \_ Transport \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="4d8a5-171">**rawcontext**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="4d8a5-172">**WPM- \_ Kontext- \_ IPSec \_ ausgehende \_ Aushandlungs Aushandlung \_ ermitteln**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="4d8a5-173">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="4d8a5-174">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d8a5-174">Filter property</span></span>                                                   | <span data-ttu-id="4d8a5-175">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8a5-175">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="4d8a5-176">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4d8a5-177">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="4d8a5-177">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="4d8a5-178">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="4d8a5-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="4d8a5-179">Ipproto \_ ICMP {V6} diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-179">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="4d8a5-180">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-180">**action.type**</span></span>                                                   | <span data-ttu-id="4d8a5-181">**f/a- \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-181">**FWP\_ACTION\_PERMIT**</span></span>                                                |
    | <span data-ttu-id="4d8a5-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-182">**weight**</span></span>                                                        | <span data-ttu-id="4d8a5-183">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                               |

        

<span data-ttu-id="4d8a5-184">**Auf dem swpm-Schicht-e/a-Abbild \_ \_ \_ \_ \_ akzeptieren \_ V {4 \| 6} eingehende Filterregeln für eingehende Verbindungen pro Verbindung**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-184">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="4d8a5-185">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-185">Add a filter with the following properties.</span></span> <span data-ttu-id="4d8a5-186">Dieser Filter lässt nur eingehende Verbindungsversuche zu, wenn Sie durch IPSec gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-186">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="4d8a5-187">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d8a5-187">Filter property</span></span>                                                   | <span data-ttu-id="4d8a5-188">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8a5-188">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="4d8a5-189">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-189">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4d8a5-190">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="4d8a5-190">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="4d8a5-191">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-191">**action.type**</span></span>                                                   | <span data-ttu-id="4d8a5-192">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-192">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="4d8a5-193">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-193">**action.calloutKey**</span></span>                                             | <span data-ttu-id="4d8a5-194">**WPM-Legende \_ \_ IPSec \_ eingehende \_ Initiierung \_ Secure \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-194">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="4d8a5-195">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-195">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="4d8a5-196">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d8a5-196">Filter property</span></span>                                                   | <span data-ttu-id="4d8a5-197">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8a5-197">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="4d8a5-198">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-198">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4d8a5-199">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="4d8a5-199">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="4d8a5-200">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="4d8a5-200">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="4d8a5-201">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-201">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="4d8a5-202">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-202">**action.type**</span></span>                                                   | <span data-ttu-id="4d8a5-203">**f/a- \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-203">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="4d8a5-204">**weight**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-204">**weight**</span></span>                                                        | <span data-ttu-id="4d8a5-205">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-205">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="4d8a5-206">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-206">Add a filter with the following properties.</span></span> <span data-ttu-id="4d8a5-207">Dieser Filter lässt eingehende Verbindungen mit dem TCP-Port 5555 zu, wenn die entsprechenden Remote Identitäten sowohl von SD1 als auch von SD2 zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-207">This filter will permit inbound connections to TCP port 5555 if the corresponding remote identities are allowed by both SD1 and SD2.</span></span> 

    | <span data-ttu-id="4d8a5-208">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d8a5-208">Filter property</span></span>                                                   | <span data-ttu-id="4d8a5-209">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8a5-209">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="4d8a5-210">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-210">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4d8a5-211">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="4d8a5-211">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="4d8a5-212">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="4d8a5-212">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="4d8a5-213">**Ipproto \_ TCP**: diese Konstante ist in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-213">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="4d8a5-214">"F" **\_ Bedingung für die \_ \_ lokale \_ Port** Filterung der Bedingung</span><span class="sxs-lookup"><span data-stu-id="4d8a5-214">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="4d8a5-215">5555</span><span class="sxs-lookup"><span data-stu-id="4d8a5-215">5555</span></span>                                                               |
    | <span data-ttu-id="4d8a5-216">**fwpm-Bedingungs- \_ \_ ID- \_ Remote Computer- \_ \_ ID**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-216">**FWPM\_CONDITION\_ALE\_REMOTE\_MACHINE\_ID**</span></span>                     | <span data-ttu-id="4d8a5-217">SD1</span><span class="sxs-lookup"><span data-stu-id="4d8a5-217">SD1</span></span>                                                                |
    | <span data-ttu-id="4d8a5-218">**\_ \_ \_ Remote \_ Benutzer- \_ ID der swpm-Bedingungs-ALE**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-218">**FWPM\_CONDITION\_ALE\_REMOTE\_USER\_ID**</span></span>                        | <span data-ttu-id="4d8a5-219">SD2</span><span class="sxs-lookup"><span data-stu-id="4d8a5-219">SD2</span></span>                                                                |
    | <span data-ttu-id="4d8a5-220">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-220">**action.type**</span></span>                                                   | <span data-ttu-id="4d8a5-221">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-221">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                              |
    | <span data-ttu-id="4d8a5-222">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-222">**action.calloutKey**</span></span>                                             | <span data-ttu-id="4d8a5-223">**WPM-Legende \_ \_ IPSec \_ eingehende \_ Initiierung \_ Secure \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-223">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>       |

        
4.  <span data-ttu-id="4d8a5-224">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-224">Add a filter with the following properties.</span></span> <span data-ttu-id="4d8a5-225">Dieser Filter blockiert alle anderen eingehenden Verbindungen mit dem TCP-Port 5555, die nicht dem vorherigen Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-225">This filter will block any other inbound connections to TCP port 5555 that did not match the previous filter.</span></span> 

    | <span data-ttu-id="4d8a5-226">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d8a5-226">Filter property</span></span>                                                   | <span data-ttu-id="4d8a5-227">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8a5-227">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="4d8a5-228">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4d8a5-229">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="4d8a5-229">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="4d8a5-230">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="4d8a5-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="4d8a5-231">**Ipproto \_ TCP**: diese Konstante ist in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="4d8a5-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="4d8a5-232">"F" **\_ Bedingung für die \_ \_ lokale \_ Port** Filterung der Bedingung</span><span class="sxs-lookup"><span data-stu-id="4d8a5-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="4d8a5-233">5555</span><span class="sxs-lookup"><span data-stu-id="4d8a5-233">5555</span></span>                                                               |
    | <span data-ttu-id="4d8a5-234">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-234">**action.type**</span></span>                                                   | <span data-ttu-id="4d8a5-235">**f- \_ Aktions \_ Block**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-235">**FWP\_ACTION\_BLOCK**</span></span>                                             |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="4d8a5-236">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d8a5-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d8a5-237">Beispielcode: Verwenden des Transport Modus</span><span class="sxs-lookup"><span data-stu-id="4d8a5-237">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="4d8a5-238">ALE Ebenen</span><span class="sxs-lookup"><span data-stu-id="4d8a5-238">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="4d8a5-239">**Integrierte Legenden Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-239">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="4d8a5-240">Filterbedingungen</span><span class="sxs-lookup"><span data-stu-id="4d8a5-240">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="4d8a5-241">**Filtern von ebenenbezeichgern**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-241">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="4d8a5-242">**\_ACTION0**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-242">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="4d8a5-243">**Kontexttyp des WPM- \_ Anbieters \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d8a5-243">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

