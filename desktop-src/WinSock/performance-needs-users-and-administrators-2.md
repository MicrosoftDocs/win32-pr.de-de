---
description: Leistungsanforderungen von Benutzern und Administratoren mit Windows Sockets (Winsock)-Anwendungen.
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Leistungsanforderungen: Benutzer und Administratoren'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a8178cf1d7516e9c16493916f8cf911752b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041722"
---
# <a name="performance-needs-users-and-administrators"></a><span data-ttu-id="8f0dc-103">Leistungsanforderungen: Benutzer und Administratoren</span><span class="sxs-lookup"><span data-stu-id="8f0dc-103">Performance Needs: Users and Administrators</span></span>

<span data-ttu-id="8f0dc-104">Benutzer beurteilen die Anwendungsleistung nach ihren Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="8f0dc-104">Users judge application performance by their experience:</span></span>

-   <span data-ttu-id="8f0dc-105">Reagiert die Anwendung schnell?</span><span class="sxs-lookup"><span data-stu-id="8f0dc-105">Is the application quick to respond?</span></span>
-   <span data-ttu-id="8f0dc-106">Wird ein Sanduhr Symbol angezeigt, während Hintergrund Vorgänge ausgeführt werden?</span><span class="sxs-lookup"><span data-stu-id="8f0dc-106">Is an hourglass icon displayed while background operations are carried out?</span></span>
-   <span data-ttu-id="8f0dc-107">Wird die Anwendung schnell gestartet und geschlossen?</span><span class="sxs-lookup"><span data-stu-id="8f0dc-107">Does the application launch and close quickly?</span></span>
-   <span data-ttu-id="8f0dc-108">Werden Fehler verständlich behandelt?</span><span class="sxs-lookup"><span data-stu-id="8f0dc-108">Are errors handled in an understandable way?</span></span>

<span data-ttu-id="8f0dc-109">Zusammenfassend möchten Benutzer, dass Anwendungen schnell und vorhersagbar sind.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-109">To summarize, users want applications to be fast and predictable.</span></span>

<span data-ttu-id="8f0dc-110">Im Gegensatz dazu beurteilen Administratoren oft die Leistung einer Anwendung, um zu bestimmen, wie effizient Netzwerkressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-110">In contrast, administrators often judge an application's performance on how efficiently it uses network resources.</span></span> <span data-ttu-id="8f0dc-111">Administratoren können Folgendes anfordern:</span><span class="sxs-lookup"><span data-stu-id="8f0dc-111">Administrators may ask:</span></span>

-   <span data-ttu-id="8f0dc-112">Hat die Anwendung einen geringen Verwaltungsaufwand und eine effiziente Netzwerk Auslastung?</span><span class="sxs-lookup"><span data-stu-id="8f0dc-112">Does the application have low overhead and efficient network usage?</span></span>
-   <span data-ttu-id="8f0dc-113">Wird die Mindestanzahl von Verbindungen verwendet, sodass der Server so viele Benutzer gleichzeitig wie möglich bedienen kann?</span><span class="sxs-lookup"><span data-stu-id="8f0dc-113">Are the minimum number of connections used, so my server can service as many users at once as possible?</span></span>
-   <span data-ttu-id="8f0dc-114">Rufe ich den Helpdesk ständig auf?</span><span class="sxs-lookup"><span data-stu-id="8f0dc-114">Am I constantly calling helpdesk?</span></span>

<span data-ttu-id="8f0dc-115">Kurz gesagt: Administratoren möchten, dass Anwendungen skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-115">In short, administrators want applications to scale.</span></span>

## <a name="best-practices-for-performance-needs"></a><span data-ttu-id="8f0dc-116">Bewährte Methoden für Leistungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="8f0dc-116">Best Practices for Performance Needs</span></span>

<span data-ttu-id="8f0dc-117">Wenn Sie eine Windows Sockets-Anwendung entwickeln, werden diese Leistungsanforderungen in nützliche Regeln übersetzt.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-117">When developing a Windows Sockets application, these performance requirements translate into useful rules.</span></span>

-   <span data-ttu-id="8f0dc-118">Schnelle Initialisierung von Netzwerkanwendungen.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-118">Have network applications initialize quickly.</span></span>

    <span data-ttu-id="8f0dc-119">Die Benutzeroberfläche sollte nicht auf Netzwerk Antworten warten müssen.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-119">The user interface should not have to wait for network responses.</span></span> <span data-ttu-id="8f0dc-120">Einige Tasks können ausgeführt werden, bevor das Netzwerk verfügbar ist, oder ohne das Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-120">Some tasks can be performed before the network is available, or without the network.</span></span> <span data-ttu-id="8f0dc-121">Wenn das Netzwerk nicht antwortet, benötigt der Benutzer möglicherweise die Benutzeroberfläche für einfache Vorgänge, z. b. das Schließen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-121">If the network is not responding, the user may need the user interface for simple operations, such as closing the application.</span></span>

-   <span data-ttu-id="8f0dc-122">Warten Sie nicht, bis das Netzwerk heruntergefahren ist.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-122">Do not wait for the network for shutdown.</span></span>

    <span data-ttu-id="8f0dc-123">Ordnungsgemäß geschriebene Client/Server-Anwendungen verarbeiten Abbruch Abbruch ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-123">Properly written client-server applications handle abortive disconnects gracefully.</span></span> <span data-ttu-id="8f0dc-124">Initiieren Sie keinen möglicherweise langwierigen Vorgang, z. b. das Synchronisieren von Dateien oder Ordnern mit einem Server, der beim Herunterfahren nicht unterbrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-124">Do not initiate a potentially lengthy operation, such as synchronizing files or folders with a server, that cannot be interrupted on shutdown.</span></span> <span data-ttu-id="8f0dc-125">Netzwerke sind nicht konsistent reaktionsfähig, sodass sogar kleine Vorgänge zeitaufwändig sein könnten.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-125">Networks are not consistently responsive, so even small operations could prove time consuming.</span></span> <span data-ttu-id="8f0dc-126">Bereitstellen von positivem Feedback für Benutzer, einschließlich Hinweise zum Fortschritt und zu geschätzten Abschlusszeiten.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-126">Provide positive feedback for users, including indications of progress and estimated completion times.</span></span>

-   <span data-ttu-id="8f0dc-127">Stellen Sie eine reaktionsfähige Benutzeroberfläche sicher.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-127">Ensure a responsive user interface.</span></span>

    <span data-ttu-id="8f0dc-128">Die Reaktionsfähigkeit der Anwendung hilft, unnötige Helpdeskanrufe auszuschließen</span><span class="sxs-lookup"><span data-stu-id="8f0dc-128">Application responsiveness helps eliminate unnecessary helpdesk calls.</span></span> <span data-ttu-id="8f0dc-129">Eine gute Richtlinie für die interaktive Reaktion ist 500 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-129">A good guideline for interactive response is 500 milliseconds.</span></span> <span data-ttu-id="8f0dc-130">Benutzer sehen länger als 500 Millisekunden als Verzögerung der Leistung an.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-130">Users perceive pauses longer than 500 milliseconds as a lag in performance.</span></span> <span data-ttu-id="8f0dc-131">Anwendungen sollten ausreichend reaktionsfähig sein, um dem Benutzer die Gewissheit über die Anwendung zu geben.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-131">Applications should be responsive enough to provide the user with confidence about the application.</span></span>

-   <span data-ttu-id="8f0dc-132">Überprüfen Sie Netzwerkfehler.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-132">Scrutinize network errors.</span></span>

    <span data-ttu-id="8f0dc-133">Nicht alle Netzwerkfehler sind von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-133">Not all network errors are critical.</span></span> <span data-ttu-id="8f0dc-134">Beispielsweise kann eine Anwendung, die alle Daten empfangen oder gesendet hat, beim Schließen der Verbindung wahrscheinlich Fehler ignorieren.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-134">For example, an application that has received or posted all of its data can likely ignore errors when closing the connection.</span></span> <span data-ttu-id="8f0dc-135">Gehen Sie nicht davon aus, dass das Netzwerk oder der Benutzer verfügbar ist. behandeln Sie Fehler ohne Benutzereingriff, oder ignorieren Sie diese, wenn Fehler nicht kritisch sind.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-135">Do not assume the network or the user is available; either handle errors without user intervention, or ignore them if errors are noncritical.</span></span>

-   <span data-ttu-id="8f0dc-136">Eine Anwendung sollte Ihre eigenen angemessenen Timeouts definieren.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-136">An application should define its own reasonable time outs.</span></span>

    <span data-ttu-id="8f0dc-137">Beispielsweise kann eine Windows Sockets Connect ()-Anforderung unter bestimmten Bedingungen für bis zu 21 Sekunden blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-137">For example, a Windows Sockets connect() request may block under some conditions for as much as 21 seconds.</span></span> <span data-ttu-id="8f0dc-138">Anwendungen müssen ggf. ihre eigenen Timeouts für Ihre Benutzer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-138">Applications may need to introduce their own time outs as appropriate for their users.</span></span>

-   <span data-ttu-id="8f0dc-139">Minimieren Sie den Protokoll Aufwand.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-139">Minimize protocol overhead.</span></span>

    <span data-ttu-id="8f0dc-140">Die Erhaltung der Netzwerkbandbreite dient zum Minimieren des Protokoll Aufwands, der von Ihrer Anwendung verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-140">Conserving network bandwidth is partially about minimizing the protocol overhead incurred by your application.</span></span> <span data-ttu-id="8f0dc-141">Es geht auch darum, unnötigen Netzwerk Datenverkehr zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-141">It is also about eliminating unnecessary network traffic.</span></span> <span data-ttu-id="8f0dc-142">Zum Übertragen von Anwendungsdaten können Protokolle mit einem niedrigeren Header Mehraufwand verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-142">Protocols with a lower header overhead can be used to transfer application data.</span></span> <span data-ttu-id="8f0dc-143">Wenn Sie z. b. kleinere Mengen nicht kritischer oder wiederholbarer Daten senden, verwenden Sie UDP anstelle von TCP, um den mehr Aufwand im Zusammenhang mit der Verbindungs Einrichtung und-Wartung zu verringern.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-143">For example, when sending smaller amounts of noncritical or repeatable data, use UDP as opposed to TCP to reduce the overhead associated with connection establishment and maintenance.</span></span> <span data-ttu-id="8f0dc-144">Wenn die gleichen Daten an mehrere Empfänger gesendet werden müssen, sollten Sie Multicast in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-144">If the same data must be sent to multiple recipients, consider multicast.</span></span> <span data-ttu-id="8f0dc-145">Beachten Sie, dass UDP-Anwendungen nicht Fluss gesteuert werden – durch pushübertragung über die verfügbare Bandbreite kann schwerwiegender Netzwerkausfall verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-145">Be aware that UDP applications are not flow-controlled—pushing beyond the available bandwidth can cause catastrophic network failure.</span></span> <span data-ttu-id="8f0dc-146">Das Hilfsprogramm netstat kann mit den Optionen **-e** und **-s** verwendet werden, um Statistiken für verschiedene Protokolle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-146">The Netstat utility can be used with its **-e** and **-s** options to display statistics for various protocols.</span></span>

-   <span data-ttu-id="8f0dc-147">Sparen Sie Systemressourcen.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-147">Conserve system resources.</span></span>

    <span data-ttu-id="8f0dc-148">System Ressourcen können schnell verbraucht werden, wenn keine ordnungsgemäße Unterhaltung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-148">System resources can be consumed quickly if proper restraint is not used.</span></span> <span data-ttu-id="8f0dc-149">Beispielsweise verbrauchen Sockets-und TCP-Verbindungen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-149">For example, sockets and TCP connections consume resources.</span></span> <span data-ttu-id="8f0dc-150">Verwenden Sie zum Zweck der Anwendung nicht mehrere TCP-Verbindungen pro Client.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-150">Do not use several TCP connections per client where one will serve the application's purpose.</span></span>

<span data-ttu-id="8f0dc-151">Bei transaktionalen Anwendungen sind gute Benutzer Funktionen und eine geringe Netzwerk Auslastung nicht in Konflikt stehende Ziele.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-151">For transactional applications, good user experience and low network utilization are not conflicting goals.</span></span> <span data-ttu-id="8f0dc-152">Das Netzwerk stellt einen Engpass dar.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-152">The network is a bottleneck.</span></span> <span data-ttu-id="8f0dc-153">Netzwerk intensive Anwendungen verbringen länger Zeit mit dem warten, und gut geschriebene Netzwerkanwendungen sind so konzipiert, dass unnötige Wartezeit sowohl für die Benutzeroberfläche als auch für Netzwerkübertragungen minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="8f0dc-153">Network-intensive applications spend more time waiting, and well written network applications are designed to minimize unnecessary wait time, both for the user interface and for network transmissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f0dc-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f0dc-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f0dc-155">Hochleistungsfähige Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="8f0dc-155">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="8f0dc-156">Leistungsdimensionen</span><span class="sxs-lookup"><span data-stu-id="8f0dc-156">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



