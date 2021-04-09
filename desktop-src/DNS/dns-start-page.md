---
title: Domain Name System (DNS)
description: Domain Name System (DNS), ein Serverlocatorpunkt-Dienst in Microsoft Windows, ist ein Industriestandard Protokoll, mit dem Computer in einem IP-basierten Netzwerk lokalisiert werden.
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- DNS (siehe Domain Name System)
- Domain Name System (DNS)
- Domain Name System, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104050826"
---
# <a name="domain-name-system"></a><span data-ttu-id="c4053-107">Domain Name System (DNS)</span><span class="sxs-lookup"><span data-stu-id="c4053-107">Domain Name System</span></span>

## <a name="purpose"></a><span data-ttu-id="c4053-108">Zweck</span><span class="sxs-lookup"><span data-stu-id="c4053-108">Purpose</span></span>

<span data-ttu-id="c4053-109">Domain Name System (DNS), ein Serverlocatorpunkt-Dienst in Microsoft Windows, ist ein Industriestandard Protokoll, mit dem Computer in einem IP-basierten Netzwerk lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4053-109">Domain Name System (DNS), a locator service in Microsoft Windows, is an industry-standard protocol that locates computers on an IP-based network.</span></span> <span data-ttu-id="c4053-110">IP-Netzwerke, wie z. b. das Internet und Windows-Netzwerke, basieren auf Zahlen basierten Adressen, um Daten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c4053-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to process data.</span></span> <span data-ttu-id="c4053-111">Benutzer können sich jedoch leichter mit Namen Adressen merken, sodass benutzerfreundliche Namen (z. b.) in Adressen übersetzt werden müssen, `www.microsoft.com` die das Netzwerk erkennen kann (z. b. 207.46.131.137).</span><span class="sxs-lookup"><span data-stu-id="c4053-111">Users however, can more easily remember name addresses, so it is necessary to translate user-friendly names (such as `www.microsoft.com`) into addresses that the network can recognize (such as 207.46.131.137).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c4053-112">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="c4053-112">Where applicable</span></span>

<span data-ttu-id="c4053-113">In Windows und Active Directory wird DNS verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4053-113">Windows and Active Directory use DNS.</span></span> <span data-ttu-id="c4053-114">DNS ist der primäre Serverlocatorpunkt-Dienst für das Internet und Active Directory. Daher wird DNS als Basis Dienst für Windows und Active Directory angesehen.</span><span class="sxs-lookup"><span data-stu-id="c4053-114">DNS is the primary locator service for the Internet and Active Directory, and therefore, DNS is considered a base service for Windows and Active Directory.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c4053-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="c4053-115">Developer audience</span></span>

<span data-ttu-id="c4053-116">Windows stellt Funktionen bereit, mit denen Anwendungsprogrammierer DNS verwenden können, wie z. b. programmgesteuerte DNS-Abfragen, Daten Satz Vergleiche und Namenssuche.</span><span class="sxs-lookup"><span data-stu-id="c4053-116">Windows provides functions that enable application programmers to use DNS, such as programmatic DNS query, record compare, and name lookup.</span></span>

<span data-ttu-id="c4053-117">Programmierbare DNS-Komponenten sind für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="c4053-117">Programmable DNS components are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="c4053-118">Vertrautheit mit Netzwerk und DNS ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4053-118">Familiarity with networking and DNS is required.</span></span> <span data-ttu-id="c4053-119">Programmierer sollten mit der IP-Protokoll Suite sowie mit dem DNS-Protokoll und den DNS-Vorgängen vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="c4053-119">Programmers should be familiar with the IP-protocol suite, as well as the DNS protocol and DNS operations.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c4053-120">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="c4053-120">Run-time requirements</span></span>

<span data-ttu-id="c4053-121">DNS wird in allen IP-Netzwerken verwendet, für die ein Internet kompatibler Serverlocatorpunkt-Dienst erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c4053-121">DNS is used on all IP networks that require an Internet-compatible locator service.</span></span> <span data-ttu-id="c4053-122">Allerdings erfordert die DNS-API Windows 2000 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c4053-122">However, the DNS API requires Windows 2000 or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c4053-123">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c4053-123">In this section</span></span>



| <span data-ttu-id="c4053-124">Thema</span><span class="sxs-lookup"><span data-stu-id="c4053-124">Topic</span></span>                                                             | <span data-ttu-id="c4053-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4053-125">Description</span></span>                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4053-126">DNS-Standarddokumente</span><span class="sxs-lookup"><span data-stu-id="c4053-126">DNS Standards Documents</span></span>](dns-standards-documents.md)<br/> | <span data-ttu-id="c4053-127">Links zu öffentlichen DNS-Standarddokumenten.</span><span class="sxs-lookup"><span data-stu-id="c4053-127">Links to public DNS standards documents.</span></span><br/>                                  |
| [<span data-ttu-id="c4053-128">Informationen zu DNS</span><span class="sxs-lookup"><span data-stu-id="c4053-128">About DNS</span></span>](about-dns.md)<br/>                             | <span data-ttu-id="c4053-129">Allgemeine Informationen zu DNS.</span><span class="sxs-lookup"><span data-stu-id="c4053-129">General information about DNS.</span></span><br/>                                            |
| [<span data-ttu-id="c4053-130">DNS-Verweis</span><span class="sxs-lookup"><span data-stu-id="c4053-130">DNS Reference</span></span>](dns-reference.md)<br/>                     | <span data-ttu-id="c4053-131">Referenz Dokumentation für DNS.</span><span class="sxs-lookup"><span data-stu-id="c4053-131">Reference documentation for DNS.</span></span><br/>                                          |
| [<span data-ttu-id="c4053-132">DNS-WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="c4053-132">DNS WMI Provider</span></span>](dns-wmi-provider.md)<br/>               | <span data-ttu-id="c4053-133">Allgemeine Informationen und Referenz Dokumentation für den DNS-WMI-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c4053-133">General information and reference documentation for the DNS WMI provider.</span></span><br/> |
| [<span data-ttu-id="c4053-134">Glossar</span><span class="sxs-lookup"><span data-stu-id="c4053-134">Glossary</span></span>](glossary-gly.md)<br/>                           | <span data-ttu-id="c4053-135">Glossar der DNS-Begriffe und-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="c4053-135">Glossary of DNS terms and definitions.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="c4053-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4053-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4053-137">DHCP</span><span class="sxs-lookup"><span data-stu-id="c4053-137">DHCP</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="c4053-138">Internet Protokoll-Hilfsprogramm</span><span class="sxs-lookup"><span data-stu-id="c4053-138">Internet Protocol Helper</span></span>](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

<span data-ttu-id="c4053-139">[Verzeichnisdienste](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="c4053-139">[Directory Services](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span></span>
</dt> </dl>

 

