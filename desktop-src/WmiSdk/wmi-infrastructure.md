---
description: In der WMI-Infrastruktur ist der WMI-Dienst (Winmgmt) die Betriebssystem Komponente, die als Vermittler zwischen Verwaltungs Anwendungen und WMI-Datenanbietern fungiert. Das WMI-Repository ist ein Speicherbereich für WMI-bezogene statische Daten.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: WMI-Infrastruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4370af9ec062ffa845d54eafda054357a76dc07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348544"
---
# <a name="wmi-infrastructure"></a><span data-ttu-id="cae8c-104">WMI-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="cae8c-104">WMI Infrastructure</span></span>

<span data-ttu-id="cae8c-105">In der WMI-Infrastruktur ist der WMI-Dienst (Winmgmt) die Betriebssystem Komponente, die als Vermittler zwischen Verwaltungs Anwendungen und WMI-Daten [*Anbietern*](gloss-p.md)fungiert.</span><span class="sxs-lookup"><span data-stu-id="cae8c-105">In the WMI infrastructure, the WMI service (Winmgmt) is the operating system component that acts as the mediator between management applications and WMI data [*providers*](gloss-p.md).</span></span> <span data-ttu-id="cae8c-106">Das [*WMI-Repository*](gloss-w.md) ist ein Speicherbereich für WMI-bezogene statische Daten.</span><span class="sxs-lookup"><span data-stu-id="cae8c-106">The [*WMI repository*](gloss-w.md) is a storage area for WMI-related static data.</span></span>

<span data-ttu-id="cae8c-107">Der WMI-Dienst wird als Dienst Prozess innerhalb eines gemeinsamen Dienst Host Prozesses (SVCHOST) implementiert.</span><span class="sxs-lookup"><span data-stu-id="cae8c-107">The WMI service is implemented as a service process within a shared service host process (SVCHOST).</span></span> <span data-ttu-id="cae8c-108">Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="cae8c-108">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="cae8c-109">Der WMI-Dienst wird gestartet, wenn die erste Verwaltungs Anwendung oder das erste Skript eine Verbindung mit einem WMI-Namespace herstellt.</span><span class="sxs-lookup"><span data-stu-id="cae8c-109">The WMI service starts when the first management application or script makes a call to connect to a WMI namespace.</span></span> <span data-ttu-id="cae8c-110">Abhängig von der Einrichtung wird der WMI-Dienst möglicherweise heruntergefahren oder zu einem Profil mit geringem Speicherplatz wechseln, wenn er nicht von einer Verwaltungs Anwendung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cae8c-110">Depending on the setup, the WMI service may shut down or go into a low memory profile when not being called by a management application.</span></span>

<span data-ttu-id="cae8c-111">Der WMI-Dienst interagiert mit Verwaltungs Anwendungen über die COM-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cae8c-111">The WMI service interacts with management applications through the COM interface.</span></span> <span data-ttu-id="cae8c-112">Wenn eine Anwendung über die-Schnittstelle eine Anforderung sendet, bestimmt WMI, ob die Anforderung für statische oder dynamische Daten ist.</span><span class="sxs-lookup"><span data-stu-id="cae8c-112">When an application makes a request through the interface, WMI determines whether the request is for static or dynamic data.</span></span> <span data-ttu-id="cae8c-113">Wenn die Anforderung statische Daten (z. b. den Namen eines verwalteten Objekts) umfasst, ruft WMI die Daten aus dem Repository ab.</span><span class="sxs-lookup"><span data-stu-id="cae8c-113">If the request involves static data, such as the name of a managed object, WMI retrieves the data from the repository.</span></span> <span data-ttu-id="cae8c-114">Wenn die Anforderung dynamische Daten umfasst, z. b. die Menge an Arbeitsspeicher, die ein verwaltetes Objekt zurzeit verwendet, übergibt WMI die Anforderung an einen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="cae8c-114">If the request involves dynamic data, such as the amount of memory a managed object is currently using, WMI passes the request on to a provider.</span></span>

<span data-ttu-id="cae8c-115">Anbieter registrieren ihren Speicherort beim WMI-Dienst, der WMI das Weiterleiten von Datenanforderungen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="cae8c-115">Providers register their location with the WMI service, which allows WMI to route data requests.</span></span> <span data-ttu-id="cae8c-116">Ein Anbieter registriert auch die Unterstützung für bestimmte Vorgänge, z. b. Datenabruf, Änderung, Löschung, Enumeration oder Abfrage Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="cae8c-116">A provider also registers support for particular operations, such as data retrieval, modification, deletion, enumeration, or query processing.</span></span> <span data-ttu-id="cae8c-117">Der WMI-Dienst verwendet die Anbieter Registrierungsinformationen, um Anwendungsanforderungen mit dem entsprechenden Anbieter abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="cae8c-117">The WMI service uses the provider registration information to match application requests with the appropriate provider.</span></span> <span data-ttu-id="cae8c-118">WMI verwendet die Registrierungsinformationen auch, um Anbieter nach Bedarf zu laden und zu entladen.</span><span class="sxs-lookup"><span data-stu-id="cae8c-118">WMI also uses the registration information to load and unload providers, as necessary.</span></span> <span data-ttu-id="cae8c-119">Wenn ein Anbieter die Verarbeitung einer Anforderung abschließt, gibt der Anbieter das Ergebnis an den WMI-Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="cae8c-119">When a provider finishes processing a request, the provider returns the result back to the WMI service.</span></span> <span data-ttu-id="cae8c-120">WMI leitet das Ergebnis dann über die COM-Schnittstelle an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="cae8c-120">WMI then forwards the result on to the application through the COM interface.</span></span> <span data-ttu-id="cae8c-121">Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cae8c-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="cae8c-122">WMI verwendet die [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) (ETW), um die WMI-Dienst Aktivität aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="cae8c-122">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) to record WMI service activity.</span></span>

<span data-ttu-id="cae8c-123">Da die-Infrastruktur den gesamten Datenverkehr zwischen den Anbietern und den Verwaltungs Anwendungen verarbeitet, bietet die-Infrastruktur die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="cae8c-123">Because the infrastructure handles all traffic between the providers and the management applications, the infrastructure provides the following features:</span></span>

-   <span data-ttu-id="cae8c-124">Unterstützung für Ereignis Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="cae8c-124">Event Notification Support</span></span>

    <span data-ttu-id="cae8c-125">Weitere Informationen finden Sie unter über [Wachen von Ereignissen](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="cae8c-125">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="cae8c-126">Unterstützung der Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="cae8c-126">Query Language Support</span></span>

    <span data-ttu-id="cae8c-127">Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="cae8c-127">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

-   <span data-ttu-id="cae8c-128">Sicherheitsunterstützung</span><span class="sxs-lookup"><span data-stu-id="cae8c-128">Security Support</span></span>

    <span data-ttu-id="cae8c-129">Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="cae8c-129">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

-   <span data-ttu-id="cae8c-130">Skripterstellung für den Zugriff auf Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="cae8c-130">Scripting Access to Performance Counter Data</span></span>

    <span data-ttu-id="cae8c-131">Weitere Informationen finden Sie unter über [Wachen von Leistungsdaten](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="cae8c-131">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cae8c-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cae8c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cae8c-133">WMI-Architektur</span><span class="sxs-lookup"><span data-stu-id="cae8c-133">WMI Architecture</span></span>](wmi-architecture.md)
</dt> </dl>

 

 
