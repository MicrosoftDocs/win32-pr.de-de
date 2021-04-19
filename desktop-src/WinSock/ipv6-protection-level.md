---
description: Die IPv6 \_ - \_ schutzebenensocketoption ermöglicht Entwicklern das Platzieren von Zugriffs Einschränkungen für IPv6-Sockets.
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353065"
---
# <a name="ipv6_protection_level"></a><span data-ttu-id="cf336-103">IPv6- \_ Schutz \_ Ebene</span><span class="sxs-lookup"><span data-stu-id="cf336-103">IPV6\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="cf336-104">Die IPv6 \_ - \_ schutzebenensocketoption ermöglicht Entwicklern das Platzieren von Zugriffs Einschränkungen für IPv6-Sockets.</span><span class="sxs-lookup"><span data-stu-id="cf336-104">The IPV6\_PROTECTION\_LEVEL socket option enables developers to place access restrictions on IPv6 sockets.</span></span> <span data-ttu-id="cf336-105">Mit solchen Einschränkungen kann sich eine im privaten LAN ausgeführte Anwendung selbst einfach und stabil vor externen Angriffen schützen.</span><span class="sxs-lookup"><span data-stu-id="cf336-105">Such restrictions enable an application running on a private LAN to simply and robustly harden itself against external attacks.</span></span> <span data-ttu-id="cf336-106">Die IPv6 \_ - \_ schutzsebene Socketoption erweitert oder schränkt den Bereich eines Abhör Sockets ein, ermöglicht bei Bedarf den uneingeschränkten Zugriff von öffentlichen und privaten Benutzern oder schränkt den Zugriff nur auf denselben Standort ein, je nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="cf336-106">The IPV6\_PROTECTION\_LEVEL socket option widens or narrows the scope of a listening socket, enabling unrestricted access from public and private users when appropriate, or restricting access only to the same site, as required.</span></span>

<span data-ttu-id="cf336-107">Die IPv6- \_ Schutz \_ Ebene verfügt zurzeit über drei definierte Schutz Ebenen.</span><span class="sxs-lookup"><span data-stu-id="cf336-107">IPV6\_PROTECTION\_LEVEL currently has three defined protection levels.</span></span>



| <span data-ttu-id="cf336-108">Schutzebene</span><span class="sxs-lookup"><span data-stu-id="cf336-108">Protection level</span></span>                                                                                                                                 | <span data-ttu-id="cf336-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf336-109">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf336-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>\_uneingeschränkte Schutz Ebene \_</span><span class="sxs-lookup"><span data-stu-id="cf336-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>PROTECTION\_LEVEL\_UNRESTRICTED</span></span><br/>       | <span data-ttu-id="cf336-111">Wird von Anwendungen verwendet, die für den Internet übergreifenden Betrieb entwickelt wurden, einschließlich Anwendungen, die die in Windows integrierten IPv6-NAT-Traversale-Funktionen nutzen (z. b. Teredo).</span><span class="sxs-lookup"><span data-stu-id="cf336-111">Used by applications designed to operate across the Internet, including applications taking advantage of IPv6 NAT traversal capabilities built into Windows (Teredo, for example).</span></span> <span data-ttu-id="cf336-112">Diese Anwendungen können IPv4-Firewalls umgehen und müssen daher vor Internetangriffen auf den geöffneten Anschluss geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="cf336-112">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/> |
| <span data-ttu-id="cf336-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>\_ \_ edgerestrierte Schutz Ebene</span><span class="sxs-lookup"><span data-stu-id="cf336-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>PROTECTION\_LEVEL\_EDGERESTRICTED</span></span><br/> | <span data-ttu-id="cf336-114">Wird von Anwendungen verwendet, die für den Betrieb über das Internet konzipiert sind.</span><span class="sxs-lookup"><span data-stu-id="cf336-114">Used by applications designed to operate across the Internet.</span></span> <span data-ttu-id="cf336-115">Diese Einstellung lässt die NAT-Überquerung nicht zu, da die Teredo-Implementierung von Windows verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf336-115">This setting does not allow NAT traversal using the Windows Teredo implementation.</span></span> <span data-ttu-id="cf336-116">Diese Anwendungen können IPv4-Firewalls umgehen und müssen daher vor Internetangriffen auf den geöffneten Anschluss geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="cf336-116">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/>                                   |
| <span data-ttu-id="cf336-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>Schutz \_ Ebene \_ eingeschränkt</span><span class="sxs-lookup"><span data-stu-id="cf336-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>PROTECTION\_LEVEL\_RESTRICTED</span></span><br/>             | <span data-ttu-id="cf336-118">Wird von Intranetanwendungen verwendet, die keine Internet Szenarios implementieren.</span><span class="sxs-lookup"><span data-stu-id="cf336-118">Used by intranet applications that do not implement Internet scenarios.</span></span> <span data-ttu-id="cf336-119">Diese Anwendungen werden im Allgemeinen nicht getestet oder vor Internetangriffen geschützt.</span><span class="sxs-lookup"><span data-stu-id="cf336-119">These applications are generally not tested or hardened against Internet-style attacks.</span></span><br/> <span data-ttu-id="cf336-120">Diese Einstellung beschränkt den empfangenen Datenverkehr auf linklokalen Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="cf336-120">This setting will limit the received traffic to link-local only.</span></span><br/>                                                                             |



 

<span data-ttu-id="cf336-121">Im folgenden Codebeispiel werden die definierten Werte für die einzelnen Werte bereitstellt:</span><span class="sxs-lookup"><span data-stu-id="cf336-121">The following code example provides the defined values for each:</span></span>

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

<span data-ttu-id="cf336-122">Diese Werte schließen sich gegenseitig aus und können nicht in einem einzelnen [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktions aufzurufen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="cf336-122">These values are mutually exclusive, and cannot be combined in a single [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function call.</span></span> <span data-ttu-id="cf336-123">Andere Werte für diese Socketoption sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="cf336-123">Other values for this socket option are reserved.</span></span> <span data-ttu-id="cf336-124">Diese Schutz Ebenen gelten nur für eingehende Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="cf336-124">These protection levels apply only to incoming connections.</span></span> <span data-ttu-id="cf336-125">Das Festlegen dieser Socketoption hat keine Auswirkung auf ausgehende Pakete oder Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="cf336-125">Setting this socket option has no effect on outbound packets or connections.</span></span>

<span data-ttu-id="cf336-126">Unter Windows 7 und Windows Server 2008 R2 ist der Standardwert für die \_ IPv6 \_ -Schutz Ebene nicht angegeben, und der Standardwert der **Schutz \_ Ebene \_** wird auf-1 festgelegt. Dies ist ein ungültiger Wert für die IPv6- \_ Schutz \_ Ebene.</span><span class="sxs-lookup"><span data-stu-id="cf336-126">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="cf336-127">Unter Windows Vista und Windows Server 2008 ist der Standardwert für die \_ IPv6 \_ -Schutz Ebene die **Schutz \_ Ebene \_ uneingeschränkt** und der Standardwert der **Schutz \_ Ebene \_** wird auf-1 festgelegt, ein unzulässiger Wert für die IPv6- \_ Schutz \_ Ebene.</span><span class="sxs-lookup"><span data-stu-id="cf336-127">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="cf336-128">Unter Windows Server 2003 und Windows XP ist der Standardwert für die \_ IPv6 \_ -Schutz Ebene die **Schutz \_ Ebene \_ edgerestrihiert** , und der **Schutz \_ Grad \_ default** ist als **Schutz \_ Ebene \_ edgerestrihiert** definiert.</span><span class="sxs-lookup"><span data-stu-id="cf336-128">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

> [!Note]  
> <span data-ttu-id="cf336-129">Die IPv6 \_ - \_ schutzsebene-Socketoption sollte festgelegt werden, bevor der Socket gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="cf336-129">The IPV6\_PROTECTION\_LEVEL socket option should be set before the socket is bound.</span></span> <span data-ttu-id="cf336-130">Andernfalls entsprechen Pakete, die zwischen [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -und [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Aufrufen empfangen werden, der **Schutz \_ Ebene \_ edgerestrihiert** und können an die Anwendung übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="cf336-130">Otherwise, packets received between [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) calls will conform to **PROTECTION\_LEVEL\_EDGERESTRICTED**, and may be delivered to the application.</span></span>

 

<span data-ttu-id="cf336-131">In der folgenden Tabelle werden die Auswirkungen der Anwendung der einzelnen Schutz Ebenen auf einen Abhör Socket beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cf336-131">The following table describes the effect of applying each protection level to a listening socket.</span></span>

<span data-ttu-id="cf336-132">Schutzebene</span><span class="sxs-lookup"><span data-stu-id="cf336-132">Protection level</span></span>

<span data-ttu-id="cf336-133">Eingehender Datenverkehr zulässig</span><span class="sxs-lookup"><span data-stu-id="cf336-133">Incoming traffic permitted</span></span>

<span data-ttu-id="cf336-134">Gleiche Website</span><span class="sxs-lookup"><span data-stu-id="cf336-134">Same site</span></span>

<span data-ttu-id="cf336-135">Extern</span><span class="sxs-lookup"><span data-stu-id="cf336-135">External</span></span>

<span data-ttu-id="cf336-136">NAT-Durchlauf (Teredo)</span><span class="sxs-lookup"><span data-stu-id="cf336-136">NAT traversal (Teredo)</span></span>

<span data-ttu-id="cf336-137">Schutz \_ Ebene \_ eingeschränkt</span><span class="sxs-lookup"><span data-stu-id="cf336-137">PROTECTION\_LEVEL\_RESTRICTED</span></span>

<span data-ttu-id="cf336-138">Ja</span><span class="sxs-lookup"><span data-stu-id="cf336-138">Yes</span></span>

<span data-ttu-id="cf336-139">Nein</span><span class="sxs-lookup"><span data-stu-id="cf336-139">No</span></span>

<span data-ttu-id="cf336-140">Nein</span><span class="sxs-lookup"><span data-stu-id="cf336-140">No</span></span>

<span data-ttu-id="cf336-141">\_ \_ edgerestrierte Schutz Ebene</span><span class="sxs-lookup"><span data-stu-id="cf336-141">PROTECTION\_LEVEL\_EDGERESTRICTED</span></span>

<span data-ttu-id="cf336-142">Ja</span><span class="sxs-lookup"><span data-stu-id="cf336-142">Yes</span></span>

<span data-ttu-id="cf336-143">Ja</span><span class="sxs-lookup"><span data-stu-id="cf336-143">Yes</span></span>

<span data-ttu-id="cf336-144">Nein</span><span class="sxs-lookup"><span data-stu-id="cf336-144">No</span></span>

<span data-ttu-id="cf336-145">\_uneingeschränkte Schutz Ebene \_</span><span class="sxs-lookup"><span data-stu-id="cf336-145">PROTECTION\_LEVEL\_UNRESTRICTED</span></span>

<span data-ttu-id="cf336-146">Ja</span><span class="sxs-lookup"><span data-stu-id="cf336-146">Yes</span></span>

<span data-ttu-id="cf336-147">Ja</span><span class="sxs-lookup"><span data-stu-id="cf336-147">Yes</span></span>

<span data-ttu-id="cf336-148">Ja</span><span class="sxs-lookup"><span data-stu-id="cf336-148">Yes</span></span>



 

<span data-ttu-id="cf336-149">In der obigen Tabelle ist die **gleiche Website** Spalte eine Kombination aus folgendem:</span><span class="sxs-lookup"><span data-stu-id="cf336-149">In the table above, the **Same site** column is a combination of the following:</span></span>

-   <span data-ttu-id="cf336-150">Lokale Adressen verknüpfen</span><span class="sxs-lookup"><span data-stu-id="cf336-150">Link local addresses</span></span>
-   <span data-ttu-id="cf336-151">Lokale Standort Adressen</span><span class="sxs-lookup"><span data-stu-id="cf336-151">Site Local addresses</span></span>
-   <span data-ttu-id="cf336-152">Globale Adressen, die bekanntermaßen zu demselben Standort gehören (übereinstimmende Präfix Tabelle)</span><span class="sxs-lookup"><span data-stu-id="cf336-152">Global addresses known to belong to the same site (matching the site prefix table)</span></span>

<span data-ttu-id="cf336-153">Unter Windows 7 und Windows Server 2008 R2 ist der Standardwert für die IPv6- \_ Schutz \_ Ebene nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="cf336-153">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified.</span></span> <span data-ttu-id="cf336-154">Wenn auf dem lokalen Computer keine auf der Edgeausnahme kompatible Firewallsoftware installiert ist (die Windows-Firewall ist deaktiviert oder eine andere Firewall installiert ist, die Teredo-Datenverkehr ignoriert), empfangen Sie Teredo-Datenverkehr nur, wenn Sie die IPv6- \_ \_ schutzebenensocketoption auf die **Schutz \_ Ebene " \_ uneingeschränkt**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="cf336-154">If there is no edge-traversal aware firewall software installed on the local computer (Windows firewall is disabled or some other firewall is installed that ignores Teredo traffic), you will receive Teredo traffic only if you set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="cf336-155">Die Windows-Firewall oder eine beliebige Edge-Traversal-fähige Firewall-Richtlinie kann diese Option jedoch aufgrund der Richtlinien Einstellungen für die Firewall ignorieren.</span><span class="sxs-lookup"><span data-stu-id="cf336-155">However, Windows firewall or any edge-traversal aware firewall policy may ignore this option based on policy settings for the firewall.</span></span> <span data-ttu-id="cf336-156">Wenn Sie diese Socketoption auf die **Schutz \_ Ebene \_ uneingeschränkt** festlegen, kommuniziert die Anwendung mit ihrer expliziten Absicht, von der auf dem lokalen Computer installierten Host Firewall den von Edge durchsuchten Datenverkehr zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="cf336-156">By setting this socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, the application is communicating its explicit intent to receive edge traversed traffic by the host firewall installed on the local machine.</span></span> <span data-ttu-id="cf336-157">Wenn also eine Host Firewall installiert ist, die auf Edgeausnahme basiert, wird die endgültige Entscheidung getroffen, ein Paket zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="cf336-157">So if there is an edge-traversal aware host firewall installed, it will have the final decision on accepting a packet.</span></span> <span data-ttu-id="cf336-158">Standardmäßig ohne festgelegte Socketoption:</span><span class="sxs-lookup"><span data-stu-id="cf336-158">By default, without any socket option set:</span></span>

-   <span data-ttu-id="cf336-159">o Wenn die Windows-Firewall aktiviert ist (oder eine andere Edgeausnahme unterstützende Host Firewall installiert ist), wird auf dem lokalen Computer das beliebige, was Sie erzwingt, beobachtet.</span><span class="sxs-lookup"><span data-stu-id="cf336-159">o If Windows firewall is enabled (or another edge-traversal aware host firewall is installed) on the local computer, whatever it enforces will be observed.</span></span> <span data-ttu-id="cf336-160">Die typische Edge-Traversal-fähige Host Firewall blockiert standardmäßig Teredo-Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="cf336-160">Typical edge-traversal aware host firewall will block Teredo traffic by default.</span></span> <span data-ttu-id="cf336-161">Daher beobachten Anwendungen den Standard, als ob es sich um eine **\_ \_ edgerestrierte Schutz Ebene** handelt.</span><span class="sxs-lookup"><span data-stu-id="cf336-161">Therefore applications will observe the default as if it was **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>
-   <span data-ttu-id="cf336-162">o Wenn die Windows-Firewall nicht aktiviert ist und keine andere auf dem lokalen System unterstützende Host Firewall installiert ist, wird standardmäßig die **Schutz \_ Ebene \_ edgerestrihiert**.</span><span class="sxs-lookup"><span data-stu-id="cf336-162">o If Windows firewall is not enabled and no other edge-traversal aware host firewall is installed on the local system, the default will be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

<span data-ttu-id="cf336-163">Unter Windows Vista und Windows Server 2008 ist der Standardwert für die IPv6- \_ Schutz \_ Ebene die **Schutz \_ Ebene \_ uneingeschränkt**.</span><span class="sxs-lookup"><span data-stu-id="cf336-163">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="cf336-164">Der effektive Wert hängt jedoch davon ab, ob die Windows-Firewall aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cf336-164">But the effective value depends on whether Windows firewall is enabled.</span></span> <span data-ttu-id="cf336-165">Die Windows-Firewall ist Edge-Traversal-fähig (Teredo-fähig), unabhängig davon, welcher Wert für die IPv6-Schutz Ebene festgelegt ist, \_ \_ und ignoriert, ob die IPv6- \_ Schutz \_ Ebene **\_ \_ uneingeschränkt geschützt** ist.</span><span class="sxs-lookup"><span data-stu-id="cf336-165">The Windows firewall is edge-traversal aware (Teredo aware), no matter what value is set for the IPV6\_PROTECTION\_LEVEL and ignores if IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="cf336-166">Der effektive Wert hängt also von der Firewallrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="cf336-166">So the effective value depends on the firewall policy.</span></span> <span data-ttu-id="cf336-167">Wenn die Windows-Firewall deaktiviert ist und keine andere auf dem lokalen Computer unterstützende Firewall installiert ist, lautet der Standardwert für die IPv6- \_ Schutz \_ Ebene **\_ \_ uneingeschränkt**.</span><span class="sxs-lookup"><span data-stu-id="cf336-167">When Windows firewall is disabled and no other edge-traversal aware firewall is installed on the local computer, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

<span data-ttu-id="cf336-168">Unter Windows Server 2003 und Windows XP lautet der Standardwert für die IPv6- \_ Schutz \_ Ebene die **Schutz \_ Ebene \_ edgerestrihiert**.</span><span class="sxs-lookup"><span data-stu-id="cf336-168">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span> <span data-ttu-id="cf336-169">Sie erhalten keinen Teredo-Datenverkehr, es sei denn, Sie haben die IPv6- \_ \_ Option "socketschutzstufe" auf "nicht **\_ \_** eingeschränkt" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf336-169">Unless you have set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, you would not receive any Teredo traffic.</span></span>

<span data-ttu-id="cf336-170">Abhängig von der IPv6- \_ Schutz \_ Ebene kann eine Anwendung, die nicht angeforderten Datenverkehr aus dem Internet benötigt, möglicherweise nicht angeforderten Datenverkehr empfangen.</span><span class="sxs-lookup"><span data-stu-id="cf336-170">Depending on the IPV6\_PROTECTION\_LEVEL, an application that requires unsolicited traffic from the Internet may not be capable of receiving unsolicited traffic.</span></span> <span data-ttu-id="cf336-171">Diese Anforderungen sind jedoch nicht erforderlich, um angeforderten Datenverkehr über die Teredo-Schnittstelle von Windows zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="cf336-171">However, these requirements are not necessary for receiving solicited traffic over the Windows Teredo interface.</span></span> <span data-ttu-id="cf336-172">Weitere Informationen zur Interaktion mit Teredo finden Sie unter [empfangen von angeforderten Datenverkehr über Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span><span class="sxs-lookup"><span data-stu-id="cf336-172">For more details on the interaction with Teredo, see [Receiving Solicited Traffic Over Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="cf336-173">Wenn eingehende Pakete oder Verbindungen aufgrund der festgelegten Schutz Ebene abgelehnt werden, wird die Ablehnung so behandelt, als ob keine Anwendung an diesem Socket lauscht.</span><span class="sxs-lookup"><span data-stu-id="cf336-173">When incoming packets or connections are refused due to the set protection level, rejection is handled as if no application was listening on that socket.</span></span>

> [!Note]
>
> <span data-ttu-id="cf336-174">Die IPv6 \_ - \_ schutzsetobjekt-Option fügt nicht notwendigerweise Zugriffs Einschränkungen für IPv6-Sockets ein oder schränkt die NAT-Überquerung mit einer anderen Methode als Windows Teredo oder sogar mit einer anderen Implementierung von Teredo durch einen anderen Anbieter ein.</span><span class="sxs-lookup"><span data-stu-id="cf336-174">The IPV6\_PROTECTION\_LEVEL socket option does not necessarily place access restrictions on IPv6 sockets or restrict NAT traversal using some method other than Windows Teredo or even using another implementation of Teredo by another vendor.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cf336-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cf336-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf336-176">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="cf336-176">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="cf336-177">Empfangen von angeforderten Datenverkehr über Teredo</span><span class="sxs-lookup"><span data-stu-id="cf336-177">Receiving Solicited Traffic Over Teredo</span></span>](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[<span data-ttu-id="cf336-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="cf336-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
