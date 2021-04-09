---
description: Im folgenden finden Sie eine Schritt-für-Schritt-Anleitung für den Einstieg in die Programmierung mit der IP-Hilfsanwendung (Application Programming Interface, API). Es wurde entwickelt, um ein Verständnis für die grundlegenden IP-Hilfsobjekte und Datenstrukturen und deren Zusammenarbeit zu bieten.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Einführung in das IP-Hilfsprogramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 566ed4503c9bbafaee846aebf30c31993f7ce7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869068"
---
# <a name="getting-started-with-ip-helper"></a><span data-ttu-id="c6077-104">Einführung in das IP-Hilfsprogramm</span><span class="sxs-lookup"><span data-stu-id="c6077-104">Getting Started with IP Helper</span></span>

<span data-ttu-id="c6077-105">Im folgenden finden Sie eine Schritt-für-Schritt-Anleitung für den Einstieg in die Programmierung mit der IP-Hilfsanwendung (Application Programming Interface, API).</span><span class="sxs-lookup"><span data-stu-id="c6077-105">The following is a step-by-step guide to getting started programming using the IP Helper application programming interface (API).</span></span> <span data-ttu-id="c6077-106">Es wurde entwickelt, um ein Verständnis für die grundlegenden IP-Hilfsobjekte und Datenstrukturen und deren Zusammenarbeit zu bieten.</span><span class="sxs-lookup"><span data-stu-id="c6077-106">It is designed to provide an understanding of basic IP Helper functions and data structures, and how they work together.</span></span>

<span data-ttu-id="c6077-107">Die Anwendung, die zur Veranschaulichung verwendet wird, ist eine sehr einfache IP-Hilfsanwendung.</span><span class="sxs-lookup"><span data-stu-id="c6077-107">The application that is used for illustration is a very basic IP Helper application.</span></span> <span data-ttu-id="c6077-108">Erweiterte Codebeispiele sind in den im Microsoft Windows Software Development Kit (SDK) enthaltenen Beispielen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c6077-108">More advanced code examples are included in the samples included with the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="c6077-109">Der erste Schritt ist für die meisten IP-Hilfsanwendungen identisch.</span><span class="sxs-lookup"><span data-stu-id="c6077-109">The first step is the same for most IP Helper applications.</span></span>

-   [<span data-ttu-id="c6077-110">Erstellen einer grundlegenden IP-Hilfsanwendung</span><span class="sxs-lookup"><span data-stu-id="c6077-110">Creating a Basic IP Helper Application</span></span>](creating-a-basic-ip-helper-application.md)

<span data-ttu-id="c6077-111">In den folgenden Abschnitten werden die verbleibenden Schritte zum Erstellen dieser grundlegenden IP-Hilfsanwendung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c6077-111">The following sections describe the remaining steps for creating this basic IP Helper application.</span></span>

-   [<span data-ttu-id="c6077-112">Abrufen von Informationen mithilfe von getnetworkpara Metern</span><span class="sxs-lookup"><span data-stu-id="c6077-112">Retrieving Information Using GetNetworkParams</span></span>](retrieving-information-using-getnetworkparams.md)
-   [<span data-ttu-id="c6077-113">Verwalten von Netzwerkadaptern mithilfe von getadaptersinfo</span><span class="sxs-lookup"><span data-stu-id="c6077-113">Managing Network Adapters Using GetAdaptersInfo</span></span>](managing-network-adapters-using-getadaptersinfo.md)
-   [<span data-ttu-id="c6077-114">Verwalten von Schnittstellen mithilfe von getinterfacetten Info</span><span class="sxs-lookup"><span data-stu-id="c6077-114">Managing Interfaces Using GetInterfaceInfo</span></span>](managing-interfaces-using-getinterfaceinfo.md)
-   [<span data-ttu-id="c6077-115">Verwalten von IP-Adressen mit getipaddrtable</span><span class="sxs-lookup"><span data-stu-id="c6077-115">Managing IP Addresses Using GetIpAddrTable</span></span>](managing-ip-addresses-using-getipaddrtable.md)
-   [<span data-ttu-id="c6077-116">Verwalten von DHCP-Leases mithilfe von ipreleaseaddress und iprenewaddress</span><span class="sxs-lookup"><span data-stu-id="c6077-116">Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress</span></span>](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [<span data-ttu-id="c6077-117">Verwalten von IP-Adressen mit addipaddress und deleteipaddress</span><span class="sxs-lookup"><span data-stu-id="c6077-117">Managing IP Addresses Using AddIPAddress and DeleteIPAddress</span></span>](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [<span data-ttu-id="c6077-118">Abrufen von Informationen mithilfe von GetIpStatistics</span><span class="sxs-lookup"><span data-stu-id="c6077-118">Retrieving Information Using GetIpStatistics</span></span>](retrieving-information-using-getipstatistics.md)
-   [<span data-ttu-id="c6077-119">Abrufen von Informationen mithilfe von GetTcpStatistics</span><span class="sxs-lookup"><span data-stu-id="c6077-119">Retrieving Information Using GetTcpStatistics</span></span>](retrieving-information-using-gettcpstatistics.md)

<span data-ttu-id="c6077-120">Der gesamte Quellcode für dieses grundlegende IP-Hilfsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c6077-120">The complete source code for this basic IP Helper example.</span></span>

-   [<span data-ttu-id="c6077-121">Vollständiger IP-hilfsanwendungs-Quellcode</span><span class="sxs-lookup"><span data-stu-id="c6077-121">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a><span data-ttu-id="c6077-122">Erweiterte IP-hilfsprogrammbeispiele</span><span class="sxs-lookup"><span data-stu-id="c6077-122">Advanced IP Helper Samples</span></span>

<span data-ttu-id="c6077-123">Im Microsoft Windows Software Development Kit (SDK) sind mehrere erweiterte IP-hilfsprogrammbeispiele enthalten.</span><span class="sxs-lookup"><span data-stu-id="c6077-123">Several more advanced IP Helper samples are included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c6077-124">In der Standardeinstellung wird der Quellcode des IP-Hilfsskripts von der Windows SDK für Windows 7 im folgenden Verzeichnis installiert:</span><span class="sxs-lookup"><span data-stu-id="c6077-124">By default, the IP Helper sample source code is installed by the Windows SDK released for Windows 7 in the following directory:</span></span>

<span data-ttu-id="c6077-125">*C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Beispiele \\ netds \\ iphelp*</span><span class="sxs-lookup"><span data-stu-id="c6077-125">*C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\IPHelp*</span></span>

<span data-ttu-id="c6077-126">Die erweiterten unten aufgeführten Beispiele befinden sich in den folgenden Verzeichnissen:</span><span class="sxs-lookup"><span data-stu-id="c6077-126">The more advanced samples listed below are found in the following directories:</span></span>

-   <span data-ttu-id="c6077-127">Enablerouter</span><span class="sxs-lookup"><span data-stu-id="c6077-127">EnableRouter</span></span>

    <span data-ttu-id="c6077-128">Dieses Verzeichnis enthält ein Beispiel, das veranschaulicht, wie die IP-Hilfsfunktionen [**enablerouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) und [**unenablerouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) verwendet werden, um die IPv4-Weiterleitung auf dem lokalen Computer zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c6077-128">This directory contains a sample that demonstrates how to use the [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) and [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) IP Helper functions to enable and disable IPv4 forwarding on the local computer.</span></span>

-   <span data-ttu-id="c6077-129">iparamep</span><span class="sxs-lookup"><span data-stu-id="c6077-129">iparp</span></span>

    <span data-ttu-id="c6077-130">Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie die IP-Hilfsfunktionen verwendet werden, um Einträge in der IPv4-ARP-Tabelle auf dem lokalen Computer anzuzeigen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c6077-130">This directory contains a sample program that demonstrates how to use the IP Helper functions to display and manipulate entries in the IPv4 ARP table on the local computer.</span></span>

-   <span data-ttu-id="c6077-131">ipchange</span><span class="sxs-lookup"><span data-stu-id="c6077-131">ipchange</span></span>

    <span data-ttu-id="c6077-132">Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie IP-Hilfsobjekte verwendet werden, um eine IP-Adresse für einen bestimmten Netzwerkadapter auf dem Computerprogramm gesteuert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c6077-132">This directory contains a sample program that demonstrates how to use IP Helper functions to programmatically change an IP address for a specific network adapter on your machine.</span></span> <span data-ttu-id="c6077-133">Dieses Programm veranschaulicht auch, wie vorhandene IP-Konfigurationsinformationen für den Netzwerkadapter abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c6077-133">This program also demonstrates how to retrieve existing network adapter IP configuration information.</span></span>

-   <span data-ttu-id="c6077-134">IPConfig</span><span class="sxs-lookup"><span data-stu-id="c6077-134">IPConfig</span></span>

    <span data-ttu-id="c6077-135">Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie Sie die IPv4-Konfigurationsinformationen Programm gesteuert abrufen, ähnlich wie das IPCONFIG.EXE Hilfsprogramm.</span><span class="sxs-lookup"><span data-stu-id="c6077-135">This directory contains a sample program that demonstrates how to programmatically retrieve IPv4 configuration information similar to the IPCONFIG.EXE utility.</span></span> <span data-ttu-id="c6077-136">Es zeigt, wie die Funktionen [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) und [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6077-136">It demonstrates how to use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) and [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) functions.</span></span> <span data-ttu-id="c6077-137">Beachten Sie, dass die **getadaptersinfo** -Funktion nur IPv4-Informationen abruft.</span><span class="sxs-lookup"><span data-stu-id="c6077-137">Note that the **GetAdaptersInfo** function only retrieves IPv4 information.</span></span>

-   <span data-ttu-id="c6077-138">Iprenew</span><span class="sxs-lookup"><span data-stu-id="c6077-138">IPRenew</span></span>

    <span data-ttu-id="c6077-139">Dieses Verzeichnis enthält ein Beispielprogramm, das die programmgesteuerte Freigabe und Erneuerung von IPv4-Adressen veranschaulicht, die über DHCP abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="c6077-139">This directory contains a sample program that demonstrates how to programmatically release and renew IPv4 addresses obtained through DHCP.</span></span> <span data-ttu-id="c6077-140">Außerdem wird in diesem Programm veranschaulicht, wie vorhandene Konfigurationsinformationen für den Netzwerkadapter abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c6077-140">This program also demonstrates how to retrieve existing network adapter configuration information.</span></span>

-   <span data-ttu-id="c6077-141">Iproute</span><span class="sxs-lookup"><span data-stu-id="c6077-141">IPRoute</span></span>

    <span data-ttu-id="c6077-142">Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie die IP-Hilfsfunktionen verwendet werden, um die IPv4-Routing Tabelle zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c6077-142">This directory contains a sample program that demonstrates how to use the IP Helper functions to manipulate the IPv4 routing table.</span></span>

-   <span data-ttu-id="c6077-143">ipstat</span><span class="sxs-lookup"><span data-stu-id="c6077-143">ipstat</span></span>

    <span data-ttu-id="c6077-144">Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie die IP-Hilfsfunktionen verwendet werden, um IPv4-Verbindungen für ein Protokoll anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c6077-144">This directory contains a sample program that demonstrates how to use the IP Helper functions to show IPv4 connections for a protocol.</span></span> <span data-ttu-id="c6077-145">Standardmäßig werden Statistiken für IP, ICMP, TCP und UDP angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6077-145">By default, statistics are shown for IP, ICMP, TCP and UDP.</span></span>

-   <span data-ttu-id="c6077-146">NetInfo</span><span class="sxs-lookup"><span data-stu-id="c6077-146">Netinfo</span></span>

    <span data-ttu-id="c6077-147">Dieses Verzeichnis enthält ein Beispielprogramm, das die Verwendung der neuen IP-Hilfsobjekte veranschaulicht, die unter Windows Vista und höher eingeführt wurden, um Adress-und Schnittstellen Informationen für IPv4 und IPv6 anzuzeigen bzw. zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c6077-147">This directory contains a sample program that demonstrates how to the use the new IP Helper APIs introduced on Windows Vista and later to display/change address and interface information for IPv4 and IPv6.</span></span>

 

 



