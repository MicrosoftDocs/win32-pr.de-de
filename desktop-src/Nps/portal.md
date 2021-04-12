---
title: Netzwerkrichtlinienserver
description: Der Netzwerk Richtlinien Server (Network Policy Server, NPS) ist die Microsoft-Implementierung eines RADIUS-Servers (Remote Authentication Dial-in User Service) und-Proxys.
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315441"
---
# <a name="network-policy-server"></a><span data-ttu-id="662a2-103">Netzwerkrichtlinienserver</span><span class="sxs-lookup"><span data-stu-id="662a2-103">Network Policy Server</span></span>

## <a name="purpose"></a><span data-ttu-id="662a2-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="662a2-104">Purpose</span></span>

<span data-ttu-id="662a2-105">Der Netzwerk Richtlinien Server (Network Policy Server, NPS) ist die Microsoft-Implementierung eines RADIUS-Servers (Remote Authentication Dial-in User Service) und-Proxys.</span><span class="sxs-lookup"><span data-stu-id="662a2-105">Network Policy Server (NPS) is the Microsoft implementation of a Remote Authentication Dial-in User Service (RADIUS) server and proxy.</span></span> <span data-ttu-id="662a2-106">Es ist der Nachfolger von Internet Authentication Service (IAS).</span><span class="sxs-lookup"><span data-stu-id="662a2-106">It is the successor of Internet Authentication Service (IAS).</span></span>

<span data-ttu-id="662a2-107">Als RADIUS-Server führt NPS Authentifizierung, Autorisierung und Kontoführung für drahtlose, authentifizier Ende Switches sowie RAS-und VPN-Verbindungen (Virtual Private Network) durch.</span><span class="sxs-lookup"><span data-stu-id="662a2-107">As a RADIUS server, NPS performs authentication, authorization, and accounting for wireless, authenticating switch, and remote access dial-up and virtual private network (VPN) connections.</span></span>

<span data-ttu-id="662a2-108">NPS ist auch ein Integritäts Bewertungs Server für den Netzwerk Zugriffsschutz (Network Access Protection, NAP).</span><span class="sxs-lookup"><span data-stu-id="662a2-108">NPS is also a health evaluator server for Network Access Protection (NAP).</span></span> <span data-ttu-id="662a2-109">NPS führt die Authentifizierung und Autorisierung von Netzwerk Verbindungs versuchen durch und wertet basierend auf den konfigurierten System Integritäts Richtlinien die Konformität der Computer Integrität aus und bestimmt, wie der Netzwerk Zugriff oder die Kommunikation eines nicht kompatiblen Computers beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="662a2-109">NPS performs authentication and authorization of network connection attempts and, based on configured system health policies, evaluates computer health compliance and determines how to limit a noncompliant computer's network access or communication.</span></span> <span data-ttu-id="662a2-110">Dies ist ein neues Feature, das nur für NPS spezifisch ist. IAS unterstützt dies nicht.</span><span class="sxs-lookup"><span data-stu-id="662a2-110">This is a new feature specific to NPS only; IAS does not support it.</span></span> <span data-ttu-id="662a2-111">Eine umfassende Liste der Features, die neu in NPS sind, finden Sie unter [Internet Authentifizierungsdienst und Netzwerk Richtlinien Server](internet-authentication-service-vs-network-policy-server.md) .</span><span class="sxs-lookup"><span data-stu-id="662a2-111">See [Internet Authentication Service and Network Policy Server](internet-authentication-service-vs-network-policy-server.md) for a complete list of features new to NPS.</span></span>

<span data-ttu-id="662a2-112">NPS umfasst zwei API-Sätze: NPS Extensions API und SDO (Server Data Objects)-API.</span><span class="sxs-lookup"><span data-stu-id="662a2-112">NPS includes two API sets: NPS Extensions API and Server Data Objects (SDO) API.</span></span> <span data-ttu-id="662a2-113">Die NPS-Erweiterungs-API und die SDO-API werden auch vom Vorgänger von NPS, dem Internet Authentifizierungsdienst, unterstützt.</span><span class="sxs-lookup"><span data-stu-id="662a2-113">Both NPS Extensions API and SDO API are also supported by the precursor of NPS, the Internet Authentication Service.</span></span>

<span data-ttu-id="662a2-114">Die NPS-Erweiterungs-API kann verwendet werden, um die Authentifizierungs-, Autorisierungs-und Buchhaltungsmethoden zu erweitern, die von NPS und früher von IAS angeboten werden</span><span class="sxs-lookup"><span data-stu-id="662a2-114">NPS Extensions API can be used to extend the authentication, authorization, and accounting methods offered by NPS and previously by IAS.</span></span>

<span data-ttu-id="662a2-115">Die Server Data Objects-API kann verwendet werden, um die Netzwerk Richtlinien Konfiguration auf einem Computer zu bearbeiten, auf dem NPS oder IAS ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="662a2-115">Server Data Objects API can be used to manipulate the network policy configuration on a computer that runs NPS or IAS.</span></span>

> [!Note]  
> <span data-ttu-id="662a2-116">Netzwerk Richtlinien in NPS entsprechen den RAS-Richtlinien in IAS.</span><span class="sxs-lookup"><span data-stu-id="662a2-116">Network policies in NPS are equivalent to remote access policies in IAS.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="662a2-117">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="662a2-117">Developer audience</span></span>

<span data-ttu-id="662a2-118">Die NPS-Erweiterungs-API ist für die Verwendung durch Programmierer konzipiert, die C/C++-Entwicklungssoftware verwenden.</span><span class="sxs-lookup"><span data-stu-id="662a2-118">The NPS Extensions API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="662a2-119">Programmierer sollten mit den Netzwerk Konzepten und dem RADIUS-Protokoll vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="662a2-119">Programmers should be familiar with networking concepts and the RADIUS protocol.</span></span> <span data-ttu-id="662a2-120">RADIUS ist in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) und [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="662a2-120">RADIUS is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

<span data-ttu-id="662a2-121">Die Server Data Objects-API ist für die Verwendung durch Programmierer konzipiert, die C/C++ oder Visual Basic Entwicklungssoftware verwenden.</span><span class="sxs-lookup"><span data-stu-id="662a2-121">The Server Data Objects API is designed for use by programmers using C/C++ or Visual Basic development software.</span></span> <span data-ttu-id="662a2-122">Programmierer sollten mit RAS ( [Remote Access Service](/windows/desktop/RRAS/remote-access-request-for-comments) ) und dem RADIUS-Protokoll vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="662a2-122">Programmers should be familiar with [Remote Access Service](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) and the RADIUS protocol.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="662a2-123">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="662a2-123">Run-time requirements</span></span>

<span data-ttu-id="662a2-124">Die NPS-Erweiterungs-API wird auf Windows Server 2008 mit der Installation von Microsoft Commercial Internet Service (MCIS) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="662a2-124">NPS Extensions API is supported on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

<span data-ttu-id="662a2-125">Die Server Data Objects-API wird auf Windows Server 2008 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="662a2-125">Server Data Objects API is supported on Windows Server 2008.</span></span>

<span data-ttu-id="662a2-126">NPS ist unter Windows Server 2008 mit der Installation von Microsoft Commercial Internet Service (MCIS) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="662a2-126">NPS is available on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="662a2-127">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="662a2-127">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="662a2-128">Übersicht</span><span class="sxs-lookup"><span data-stu-id="662a2-128">Overview</span></span>](about-network-policy-server.md)
</dt> <dd>

<span data-ttu-id="662a2-129">Allgemeine Informationen zu RADIUS, IAS und NPS.</span><span class="sxs-lookup"><span data-stu-id="662a2-129">General information regarding RADIUS, IAS, and NPS.</span></span>

</dd> <dt>

[<span data-ttu-id="662a2-130">API für Netzwerk Richtlinien Server-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="662a2-130">Network Policy Server Extensions API</span></span>](ias-extensions.md)
</dt> <dd>

<span data-ttu-id="662a2-131">API zum Implementieren von Erweiterungs-DLLs, die für Authentifizierung, Autorisierung und Kontoführung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="662a2-131">API for implementing extension DLLs used for authentication, authorization, and accounting.</span></span>

</dd> <dt>

[<span data-ttu-id="662a2-132">Server Data Objects-API</span><span class="sxs-lookup"><span data-stu-id="662a2-132">Server Data Objects API</span></span>](server-data-objects.md)
</dt> <dd>

<span data-ttu-id="662a2-133">API zum Verwalten der Netzwerk Richtlinien Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="662a2-133">API for managing the network policy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="662a2-134">SQL-Programmierbarkeit</span><span class="sxs-lookup"><span data-stu-id="662a2-134">SQL Programmability</span></span>](sql-programmability.md)
</dt> <dd>

<span data-ttu-id="662a2-135">Beispiele für gespeicherte Prozeduren, die zum Verwalten der NPS-Protokollierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="662a2-135">Samples of stored procedures used for managing NPS (IAS) logging.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="662a2-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="662a2-136">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="662a2-137">[TechNet: Netzwerk Richtlinien Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="662a2-137">[TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="662a2-138">[TechNet: Internet Authentifizierungsdienst](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="662a2-138">[TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="662a2-139">Netzwerk Zugriffsschutz</span><span class="sxs-lookup"><span data-stu-id="662a2-139">Network Access Protection</span></span>](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 