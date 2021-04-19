---
title: Manuelles SA
description: Mit dem IPSec-Richtlinien Szenario "manuelle Sicherheits Zuordnung (SA)" können Aufrufer die integrierten IPsec-Schlüssel Bindungs Module (IKE und AuthIP) umgehen, indem Sie die IPSec-SAS direkt angeben, um den Netzwerkverkehr zu sichern.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beeef4486e3a07dea2e83d924c2354a3dabca241
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314573"
---
# <a name="manual-sa"></a><span data-ttu-id="05ba0-103">Manuelles SA</span><span class="sxs-lookup"><span data-stu-id="05ba0-103">Manual SA</span></span>

<span data-ttu-id="05ba0-104">Mit dem IPSec-Richtlinien Szenario "manuelle Sicherheits Zuordnung (SA)" können Aufrufer die integrierten IPsec-Schlüssel Bindungs Module (IKE und AuthIP) umgehen, indem Sie die IPSec-SAS direkt angeben, um den Netzwerkverkehr zu sichern.</span><span class="sxs-lookup"><span data-stu-id="05ba0-104">The Manual Security Association (SA) IPsec policy scenario allows callers to bypass the built-in IPsec keying modules (IKE and AuthIP) by directly specifying IPsec SAs to secure any network traffic.</span></span>

<span data-ttu-id="05ba0-105">Ein Beispiel für ein mögliches Manuelles SA-Szenario ist "Hinzufügen eines IPSec-SA-Paars zum Sichern des gesamten unicastdatenverkehrs zwischen IP-Adressen 1.1.1.1 & 2.2.2.2, mit Ausnahme von ICMP, mit IPSec-Transportmodus".</span><span class="sxs-lookup"><span data-stu-id="05ba0-105">An example of a possible Manual SA scenario is "Add an IPsec SA pair to secure all unicast data traffic between IP addresses 1.1.1.1 & 2.2.2.2, except ICMP, using IPsec transport mode."</span></span>

> [!Note]  
> <span data-ttu-id="05ba0-106">Die folgenden Schritte müssen auf beiden Computern ausgeführt werden, auf denen die IP-Adressen entsprechend festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="05ba0-106">The following steps must be executed on both machines with IP addresses appropriately set.</span></span>

 

<span data-ttu-id="05ba0-107">Um dieses Beispielprogramm gesteuert zu implementieren, verwenden Sie die folgende WFP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="05ba0-107">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="05ba0-108">**Auf der swpm- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6} einrichten eingehender Filterregeln pro Paket**</span><span class="sxs-lookup"><span data-stu-id="05ba0-108">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="05ba0-109">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="05ba0-109">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="05ba0-110">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="05ba0-110">Filter property</span></span>                                                   | <span data-ttu-id="05ba0-111">Wert</span><span class="sxs-lookup"><span data-stu-id="05ba0-111">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="05ba0-112">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="05ba0-112">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="05ba0-113">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="05ba0-113">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="05ba0-114">**\_ \_ lokale IP-Adresse der Bedingung für die lokale IP- \_ \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="05ba0-114">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS**</span></span>                           | <span data-ttu-id="05ba0-115">Die entsprechende lokale Adresse (1.1.1.1 oder 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="05ba0-115">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>           |
    | <span data-ttu-id="05ba0-116">**\_ \_ IP-Adresse für die IP- \_ Adresse der Bedingung \_**</span><span class="sxs-lookup"><span data-stu-id="05ba0-116">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS**</span></span>                          | <span data-ttu-id="05ba0-117">Die entsprechende Remote Adresse (1.1.1.1 oder 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="05ba0-117">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>          |
    | <span data-ttu-id="05ba0-118">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="05ba0-118">**action.type**</span></span>                                                   | <span data-ttu-id="05ba0-119">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="05ba0-119">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                         |
    | <span data-ttu-id="05ba0-120">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="05ba0-120">**action.calloutKey**</span></span>                                             | <span data-ttu-id="05ba0-121">**Swpm-Legende \_ \_ IPSec- \_ Eingangs \_ Transport \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="05ba0-121">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>         |

        
2.  <span data-ttu-id="05ba0-122">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="05ba0-122">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="05ba0-123">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="05ba0-123">Filter property</span></span>                                                   | <span data-ttu-id="05ba0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="05ba0-124">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="05ba0-125">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="05ba0-125">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="05ba0-126">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="05ba0-126">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="05ba0-127">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="05ba0-127">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="05ba0-128">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="05ba0-128">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="05ba0-129">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="05ba0-129">**action.type**</span></span>                                                   | <span data-ttu-id="05ba0-130">**f/a- \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="05ba0-130">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="05ba0-131">**weight**</span><span class="sxs-lookup"><span data-stu-id="05ba0-131">**weight**</span></span>                                                        | [<span data-ttu-id="05ba0-132">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="05ba0-132">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="05ba0-133">**Bei der WPM- \_ Schicht \_ ausgehende \_ Transport \_ V {4 \| 6} Einrichten von ausgehenden Regeln pro Paket Filtern**</span><span class="sxs-lookup"><span data-stu-id="05ba0-133">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="05ba0-134">Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="05ba0-134">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="05ba0-135">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="05ba0-135">Filter property</span></span>                                                   | <span data-ttu-id="05ba0-136">Wert</span><span class="sxs-lookup"><span data-stu-id="05ba0-136">Value</span></span>                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | <span data-ttu-id="05ba0-137">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="05ba0-137">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="05ba0-138">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="05ba0-138">NlatUnicast</span></span>                                            |
    | <span data-ttu-id="05ba0-139">"F" **\_ Bedingung für die \_ \_ lokale \_ Adress** Filterung der Bedingung</span><span class="sxs-lookup"><span data-stu-id="05ba0-139">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS** filtering condition</span></span>       | <span data-ttu-id="05ba0-140">Die entsprechende lokale Adresse (1.1.1.1 oder 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="05ba0-140">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>    |
    | <span data-ttu-id="05ba0-141">"F" **\_ Bedingung zum Filtern der Bedingung \_ IP- \_ Remote \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="05ba0-141">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS** filtering condition</span></span>      | <span data-ttu-id="05ba0-142">Die entsprechende Remote Adresse (1.1.1.1 oder 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="05ba0-142">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>   |
    | <span data-ttu-id="05ba0-143">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="05ba0-143">**action.type**</span></span>                                                   | <span data-ttu-id="05ba0-144">**aufrufende f- \_ Aktions Legende \_ \_**</span><span class="sxs-lookup"><span data-stu-id="05ba0-144">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                  |
    | <span data-ttu-id="05ba0-145">**Action. calloutkey**</span><span class="sxs-lookup"><span data-stu-id="05ba0-145">**action.calloutKey**</span></span>                                             | <span data-ttu-id="05ba0-146">**WPM-Legende \_ \_ IPSec- \_ ausgehenden \_ Transport \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="05ba0-146">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="05ba0-147">Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="05ba0-147">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="05ba0-148">Filter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="05ba0-148">Filter property</span></span>                                                   | <span data-ttu-id="05ba0-149">Wert</span><span class="sxs-lookup"><span data-stu-id="05ba0-149">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="05ba0-150">"F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung**</span><span class="sxs-lookup"><span data-stu-id="05ba0-150">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="05ba0-151">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="05ba0-151">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="05ba0-152">"F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung</span><span class="sxs-lookup"><span data-stu-id="05ba0-152">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="05ba0-153">**Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.</span><span class="sxs-lookup"><span data-stu-id="05ba0-153">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="05ba0-154">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="05ba0-154">**action.type**</span></span>                                                   | <span data-ttu-id="05ba0-155">**f/a- \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="05ba0-155">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="05ba0-156">**weight**</span><span class="sxs-lookup"><span data-stu-id="05ba0-156">**weight**</span></span>                                                        | <span data-ttu-id="05ba0-157">**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="05ba0-157">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="05ba0-158">**Einrichten von eingehenden und ausgehenden Sicherheits Zuordnungen**</span><span class="sxs-lookup"><span data-stu-id="05ba0-158">**Setup inbound and outbound security associations**</span></span>

1.  <span data-ttu-id="05ba0-159">Rufen Sie [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)mit dem Parameter *outboundtraffic* auf, der die IP-Adressen as 1.1.1.1 & 2.2.2.2 und **ipsecfilterid** als LUID des oben hinzugefügten IPSec-Legenden Filters der ausgehenden Transportschicht enthält.</span><span class="sxs-lookup"><span data-stu-id="05ba0-159">Call [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), with the *outboundTraffic* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the outbound transport layer IPsec callout filter added above.</span></span>
2.  <span data-ttu-id="05ba0-160">Rufen Sie [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)mit dem *ID* -Parameter auf, der die von [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)zurückgegebene Kontext-ID enthält, und den *getspi* -Parameter mit den IP-Adressen 1.1.1.1 & 2.2.2.2 und **ipsecfilterid** als LUID des oben hinzugefügten IPSec-Legenden Filters der eingehenden Transportschicht.</span><span class="sxs-lookup"><span data-stu-id="05ba0-160">Call [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *getSpi* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the inbound transport layer IPsec callout filter added above.</span></span> <span data-ttu-id="05ba0-161">Der zurückgegebene SPI-Wert ist für die Verwendung als eingehende SA-SPI durch den lokalen Computer und als ausgehende SA-SPI durch den entsprechenden Remote Computer vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="05ba0-161">The returned SPI value is meant to be used as the inbound SA SPI by the local machine and as the outbound SA SPI by the corresponding remote machine.</span></span> <span data-ttu-id="05ba0-162">Beide Computer müssen Out-of-Band-Mittel zum Austauschen der SPI-Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="05ba0-162">Both machines must use some out-of-band means to exchange the SPI values.</span></span>
3.  <span data-ttu-id="05ba0-163">Aufrufen von [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)mit dem *ID* -Parameter, der die von [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)zurückgegebene Kontext-ID enthält, und dem *inboundbundle* -Parameter, der die Eigenschaften des eingehenden SA-Bundles beschreibt (z. b. der eingehende SA-SPI, der Transformationstyp, Algorithmustypen, Schlüssel usw.</span><span class="sxs-lookup"><span data-stu-id="05ba0-163">Call [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *inboundBundle* parameter describing the properties of the inbound SA bundle (such as the inbound SA SPI, transform type, algorithm types, keys, etc).</span></span>
4.  <span data-ttu-id="05ba0-164">Aufrufen von [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)mit dem *ID* -Parameter, der die von [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)zurückgegebene Kontext-ID enthält, und dem *outboundbundle* -Parameter, der die Eigenschaften des ausgehenden SA-Pakets beschreibt (z. b. die ausgehende SA-SPI, der Transformationstyp, Algorithmustypen, Schlüssel usw.).</span><span class="sxs-lookup"><span data-stu-id="05ba0-164">Call [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *outboundBundle* parameter describing the properties of the outbound SA bundle (such as the outbound SA SPI, transform type, algorithm types, keys, etc).</span></span>

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="05ba0-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05ba0-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05ba0-166">Beispielcode: manuelle SA-Schlüssel Erstellung</span><span class="sxs-lookup"><span data-stu-id="05ba0-166">Sample code: Manual SA Keying</span></span>](manual-sa-keying.md)
</dt> <dt>

[<span data-ttu-id="05ba0-167">**Integrierte Legenden Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="05ba0-167">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="05ba0-168">**Filtern von ebenenbezeichgern**</span><span class="sxs-lookup"><span data-stu-id="05ba0-168">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="05ba0-169">**\_ACTION0**</span><span class="sxs-lookup"><span data-stu-id="05ba0-169">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

