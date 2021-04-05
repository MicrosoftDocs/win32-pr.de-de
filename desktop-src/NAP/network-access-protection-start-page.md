---
title: Netzwerkzugriffsschutz
description: Hinweis die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 Network Access Protection (NAP) nicht mehr verfügbar. es handelt sich um eine Gruppe von Betriebssystemkomponenten, die eine Plattform für den geschützten Zugriff auf private Netzwerke bereitstellen.
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Netzwerkzugriffsschutz
- Netzwerk Zugriffsschutz, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b99348428a867be5bf846fd40b030b844460cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709803"
---
# <a name="network-access-protection"></a><span data-ttu-id="06915-105">Netzwerkzugriffsschutz</span><span class="sxs-lookup"><span data-stu-id="06915-105">Network Access Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="06915-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="06915-106">Purpose</span></span>

> [!Note]  
> <span data-ttu-id="06915-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="06915-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="06915-108">Der Netzwerk Zugriffsschutz (Network Access Protection, NAP) ist ein Satz von Betriebssystemkomponenten, die eine Plattform für den geschützten Zugriff auf private Netzwerke bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="06915-108">Network Access Protection (NAP) is a set of operating system components that provide a platform for protected access to private networks.</span></span> <span data-ttu-id="06915-109">Die NAP-Plattform bietet eine integrierte Möglichkeit, den System Integritäts Status eines Netzwerk Clients auszuwerten, der versucht, eine Verbindung mit einem Netzwerk herzustellen oder in einem Netzwerk zu kommunizieren und den Zugriff auf den Netzwerkclient einzuschränken, bis die Integritäts Richtlinien Anforderungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="06915-109">The NAP platform provides an integrated way of evaluating the system health state of a network client that is attempting to connect to or communicate on a network and restricting the access of the network client until health policy requirements have been met.</span></span>

<span data-ttu-id="06915-110">NAP ist eine erweiterbare Plattform, die eine Infrastruktur und einen API-Satz zum Hinzufügen von Komponenten bereitstellt, die den Systemintegritäts Zustand eines Computers speichern, melden, validieren und korrigieren.</span><span class="sxs-lookup"><span data-stu-id="06915-110">NAP is an extensible platform that provides an infrastructure and an API set for adding components that store, report, validate, and correct a computer's system health state.</span></span> <span data-ttu-id="06915-111">Die NAP-Plattform bietet allein keine Komponenten zum ansammeln und Auswerten von Attributen für den Integritäts Zustand eines Computers.</span><span class="sxs-lookup"><span data-stu-id="06915-111">By itself, the NAP platform does not provide components to accumulate and evaluate attributes of a computer's health state.</span></span> <span data-ttu-id="06915-112">Andere Komponenten, die als Systemintegritäts-Agents (SHAs) und System Integritätsprüfungen (SHVs) bezeichnet werden, stellen die Überprüfung der Netzwerk Richtlinie und die Konformität der Netzwerk Richtlinie bereit.</span><span class="sxs-lookup"><span data-stu-id="06915-112">Other components, known as system health agents (SHAs) and system health validators (SHVs), provide network policy validation and network policy compliance.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="06915-113">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="06915-113">Where applicable</span></span>

<span data-ttu-id="06915-114">NAP ist als erweiterbar konzipiert.</span><span class="sxs-lookup"><span data-stu-id="06915-114">NAP is designed to be extensible.</span></span> <span data-ttu-id="06915-115">Er kann mit sämtlicher Hersteller Software interagieren, die SHAs und SHVs bereitstellt oder den veröffentlichten API-Satz erkennt.</span><span class="sxs-lookup"><span data-stu-id="06915-115">It can interoperate with any vendor software that provides SHAs and SHVs or that recognizes its published API set.</span></span> <span data-ttu-id="06915-116">NAP hilft bei der Bereitstellung einer Lösung für die folgenden gängigen Szenarien:</span><span class="sxs-lookup"><span data-stu-id="06915-116">NAP helps provide a solution for the following common scenarios:</span></span>

-   <span data-ttu-id="06915-117">Überprüfen Sie die Integrität und den Status von Roaminglaptops.</span><span class="sxs-lookup"><span data-stu-id="06915-117">Check the health and status of roaming laptops.</span></span>
-   <span data-ttu-id="06915-118">Stellen Sie sicher, dass die Integrität von Desktop Computern besteht.</span><span class="sxs-lookup"><span data-stu-id="06915-118">Ensure the health of desktop computers.</span></span>
-   <span data-ttu-id="06915-119">Überprüfen Sie die Konformität und Integrität von Computern in Remote Niederlassungen.</span><span class="sxs-lookup"><span data-stu-id="06915-119">Verify the compliance and health of computers in remote offices.</span></span>
-   <span data-ttu-id="06915-120">Ermitteln der Integrität von Laptops.</span><span class="sxs-lookup"><span data-stu-id="06915-120">Determine the health of visiting laptops.</span></span>
-   <span data-ttu-id="06915-121">Überprüfen Sie die Konformität und Integrität nicht verwalteter Heimcomputer.</span><span class="sxs-lookup"><span data-stu-id="06915-121">Verify the compliance and health of unmanaged home computers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="06915-122">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="06915-122">Developer audience</span></span>

<span data-ttu-id="06915-123">Die NAP-API ist für C/C++-Entwickler konzipiert.</span><span class="sxs-lookup"><span data-stu-id="06915-123">The NAP API is designed for C/C++ developers.</span></span> <span data-ttu-id="06915-124">Für die NAP-Erzwingungs Methoden sollten Programmierer mit Netzwerkprotokollen und-Technologien wie z. b. Remote Authentication Dial-in User Service (RADIUS), Dynamic Host Configuration-Protokoll (DHCP), virtuellen privaten Netzwerken (VPNs), dem IEEE 802.1 x-Standard für Kabel-und drahtlos Zugriff und Internet Protokoll Sicherheit (IPSec) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="06915-124">For the NAP enforcement methods, programmers should be familiar with networking protocols and technologies such as Remote Authentication Dial-in User Service (RADIUS), Dynamic Host Configuration Protocol (DHCP), virtual private networks (VPNs), the IEEE 802.1X standard for wired and wireless access, and Internet Protocol security (IPsec).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="06915-125">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="06915-125">Run-time requirements</span></span>

<span data-ttu-id="06915-126">Die NAP-Plattform erfordert NAP-Infrastruktur Server, auf denen Windows Server 2008 oder höher ausgeführt wird, sowie NAP-Clients, auf denen Windows XP mit Service Pack 3 (SP3), Windows Vista oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06915-126">The NAP platform requires NAP infrastructure servers running Windows Server 2008 or later and NAP clients running Windows XP with Service Pack 3 (SP3), Windows Vista, or later operating systems.</span></span> <span data-ttu-id="06915-127">Spezifische Informationen dazu, welche Betriebssysteme ein bestimmtes Programmier Element unterstützen, finden Sie in den Abschnitten zu den Anforderungen der NAP-APIs in der NAP-Referenz Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="06915-127">For specific information about which operating systems support a particular programming element, refer to the Requirements sections of the NAP APIs in the NAP Reference documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="06915-128">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="06915-128">In this section</span></span>



| <span data-ttu-id="06915-129">Thema</span><span class="sxs-lookup"><span data-stu-id="06915-129">Topic</span></span>                                         | <span data-ttu-id="06915-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06915-130">Description</span></span>                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="06915-131">Informationen zu NAP</span><span class="sxs-lookup"><span data-stu-id="06915-131">About NAP</span></span>](about-nap.md)<br/>         | <span data-ttu-id="06915-132">Allgemeine Informationen zur NAP-API.</span><span class="sxs-lookup"><span data-stu-id="06915-132">General information about NAP API.</span></span><br/>                                     |
| [<span data-ttu-id="06915-133">Verwenden von NAP</span><span class="sxs-lookup"><span data-stu-id="06915-133">Using NAP</span></span>](using-nap.md)<br/>         | <span data-ttu-id="06915-134">Verwendungs Beispiele für die NAP-API.</span><span class="sxs-lookup"><span data-stu-id="06915-134">Usage examples for NAP API.</span></span><br/>                                            |
| [<span data-ttu-id="06915-135">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="06915-135">NAP Reference</span></span>](nap-reference.md)<br/> | <span data-ttu-id="06915-136">Dokumentation für NAP-Schnittstellen, Strukturen und andere Code Elemente.</span><span class="sxs-lookup"><span data-stu-id="06915-136">Documentation for NAP interfaces, structures, and other code elements.</span></span><br/> |



 

 

 





