---
title: Informationen zu DNS
description: Domain Name System (DNS) ist ein Industriestandard Protokoll, das zum Auffinden von Computern in einem IP-basierten Netzwerk verwendet wird. Benutzer können anzeigen Amen wie z. b. www.Microsoft.com einfacher als Zahlen basierte Adressen, z. b. 207.46.131.137, merken.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Informationen zu Domain Name System DNS
- Domain Name System DNS, Informationen zu
- Domain Name System DNS, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104219406"
---
# <a name="about-dns"></a><span data-ttu-id="28d41-107">Informationen zu DNS</span><span class="sxs-lookup"><span data-stu-id="28d41-107">About DNS</span></span>

<span data-ttu-id="28d41-108">Domain Name System (DNS) ist ein Industriestandard Protokoll, das zum Auffinden von Computern in einem IP-basierten Netzwerk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="28d41-108">Domain Name System (DNS) is an industry-standard protocol used to locate computers on an IP-based network.</span></span> <span data-ttu-id="28d41-109">Benutzer können sich anzeigen Amen, wie z `www.microsoft.com` . b. einfacher als Zahlen basierte Adressen, wie z. b. 207.46.131.137, merken.</span><span class="sxs-lookup"><span data-stu-id="28d41-109">Users can remember display names, such as `www.microsoft.com` easier than number-based addresses, such as 207.46.131.137.</span></span>

<span data-ttu-id="28d41-110">IP-Netzwerke, wie z. b. das Internet und Windows-Netzwerke, basieren auf Zahlen basierten Adressen, um Daten im gesamten Netzwerk zu übertragen. Daher ist es notwendig, anzeigen Amen (z `www.microsoft.com` . b.) in numerische Adressen zu übersetzen, die das Netzwerk erkennen kann (z. b. 207.46.131.137).</span><span class="sxs-lookup"><span data-stu-id="28d41-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to transmit data throughout the network; therefore, it is necessary to translate display names (such as `www.microsoft.com`) into numeric addresses that the network can recognize (such as 207.46.131.137).</span></span> <span data-ttu-id="28d41-111">DNS ist der bevorzugte Dienst in Windows, um solche Ressourcen zu suchen und in IP-Adressen zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="28d41-111">DNS is the service of choice in Windows to locate such resources and translate them into IP addresses.</span></span>

<span data-ttu-id="28d41-112">DNS ist der primäre Serverlocatorpunkt-Dienst für Active Directory. Daher kann DNS als Basis Dienst für Windows und Active Directory betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="28d41-112">DNS is the primary locator service for Active Directory, and therefore, DNS can be considered a base service for both Windows and Active Directory.</span></span> <span data-ttu-id="28d41-113">Windows stellt Funktionen bereit, mit denen Anwendungsprogrammierer DNS-Funktionen wie das programmgesteuerte Ausführen von DNS-Abfragen, das Vergleichen von Datensätzen und das Suchen von Namen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="28d41-113">Windows provides functions that enable application programmers to use DNS functions such as programmatically making DNS queries, comparing records, and looking up names.</span></span>

<span data-ttu-id="28d41-114">Viele DNS-Funktionen sind tatsächlich Funktionstypen, da es einen Basisnamen für die Funktion gibt, deren Verwendung jedoch von der Zeichencodierung abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="28d41-114">Many DNS functions are actually function types, in that there is a base name for the function, but its use depends on character encoding.</span></span> <span data-ttu-id="28d41-115">Beispielsweise ist die [**DNSQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) -Funktion in der Funktionsreferenz der DNS-API (Application Programming Interface) als **DNSQuery** aufgeführt. die Verwendung in Anwendungen hängt jedoch davon ab, ob die Zeichencodierung ANSI (durch Anhängen von \_ an den Funktionstyp Namen), Unicode (durch Anhängen von \_ W an den Funktionstyp Namen) oder UTF-8 (durch Anhängen von UTF an den Funktionstyp Namen) oder UTF-8 (festgelegt durch Anhängen von UTF an den Funktionstyp Namen) ist \_ .</span><span class="sxs-lookup"><span data-stu-id="28d41-115">For example, the [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) function is listed in the function reference of the DNS Application Programming Interface (API) as **DnsQuery**, but its use in applications depends on whether the character encoding is ANSI (designated by appending \_A to the function type name), Unicode (designated by appending \_W to the function type name), or UTF-8 (designated by appending \_UTF to the function type name).</span></span> <span data-ttu-id="28d41-116">Daher würde der Funktions Aufrufder **DNSQuery** -Funktion eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="28d41-116">Therefore, the function call for the **DnsQuery** function would actually be one of the following:</span></span>

<span data-ttu-id="28d41-117">DNSQuery \_ A ( \_ a für ANSI-Codierung)</span><span class="sxs-lookup"><span data-stu-id="28d41-117">DnsQuery\_A (\_A for ANSI encoding)</span></span>

<span data-ttu-id="28d41-118">DNSQuery \_ w ( \_ w für Unicode-Codierung)</span><span class="sxs-lookup"><span data-stu-id="28d41-118">DnsQuery\_W (\_W for Unicode encoding)</span></span>

<span data-ttu-id="28d41-119">DNSQuery \_ utf8 ( \_ UTF8 für UTF-8-Codierung)</span><span class="sxs-lookup"><span data-stu-id="28d41-119">DnsQuery\_UTF8 (\_UTF8 for UTF-8 encoding)</span></span>

<span data-ttu-id="28d41-120">Alle Funktionen, die diese Konvention erfordern, geben diese Anforderung in den ersten Sätzen ihrer Funktionsdefinition eindeutig an.</span><span class="sxs-lookup"><span data-stu-id="28d41-120">All functions that require this convention clearly state this requirement within the first few sentences of their function definition.</span></span> <span data-ttu-id="28d41-121">Verwenden Sie den richtigen Funktionsnamen; Beispielsweise können Sie nicht einfach [**DNSQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) anstelle von DNSQuery A aufzurufen \_ .</span><span class="sxs-lookup"><span data-stu-id="28d41-121">Use the proper function name; for example, you cannot simply call [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) instead of DnsQuery\_A.</span></span>

 

 




