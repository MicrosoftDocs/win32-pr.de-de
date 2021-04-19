---
title: Informationen zur Windows-Filter Plattform
description: Windows Filtering Platform (WFP) ist eine Plattform für die Verarbeitung von Netzwerk Datenverkehr, die die Schnittstellen für das Filtern von Netzwerk Datenverkehr in Windows XP und Windows Server 2003 ersetzen soll
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339485"
---
# <a name="about-windows-filtering-platform"></a><span data-ttu-id="821ce-103">Informationen zur Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="821ce-103">About Windows Filtering Platform</span></span>

<span data-ttu-id="821ce-104">Windows Filtering Platform (WFP) ist eine Plattform für die Verarbeitung von Netzwerk Datenverkehr, die die Schnittstellen für das Filtern von Netzwerk Datenverkehr in Windows XP und Windows Server 2003 ersetzen soll</span><span class="sxs-lookup"><span data-stu-id="821ce-104">Windows Filtering Platform (WFP) is a network traffic processing platform designed to replace the Windows XP and Windows Server 2003 network traffic filtering interfaces.</span></span> <span data-ttu-id="821ce-105">WFP besteht aus einem Satz von Hooks im Netzwerk Stapel und einer Filter-Engine, die die Interaktion von Netzwerk Stapeln koordiniert.</span><span class="sxs-lookup"><span data-stu-id="821ce-105">WFP consists of a set of hooks into the network stack and a filtering engine that coordinates network stack interactions.</span></span>

## <a name="the-wfp-components"></a><span data-ttu-id="821ce-106">Die WFP-Komponenten</span><span class="sxs-lookup"><span data-stu-id="821ce-106">The WFP components</span></span>

### <a name="filter-engine"></a><span data-ttu-id="821ce-107">Filter-Engine</span><span class="sxs-lookup"><span data-stu-id="821ce-107">Filter Engine</span></span>

<span data-ttu-id="821ce-108">Die zentrale Filterinfrastruktur für mehrere Ebenen, die im Kernel Modus und im Benutzermodus gehostet wird und die mehrere Filtermodule im Netzwerk Subsystem Windows XP und Windows Server 2003 ersetzt.</span><span class="sxs-lookup"><span data-stu-id="821ce-108">The core multi-layer filtering infrastructure, hosted in both kernel-mode and user-mode, that replaces the multiple filtering modules in the Windows XP and Windows Server 2003 networking subsystem.</span></span>

-   <span data-ttu-id="821ce-109">Filtert den Netzwerk Datenverkehr auf jeder Ebene im System über alle Datenfelder, die von einem Shim bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="821ce-109">Filters network traffic at any layer in the system over any data fields that a shim can provide.</span></span>
-   <span data-ttu-id="821ce-110">Implementiert die "Callout"-Filter durch Aufrufen von Aufrufen während der Klassifizierung.</span><span class="sxs-lookup"><span data-stu-id="821ce-110">Implements the "Callout" filters by invoking callouts during classification.</span></span>
-   <span data-ttu-id="821ce-111">Gibt Aktionen vom Typ "zulassen" oder "blockieren" für das Shim zurück, von dem es zur Erzwingung aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="821ce-111">Returns "Permit" or "Block" actions to the shim that invoked it for enforcement.</span></span>
-   <span data-ttu-id="821ce-112">Stellt das zwischen Verfahren zwischen verschiedenen Richtlinien Quellen bereit.</span><span class="sxs-lookup"><span data-stu-id="821ce-112">Provides arbitration between different policy sources.</span></span> <span data-ttu-id="821ce-113">Beispielsweise bestimmt die Priorität, wenn eine Anwendung so konfiguriert ist, dass Sie Netzwerk Datenverkehr sichert, aber die lokale Firewall ist so konfiguriert, dass der von der Anwendung gesicherte Datenverkehr verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="821ce-113">For example, determines priority when an application is configured to secure any network traffic related to it, but the local firewall is configured to prevent application secured traffic.</span></span><br/>

### <a name="base-filtering-engine-bfe"></a><span data-ttu-id="821ce-114">Basis Filter-Engine (BFE)</span><span class="sxs-lookup"><span data-stu-id="821ce-114">Base Filtering Engine (BFE)</span></span>

<span data-ttu-id="821ce-115">Ein Dienst, der den Betrieb der Windows-Filter Plattform steuert.</span><span class="sxs-lookup"><span data-stu-id="821ce-115">A service that controls the operation of the Windows Filtering Platform.</span></span> <span data-ttu-id="821ce-116">Sie führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="821ce-116">It performs the following tasks.</span></span>

-   <span data-ttu-id="821ce-117">Akzeptiert Filter und andere Konfigurationseinstellungen für die Plattform.</span><span class="sxs-lookup"><span data-stu-id="821ce-117">Accepts filters and other configuration settings for the platform.</span></span>
-   <span data-ttu-id="821ce-118">Meldet den aktuellen Status des Systems, einschließlich der Statistiken.</span><span class="sxs-lookup"><span data-stu-id="821ce-118">Reports the current state of the system, including statistics.</span></span>
-   <span data-ttu-id="821ce-119">Erzwingt das Sicherheitsmodell für die Annahme der Konfiguration auf der Plattform.</span><span class="sxs-lookup"><span data-stu-id="821ce-119">Enforces the security model for accepting configuration in the platform.</span></span> <span data-ttu-id="821ce-120">Beispielsweise kann ein lokaler Administrator Filter hinzufügen, andere Benutzer können Sie jedoch nur anzeigen.</span><span class="sxs-lookup"><span data-stu-id="821ce-120">For example, a local administrator can add filters but other users can only view them.</span></span><br/>
-   <span data-ttu-id="821ce-121">Die Konfigurationseinstellungen werden auf andere Module im System überfallen.</span><span class="sxs-lookup"><span data-stu-id="821ce-121">Plumbs configuration settings to other modules in the system.</span></span> <span data-ttu-id="821ce-122">IPSec-Aushandlungs Richtlinien werden z. b. in IKE/AuthIP-Schlüssel-/Verschlüsselungsmodulen geleitet. Filter werden an die Filter-Engine gesendet.</span><span class="sxs-lookup"><span data-stu-id="821ce-122">For example, IPsec negotiation polices go to IKE/AuthIP keying modules, filters go to the filter engine.</span></span><br/>

### <a name="shims"></a><span data-ttu-id="821ce-123">Shims</span><span class="sxs-lookup"><span data-stu-id="821ce-123">Shims</span></span>

<span data-ttu-id="821ce-124">Kernelmoduskomponenten, die sich zwischen dem Netzwerk Stapel und der Filter-Engine befinden.</span><span class="sxs-lookup"><span data-stu-id="821ce-124">Kernel-mode components that reside between the Network Stack and the filter engine.</span></span> <span data-ttu-id="821ce-125">Shims treffen die Filter Entscheidung, indem die Filter-Engine klassifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="821ce-125">Shims make the filtering decision by classifying against the filter engine.</span></span> <span data-ttu-id="821ce-126">Im folgenden finden Sie eine Liste der verfügbaren Shims.</span><span class="sxs-lookup"><span data-stu-id="821ce-126">Following is a list of available shims.</span></span>

-   <span data-ttu-id="821ce-127">Anwendungsschicht-Erzwingungs-Shim.</span><span class="sxs-lookup"><span data-stu-id="821ce-127">Application Layer Enforcement (ALE) shim.</span></span>
-   <span data-ttu-id="821ce-128">Das transportebenenmodul-Shim.</span><span class="sxs-lookup"><span data-stu-id="821ce-128">Transport Layer Module shim.</span></span>
-   <span data-ttu-id="821ce-129">Shim des netzwerkebenenmoduls.</span><span class="sxs-lookup"><span data-stu-id="821ce-129">Network Layer Module shim.</span></span>
-   <span data-ttu-id="821ce-130">ICMP-Fehler (Internet Control Message Protocol).</span><span class="sxs-lookup"><span data-stu-id="821ce-130">Internet Control Message Protocol (ICMP) Error shim.</span></span>
-   <span data-ttu-id="821ce-131">Verwerfen Sie das Shim.</span><span class="sxs-lookup"><span data-stu-id="821ce-131">Discard shim.</span></span>
-   <span data-ttu-id="821ce-132">Stream-Shim.</span><span class="sxs-lookup"><span data-stu-id="821ce-132">Stream shim.</span></span>

### <a name="callouts"></a><span data-ttu-id="821ce-133">Aufrufe</span><span class="sxs-lookup"><span data-stu-id="821ce-133">Callouts</span></span>

<span data-ttu-id="821ce-134">Eine Reihe von Funktionen, die von einem Treiber verfügbar gemacht und für spezialisierte Filter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="821ce-134">Set of functions exposed by a driver and used for specialized filtering.</span></span> <span data-ttu-id="821ce-135">Neben den grundlegenden Aktionen "zulassen" und "blockieren" können durch Aufrufe der eingehende und ausgehende Netzwerk Datenverkehr geändert und gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="821ce-135">Besides the basic actions of "Permit" and "Block", callouts can modify and secure inbound and outbound network traffic.</span></span> <span data-ttu-id="821ce-136">Weitere Informationen zu Legenden aufrufen finden Sie im Thema [Windows-Filterungs Plattform-Callout-Treiber](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) in der Dokumentation zum Windows-Treiberkit (WDK).</span><span class="sxs-lookup"><span data-stu-id="821ce-136">See the [Windows Filtering Platform Callout Drivers](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) topic in the Windows Driver Kit (WDK) documentation for more information on callouts.</span></span> <span data-ttu-id="821ce-137">WFP bietet integrierte Legenden, mit denen die folgenden Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="821ce-137">WFP provides built-in callouts that accomplish the following tasks.</span></span><br/>

-   <span data-ttu-id="821ce-138">IPSec-Verarbeitung ausführen.</span><span class="sxs-lookup"><span data-stu-id="821ce-138">Perform IPsec processing.</span></span>
-   <span data-ttu-id="821ce-139">Anpassen des Verhaltens der Zustands behafteten Filterung.</span><span class="sxs-lookup"><span data-stu-id="821ce-139">Adjust stateful filtering behavior.</span></span>
-   <span data-ttu-id="821ce-140">Führt die Filterung im Debugmodus aus (Automatisches Löschen von nicht angeforderten Paketen).</span><span class="sxs-lookup"><span data-stu-id="821ce-140">Perform stealth mode filtering (silent drop of packets that were not requested).</span></span>
-   <span data-ttu-id="821ce-141">Steuern Sie die TCP-Chimney-Abladung.</span><span class="sxs-lookup"><span data-stu-id="821ce-141">Control TCP chimney offload.</span></span>
-   <span data-ttu-id="821ce-142">Interagieren Sie mit dem Teredo-Dienst.</span><span class="sxs-lookup"><span data-stu-id="821ce-142">Interact with the Teredo service.</span></span>

<br/> <span data-ttu-id="821ce-143">Die Filter-Engine ermöglicht das Registrieren von Drittanbieter-Legenden für jede der kernelmodusschichten.</span><span class="sxs-lookup"><span data-stu-id="821ce-143">The filter engine allows third-party callouts to register at each of its kernel-mode layers.</span></span><br/>

### <a name="application-programming-interface"></a><span data-ttu-id="821ce-144">Anwendungsprogrammierschnittstelle</span><span class="sxs-lookup"><span data-stu-id="821ce-144">Application Programming Interface</span></span>

<span data-ttu-id="821ce-145">Eine Reihe von Datentypen und Funktionen, die Entwicklern zur Erstellung und Verwaltung von Netzwerk Filterungs Anwendungen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="821ce-145">A set of data types and functions available to the developers to build and manage network filtering applications.</span></span> <span data-ttu-id="821ce-146">Diese Datentypen und Funktionen sind in mehreren [API-Sätzen](api-sets.md)gruppiert.</span><span class="sxs-lookup"><span data-stu-id="821ce-146">These data types and functions are grouped into multiple [API sets](api-sets.md).</span></span>

## <a name="wfp-features"></a><span data-ttu-id="821ce-147">WFP-Features</span><span class="sxs-lookup"><span data-stu-id="821ce-147">WFP Features</span></span>

-   <span data-ttu-id="821ce-148">Bietet eine Paket Filterungs Infrastruktur, in der unabhängige Softwarehersteller (ISVs) spezialisierte Filtermodule einbinden können.</span><span class="sxs-lookup"><span data-stu-id="821ce-148">Provides a packet filtering infrastructure where independent software vendors (ISVs) can plug-in specialized filtering modules.</span></span>
-   <span data-ttu-id="821ce-149">Funktioniert sowohl mit IPv4 als auch mit IPv6.</span><span class="sxs-lookup"><span data-stu-id="821ce-149">Works with both IPv4 and IPv6.</span></span>
-   <span data-ttu-id="821ce-150">Ermöglicht das Filtern, ändern und erneute Einschleusen von Daten.</span><span class="sxs-lookup"><span data-stu-id="821ce-150">Allows for data filtering, modification, and re-injection.</span></span>
-   <span data-ttu-id="821ce-151">Führt sowohl die Paket-als auch die streamverarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="821ce-151">Performs both packet and stream processing.</span></span>
-   <span data-ttu-id="821ce-152">Ermöglicht das Aktivieren der Paketfilterung pro Anwendung, pro Benutzer und pro Verbindung zusätzlich zur Netzwerkschnittstelle oder pro Port.</span><span class="sxs-lookup"><span data-stu-id="821ce-152">Allows packet filtering to be enabled per application, per user, and per connection in addition to per network interface or per port.</span></span>
-   <span data-ttu-id="821ce-153">Stellt die Systemstart Zeit Sicherheit bereit, bis die Basis Filter-Engine (BFE) gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="821ce-153">Provides boot-time security until Base Filtering Engine (BFE) can start.</span></span>
-   <span data-ttu-id="821ce-154">Aktiviert das Filtern Zustands behafteter Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="821ce-154">Enables stateful connection filtering.</span></span>
-   <span data-ttu-id="821ce-155">Verarbeitet sowohl vorab-als auch Post-verschlüsselte IPSec-verschlüsselte Daten.</span><span class="sxs-lookup"><span data-stu-id="821ce-155">Handles both pre and post IPsec-encrypted data.</span></span>
-   <span data-ttu-id="821ce-156">Ermöglicht die Integration von IPSec-und firewallfilterungs Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="821ce-156">Allows integration of IPsec and firewall filtering policies.</span></span>
-   <span data-ttu-id="821ce-157">Stellt eine Richtlinien Verwaltungsinfrastruktur bereit, um zu bestimmen, wann bestimmte Filter aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="821ce-157">Provides a policy management infrastructure to determine when specific filters should be activated.</span></span> <span data-ttu-id="821ce-158">Dies schließt die unterschiedlichen Anforderungen von mehreren Filtern ein, die von verschiedenen Anbietern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="821ce-158">This includes mediating conflicting requirements from multiple filters provided by different vendors.</span></span>
-   <span data-ttu-id="821ce-159">Behandelt die meisten Pakete zur Neuzuweisung und Zustandsüberwachung.</span><span class="sxs-lookup"><span data-stu-id="821ce-159">Handles most packet reassembly and state tracking.</span></span>
-   <span data-ttu-id="821ce-160">Enthält ein generisches Benutzer Benachrichtigungssystem, das Abonnenten über Änderungen am Filtersystem informiert.</span><span class="sxs-lookup"><span data-stu-id="821ce-160">Includes a generic user notification system that informs subscribers of changes to the filtering system.</span></span>
-   <span data-ttu-id="821ce-161">Implementiert Enumerationsfunktionen, die den Status des Systems melden.</span><span class="sxs-lookup"><span data-stu-id="821ce-161">Implements enumeration functions that report on the state of the system.</span></span>
-   <span data-ttu-id="821ce-162">Verwendet Net-Ereignisse, um IPsec-Fehler und Paket Abstürze aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="821ce-162">Uses net events to record IPsec errors and packet drops.</span></span>
-   <span data-ttu-id="821ce-163">Unterstützt eine Hilfsprogrammklasse für das Netzwerk Diagnose Framework [(ndf)](/windows/desktop/NDF/extensible-helper-classes).</span><span class="sxs-lookup"><span data-stu-id="821ce-163">Supports a Network Diagnostics Framework [(NDF) helper class](/windows/desktop/NDF/extensible-helper-classes).</span></span>
-   <span data-ttu-id="821ce-164">Unterstützt die [Secure Socket-Erweiterungen](/windows/desktop/WinSock/winsock-secure-socket-extensions) für die Winsock-API, mit denen Netzwerkanwendungen den Datenverkehr durch Konfigurieren von WFP sichern können.</span><span class="sxs-lookup"><span data-stu-id="821ce-164">Supports the [Secure Socket extensions](/windows/desktop/WinSock/winsock-secure-socket-extensions) to the Winsock API, which allow network applications to secure their traffic by configuring WFP.</span></span>
-   <span data-ttu-id="821ce-165">Bei der Erzwingung der Logik Schicht wirkt sich minimal auf die Netzwerkleistung aus, indem nur das erste Paket in einer Verbindung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="821ce-165">At Application Layer Enforcement (ALE) layers, minimally impacts network performance by processing only the first packet in a connection.</span></span>
-   <span data-ttu-id="821ce-166">Integriert die Hardware Auslagerung, bei der kernelmoduscallout-Module Hardware verwenden können, um eine bestimmte Paket Untersuchung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="821ce-166">Integrates hardware offload where kernel-mode callout modules can use hardware to perform specific packet inspection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="821ce-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="821ce-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="821ce-168">WFP-Architektur</span><span class="sxs-lookup"><span data-stu-id="821ce-168">WFP Architecture</span></span>](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[<span data-ttu-id="821ce-169">WFP-Vorgang</span><span class="sxs-lookup"><span data-stu-id="821ce-169">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="821ce-170">Durchsetzung der Anwendungsschicht (ALE)</span><span class="sxs-lookup"><span data-stu-id="821ce-170">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="821ce-171">IPSec-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="821ce-171">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="821ce-172">WFP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="821ce-172">WFP Configuration</span></span>](wfp-configuration.md)
</dt> <dt>

[<span data-ttu-id="821ce-173">WFP-Überwachung</span><span class="sxs-lookup"><span data-stu-id="821ce-173">WFP Monitoring</span></span>](wfp-monitoring.md)
</dt> <dt>

[<span data-ttu-id="821ce-174">WFP-API</span><span class="sxs-lookup"><span data-stu-id="821ce-174">WFP API</span></span>](api-sets.md)
</dt> </dl>

 

