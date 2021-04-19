---
title: Windows-Filterplattform
description: Windows Filtering Platform (WFP) ist ein Satz von API-und System Diensten, die eine Plattform zum Erstellen von Netzwerk Filterungs Anwendungen bereitstellen.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Windows-Filterplattform
- Startseite der Windows-Filter Plattform, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106338096"
---
# <a name="windows-filtering-platform"></a><span data-ttu-id="925d7-105">Windows-Filterplattform</span><span class="sxs-lookup"><span data-stu-id="925d7-105">Windows Filtering Platform</span></span>

## <a name="purpose"></a><span data-ttu-id="925d7-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="925d7-106">Purpose</span></span>

<span data-ttu-id="925d7-107">Windows Filtering Platform (WFP) ist ein Satz von API-und System Diensten, die eine Plattform zum Erstellen von Netzwerk Filterungs Anwendungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="925d7-107">Windows Filtering Platform (WFP) is a set of API and system services that provide a platform for creating network filtering applications.</span></span> <span data-ttu-id="925d7-108">Mithilfe der WFP-API können Entwickler Code schreiben, der mit der Paketverarbeitung interagiert, die auf verschiedenen Ebenen im Netzwerkstapel des Betriebssystems erfolgt.</span><span class="sxs-lookup"><span data-stu-id="925d7-108">The WFP API allows developers to write code that interacts with the packet processing that takes place at several layers in the networking stack of the operating system.</span></span> <span data-ttu-id="925d7-109">Netzwerkdaten können gefiltert und auch geändert werden, bevor sie ihr Ziel erreichen.</span><span class="sxs-lookup"><span data-stu-id="925d7-109">Network data can be filtered and also modified before it reaches its destination.</span></span>

<span data-ttu-id="925d7-110">Durch die Bereitstellung einer einfacheren Entwicklungsplattform ist WFP darauf ausgelegt, vorherige Paket Filterungs Technologien wie Transport Driver Interface (TDI)-Filter, Network Driver Interface Specification (NDIS)-Filter und Winsock-Schicht-Dienstanbieter (LSP) zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="925d7-110">By providing a simpler development platform, WFP is designed to replace previous packet filtering technologies such as Transport Driver Interface (TDI) filters, Network Driver Interface Specification (NDIS) filters, and Winsock Layered Service Providers (LSP).</span></span> <span data-ttu-id="925d7-111">Ab Windows Server 2008 und Windows Vista sind der firewallhook und die Filter Hook-Treiber nicht verfügbar. Anwendungen, die diese Treiber verwenden, sollten stattdessen WFP verwenden.</span><span class="sxs-lookup"><span data-stu-id="925d7-111">Starting in Windows Server 2008 and Windows Vista, the firewall hook and the filter hook drivers are not available; applications that were using these drivers should use WFP instead.</span></span>

<span data-ttu-id="925d7-112">Mit der WFP-API können Entwickler Firewalls, Angriffs Erkennungssysteme, Antivirussoftware, Netzwerk Überwachungstools und elterliche Kontrollen implementieren.</span><span class="sxs-lookup"><span data-stu-id="925d7-112">With the WFP API, developers can implement firewalls, intrusion detection systems, antivirus programs, network monitoring tools, and parental controls.</span></span> <span data-ttu-id="925d7-113">WFP ist in integriert und bietet Unterstützung für Firewallfeatures, wie z. b. authentifizierte Kommunikation und dynamische Firewallkonfiguration, basierend auf der Verwendung der Sockets-API (Anwendungs basierte Richtlinie) der Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="925d7-113">WFP integrates with and provides support for firewall features such as authenticated communication and dynamic firewall configuration based on applications' use of sockets API (application-based policy).</span></span> <span data-ttu-id="925d7-114">WFP bietet auch eine Infrastruktur für die IPSec-Richtlinien Verwaltung, Änderungs Benachrichtigungen, Netzwerk Diagnose und Zustands behaftete Filterung.</span><span class="sxs-lookup"><span data-stu-id="925d7-114">WFP also provides infrastructure for IPsec policy management, change notifications, network diagnostics, and stateful filtering.</span></span>

<span data-ttu-id="925d7-115">Die Windows-Filter Plattform ist eine Entwicklungsplattform und keine Firewall selbst.</span><span class="sxs-lookup"><span data-stu-id="925d7-115">Windows Filtering Platform is a development platform and not a firewall itself.</span></span> <span data-ttu-id="925d7-116">Die Firewall-Anwendung, die in Windows Vista, Windows Server 2008 und spätere Betriebssysteme Windows-Firewall mit erweiterter Sicherheit (wfas) integriert ist, wird mithilfe von WFP implementiert.</span><span class="sxs-lookup"><span data-stu-id="925d7-116">The firewall application that is built into Windows Vista, Windows Server 2008, and later operating systems   Windows Firewall with Advanced Security (WFAS)   is implemented using WFP.</span></span> <span data-ttu-id="925d7-117">Aus diesem Grund verwenden Anwendungen, die mit der WFP-API oder der [wfas-API](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) entwickelt wurden, die gängige Filterungs Logik, die in WFP integriert ist.</span><span class="sxs-lookup"><span data-stu-id="925d7-117">Therefore, applications developed with the WFP API or the [WFAS API](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) use the common filtering arbitration logic that is built into WFP.</span></span>

<span data-ttu-id="925d7-118">Die WFP-API besteht aus einer benutzermodusapi und einer kernelmodusapi.</span><span class="sxs-lookup"><span data-stu-id="925d7-118">The WFP API consists of a user-mode API and a kernel-mode API.</span></span> <span data-ttu-id="925d7-119">Dieser Abschnitt enthält eine Übersicht über die gesamte WFP und beschreibt ausführlich nur den benutzermodusbereich der WFP-API.</span><span class="sxs-lookup"><span data-stu-id="925d7-119">This section provides an overview of the entire WFP and describes in detail only the user-mode portion of the WFP API.</span></span> <span data-ttu-id="925d7-120">Eine ausführliche Beschreibung der kernelmoduswfp-API finden Sie in der Online Hilfe zum [Windows-Treiberkit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .</span><span class="sxs-lookup"><span data-stu-id="925d7-120">For a detailed description of the kernel-mode WFP API, see the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) online help.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="925d7-121">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="925d7-121">Developer audience</span></span>

<span data-ttu-id="925d7-122">Die Windows-Filter Plattform-API ist für die Verwendung durch Programmierer mit C/C++-Entwicklungssoftware konzipiert.</span><span class="sxs-lookup"><span data-stu-id="925d7-122">The Windows Filtering Platform API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="925d7-123">Programmierer sollten mit den Netzwerk Konzepten und dem Entwurf von Systemen im Benutzermodus und im Kernel Modus vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="925d7-123">Programmers should be familiar with networking concepts and design of systems using user-mode and kernel-mode components.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="925d7-124">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="925d7-124">Run-time requirements</span></span>

<span data-ttu-id="925d7-125">Die Windows-Filter Plattform wird auf Clients unterstützt, auf denen Windows Vista und höher ausgeführt wird, sowie auf Servern unter Windows Server 2008 und höher.</span><span class="sxs-lookup"><span data-stu-id="925d7-125">The Windows Filtering Platform is supported on clients running Windows Vista and later, and on servers running Windows Server 2008 and later.</span></span> <span data-ttu-id="925d7-126">Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="925d7-126">For information about the run-time requirements for a specific programming element, see the Requirements section of the reference page for that element.</span></span>





 

## <a name="in-this-section"></a><span data-ttu-id="925d7-127">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="925d7-127">In this section</span></span>



| <span data-ttu-id="925d7-128">Thema</span><span class="sxs-lookup"><span data-stu-id="925d7-128">Topic</span></span>                                                                                               | <span data-ttu-id="925d7-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="925d7-129">Description</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="925d7-130">Neues in der Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="925d7-130">What's New in Windows Filtering Platform</span></span>](what-s-new-in-windows-filtering-platform.md)<br/> | <span data-ttu-id="925d7-131">Informationen zu neuen Features und APIs in der Windows-Filter Plattform.</span><span class="sxs-lookup"><span data-stu-id="925d7-131">Information on new features and APIs in Windows Filtering Platform.</span></span><br/>                    |
| [<span data-ttu-id="925d7-132">Informationen zur Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="925d7-132">About Windows Filtering Platform</span></span>](about-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="925d7-133">Eine Übersicht über die Windows-Filter Plattform.</span><span class="sxs-lookup"><span data-stu-id="925d7-133">An overview of Windows Filtering Platform.</span></span><br/>                                             |
| [<span data-ttu-id="925d7-134">Verwenden der Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="925d7-134">Using Windows Filtering Platform</span></span>](using-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="925d7-135">Beispielcode, der die Windows-Filter Plattform-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="925d7-135">Example code using the Windows Filtering Platform API.</span></span> <br/>                                |
| [<span data-ttu-id="925d7-136">API-Referenz zur Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="925d7-136">Windows Filtering Platform API Reference</span></span>](fwp-reference.md)<br/>                            | <span data-ttu-id="925d7-137">Dokumentation für die Funktionen, Strukturen und Konstanten der Windows-Filter Plattform.</span><span class="sxs-lookup"><span data-stu-id="925d7-137">Documentation for the Windows Filtering Platform functions, structures, and constants.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="925d7-138">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="925d7-138">Additional resources</span></span>

<span data-ttu-id="925d7-139">Um Fragen zu stellen und Diskussionen zur Verwendung der WFP-API zu erhalten, besuchen Sie das [Forum Windows-Filter Plattform](https://social.msdn.microsoft.com/forums/wfp/threads/).</span><span class="sxs-lookup"><span data-stu-id="925d7-139">To ask questions and have discussions about using the WFP API, visit the [Windows Filtering Platform Forum](https://social.msdn.microsoft.com/forums/wfp/threads/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="925d7-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="925d7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="925d7-141">Kernelmodusfilter für Windows-Filter Plattform-Entwurfs Handbuch</span><span class="sxs-lookup"><span data-stu-id="925d7-141">Kernel-Mode Windows Filtering Platform API - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="925d7-142">Kernel Modus Windows-Filter Plattform-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="925d7-142">Kernel-Mode Windows Filtering Platform API - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[<span data-ttu-id="925d7-143">Windows-Firewall mit erweiterter Sicherheit</span><span class="sxs-lookup"><span data-stu-id="925d7-143">Windows Firewall with Advanced Security</span></span>](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[<span data-ttu-id="925d7-144">Erweiterbare Hilfsklasse der WFP-Diagnose</span><span class="sxs-lookup"><span data-stu-id="925d7-144">WFP Diagnostics Extensible Helper Class</span></span>](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[<span data-ttu-id="925d7-145">Winsock Secure Socket Extensions</span><span class="sxs-lookup"><span data-stu-id="925d7-145">Winsock Secure Socket Extensions</span></span>](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

