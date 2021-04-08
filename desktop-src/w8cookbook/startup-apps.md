---
title: Start-apps
description: Start-apps
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- Start-App
- Hintergrundaufgabe
- Taste ausführen
- RunOnce
- Startordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "103734632"
---
# <a name="startup-apps"></a><span data-ttu-id="d3f5a-108">Start-apps</span><span class="sxs-lookup"><span data-stu-id="d3f5a-108">Startup apps</span></span>

## <a name="platform"></a><span data-ttu-id="d3f5a-109">Plattform</span><span class="sxs-lookup"><span data-stu-id="d3f5a-109">Platform</span></span>

<span data-ttu-id="d3f5a-110">**Clients**   Windows 8</span><span class="sxs-lookup"><span data-stu-id="d3f5a-110">**Clients**   Windows 8</span></span>  


## <a name="description"></a><span data-ttu-id="d3f5a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3f5a-111">Description</span></span>

<span data-ttu-id="d3f5a-112">Eine der großen Wett-und Windows-Anwendungen ist die Möglichkeit, verschiedene Formfaktoren, von herkömmlichen Desktops und Laptops bis hin zu kleinen Tablets, zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-112">One of the big bets with Windows is the ability to light up various form factors, from the traditional desktops and laptops to low-powered tablets.</span></span> <span data-ttu-id="d3f5a-113">Um sicherzustellen, dass unsere wechselseitigen Kunden eine gute Benutzeroberfläche für jeden von Ihnen gewählten Formfaktor haben, sind zwei wichtige Erfolgs Metriken, die berücksichtigt werden müssen, eine größere Akku Lebensdauer und eine ausgezeichnete PC-Reaktionsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-113">To ensure that our mutual customers have a great experience on any form factor they choose with Windows, two key success metrics that need to be addressed are increased battery life and excellent PC responsiveness.</span></span> <span data-ttu-id="d3f5a-114">Um dies zu erreichen, wurden Verbesserungen an mehreren Windows-Bereichen vorgenommen, einschließlich Prozess Lebenszyklus, Ruhezustand und Start-apps (Apps mit automatisiertem Start nach dem Starten des Computers).</span><span class="sxs-lookup"><span data-stu-id="d3f5a-114">In order to achieve these, improvements have been made in multiple areas of Windows including process life cycle, sleep states and startup apps (apps with automated launch after machine boot).</span></span> <span data-ttu-id="d3f5a-115">In diesem Thema werden einige der Auswirkungen von Start-apps auf einem Windows-Gerät hervorgehoben und Anleitungen für Entwickler (ISV/IHV) und OEMs bereitstellt, um die Verwendungs Muster von Start-apps zu überdenken, um die Akku Lebensdauer und Reaktionsfähigkeit unserer gegenseitigen Kunden zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-115">This topic highlights some of the impacts that startup apps have on a Windows device, and provides guidance to developers (ISV/IHV) and OEMs to rethink the usage patterns of startup apps in order to improve battery life and responsiveness for our mutual customers.</span></span> <span data-ttu-id="d3f5a-116">Außerdem werden die Änderungen in Windows beschrieben, mit denen Benutzer steuern können, welche der Start-apps tatsächlich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-116">It also describes the changes in Windows that put users in control of determining which of the startup apps actually get to execute.</span></span>

<span data-ttu-id="d3f5a-117">Windows Store-Apps sind so konzipiert, dass Sie neuen Standards für den Akku Verbrauch und die Reaktionsfähigkeit entsprechen, und Windows verwaltet ihren Lebenszyklus, indem Sie angehalten und/oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-117">Windows Store apps are designed to adhere to new standards of battery consumption and responsiveness, and Windows manages their life cycle by suspending and/or terminating them.</span></span> <span data-ttu-id="d3f5a-118">Desktop-Apps, die für frühere Windows-Versionen entwickelt wurden, wurden jedoch nicht notwendigerweise so entworfen, dass Sie die Akku Lebensdauer beibehalten oder die Benutzeraktivität beeinträchtigen können. Sie können sich auch auf die Reaktionsfähigkeit des Systems auswirken (z. b. Wenn eine APP einen regulären 1-Sekunden-Takt sendet, um nach Updates zu suchen, oder den Arbeitsspeicher vorab bereitstellen).</span><span class="sxs-lookup"><span data-stu-id="d3f5a-118">However, desktop apps designed for prior Windows versions have not necessarily been designed to preserve battery life or be sensitive to user activity, and can affect system responsiveness (for example, when an app sends a regular 1-second heartbeat to check for updates, or pre-allocates memory upfront in case it needs it later).</span></span> <span data-ttu-id="d3f5a-119">Dies kann für den Benutzer, der einen Windows-Tablet PC kauft, mit einer langen Akku Lebensdauer und Wochen im Standbymodus eine schlechte Benutzer Leistung schaffen, aber es wird feststellt, dass die Akku Lebensdauer des Tablets diese Ziele nicht erreicht.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-119">This can create a poor experience for the user who buys a Windows tablet PC with a long battery life expectancy and weeks of standby, but discovers the tablet s battery life does not achieve these goals.</span></span> <span data-ttu-id="d3f5a-120">Da Start-apps im Hintergrund ausgeführt werden, kann die Anzahl von apps, die auf dem System ausgeführt werden, deutlich länger sein als das, was der Benutzer kennt, und sich auf die Reaktionsfähigkeit des Systems auswirken.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-120">Also, since startup apps run in the background, the number of apps running on the system can be significantly more than what the user is aware of and affect system responsiveness.</span></span> <span data-ttu-id="d3f5a-121">Start-apps werden klassifiziert, um diejenigen zu berücksichtigen, die diese Mechanismen zum Starten nutzen:</span><span class="sxs-lookup"><span data-stu-id="d3f5a-121">Startup apps are classified to include those leveraging these mechanisms to start:</span></span>

-   <span data-ttu-id="d3f5a-122">Ausführen von Registrierungs Schlüsseln (HKLM, HKCU, WOW64-Knoten eingeschlossen)</span><span class="sxs-lookup"><span data-stu-id="d3f5a-122">Run registry keys (HKLM, HKCU, wow64 nodes included)</span></span>
-   <span data-ttu-id="d3f5a-123">RunOnce-Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="d3f5a-123">RunOnce registry keys</span></span>
-   <span data-ttu-id="d3f5a-124">Startordner im Startmenü für Benutzer-und öffentliche Speicherorte</span><span class="sxs-lookup"><span data-stu-id="d3f5a-124">Startup folders under the start menu for per user and public locations</span></span>

<span data-ttu-id="d3f5a-125">Windows wurde eine neue Funktionalität hinzugefügt, um sicherzustellen, dass Endbenutzer immer die Kontrolle über die apps haben, die auf Ihren Systemen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-125">New functionality has been added to Windows to ensure that end users are always in control of the apps that run on their systems.</span></span> <span data-ttu-id="d3f5a-126">Auf der Registerkarte "Start" im Task-Manager wird eine Liste der Start-apps angezeigt. Außerdem werden Steuerelemente angezeigt, mit denen Benutzer Start-apps deaktivieren</span><span class="sxs-lookup"><span data-stu-id="d3f5a-126">The Startup tab in Task Manager shows a list of startup apps, along with controls that allow users to disable startup apps.</span></span> <span data-ttu-id="d3f5a-127">Um Benutzern zu helfen, zu deaktivieren, was deaktiviert werden soll, zeigt der Task-Manager ein Measure für jede Auswirkung der Start-APP an</span><span class="sxs-lookup"><span data-stu-id="d3f5a-127">To help users determine what to disable, Task Manager displays a measure of each startup app s impact.</span></span> <span data-ttu-id="d3f5a-128">Die Auswirkung wird basierend auf der CPU und der Datenträger Nutzung einer APP beim Start bewertet.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-128">Impact is assessed based on an app s CPU and disk usage at startup.</span></span> <span data-ttu-id="d3f5a-129">Die Auswirkung von Werten wird durch Anwenden der folgenden Kriterien bestimmt:</span><span class="sxs-lookup"><span data-stu-id="d3f5a-129">Impact values are determined by applying these criteria:</span></span>

-   <span data-ttu-id="d3f5a-130">**Hohe Auswirkung**   Apps, die mehr als eine Sekunde CPU-Zeit oder mehr als 3 MB Datenträger-e/a beim Start verwenden</span><span class="sxs-lookup"><span data-stu-id="d3f5a-130">**High impact**   Apps that use more than 1 second of CPU time or more than 3 MB of disk I/O at startup</span></span>
-   <span data-ttu-id="d3f5a-131">**Mittlere Auswirkung**   Apps mit 300 MS-1000 ms CPU-Zeit oder 300 KB-3 MB Datenträger-e/a</span><span class="sxs-lookup"><span data-stu-id="d3f5a-131">**Medium impact**   Apps that use 300 ms - 1000 ms of CPU time or 300 KB - 3 MB of disk I/O</span></span>
-   <span data-ttu-id="d3f5a-132">**Geringe Auswirkung**   Apps, die weniger als 300 ms CPU-Zeit und weniger als 300 KB Datenträger-e/a verwenden</span><span class="sxs-lookup"><span data-stu-id="d3f5a-132">**Low impact**   Apps that use less than 300 ms of CPU time and less than 300 KB of disk I/O</span></span>

<span data-ttu-id="d3f5a-133">Microsoft stellt Tools bereit, die APP-Entwicklern bei der Bewertung, Analyse und Durchführung von Maßnahmen unterstützen, um die Auswirkungen auf den Start zu verringern und die Benutzer</span><span class="sxs-lookup"><span data-stu-id="d3f5a-133">Microsoft provides tools to help app developers assess, analyze and take steps to reduce their startup impact and improve the user experience.</span></span> <span data-ttu-id="d3f5a-134">Das Assessment and Deployment Kit bietet die Möglichkeit, eine Start Leistungsbewertung auszuführen und die Auswirkungen von apps zu messen, die beim Start ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-134">The Assessment and Deployment Kit provides the ability to run a boot performance assessment and measure the impact of apps that run at startup.</span></span> <span data-ttu-id="d3f5a-135">Die Bewertungsergebnisse enthalten ggf. detaillierte Analyse-und Wiederherstellungs Informationen für die wichtigsten Komponenten beim Windows-Start.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-135">The assessment results contain detailed analysis and remediation info where applicable, for the top-impacting components at Windows startup.</span></span> <span data-ttu-id="d3f5a-136">Mithilfe von Windows Performance Analyzer können App-Entwickler eine umfassende Analyse durchführen, um die Grundursache der Auswirkungen auf die Leistung zu ermitteln und die Windows-Startleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-136">Using the Windows Performance Analyzer, app developers can perform deep analysis to find the root cause of the performance impact and improve Windows startup performance.</span></span> <span data-ttu-id="d3f5a-137">Installieren Sie das Windows ADK von [hier](/previous-versions/windows/hh825494(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="d3f5a-137">Install the Windows ADK from [here](/previous-versions/windows/hh825494(v=win.10)).</span></span>

## <a name="guidance"></a><span data-ttu-id="d3f5a-138">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="d3f5a-138">Guidance</span></span>

<span data-ttu-id="d3f5a-139">Start-apps umfassen mehrere Kategorien, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-139">Startup apps span multiple categories as described in the table below.</span></span> <span data-ttu-id="d3f5a-140">Eine Reihe von Empfehlungen für Entwickler werden den Kategorien von Start-apps zugeordnet, um die oben beschriebenen Windows-Funktionsänderungen auszurichten.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-140">A set of recommendations for developers is mapped to the categories of startup apps to align with the Windows functional changes described above.</span></span>



<span data-ttu-id="d3f5a-141">Kategorien von Start-apps</span><span class="sxs-lookup"><span data-stu-id="d3f5a-141">Startup Apps Categories</span></span>

<span data-ttu-id="d3f5a-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3f5a-142">Description</span></span>

<span data-ttu-id="d3f5a-143">Empfehlung</span><span class="sxs-lookup"><span data-stu-id="d3f5a-143">Recommendation</span></span>

<span data-ttu-id="d3f5a-144">**Aktualisierungen**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-144">**Updaters**</span></span>

<span data-ttu-id="d3f5a-145">Überwachen und Aktualisieren von Benutzern für Online Updates</span><span class="sxs-lookup"><span data-stu-id="d3f5a-145">Monitor and update users for online updates</span></span>

<span data-ttu-id="d3f5a-146">**Wartungs Task**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-146">**Maintenance Task**</span></span>

> [!Note]  
> <span data-ttu-id="d3f5a-147">Alle Updates sollten Wartungs Tasks sein, ohne dass Anforderungen an die UI-Interaktion bestehen.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-147">All updates should be maintenance tasks, without any UI interaction requirements.</span></span> <span data-ttu-id="d3f5a-148">Apps sollten sich einfach selbst aktualisieren und bei einem Fehler ein Rollback durchführen.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-148">Apps should just update themselves quietly, and rollback on failure</span></span>

<br/>

<span data-ttu-id="d3f5a-149">$ {ROWSPAN2} $**Hardware Unterstützung**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="d3f5a-149">${ROWSPAN2}$**Hardware Assistance**${REMOVE}$</span></span>  

<span data-ttu-id="d3f5a-150">Alternative Zugriffspunkte</span><span class="sxs-lookup"><span data-stu-id="d3f5a-150">Alternative Access Points</span></span>

<span data-ttu-id="d3f5a-151">Bereitstellen des Zugriffs auf Windows-Features und-apps, die über andere Zugriffspunkte in Windows zugänglich sind</span><span class="sxs-lookup"><span data-stu-id="d3f5a-151">Provide access to Windows features and apps that are accessible via other access points in Windows</span></span>

<span data-ttu-id="d3f5a-152">**Remove**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-152">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="d3f5a-153">Der Schlüssel besteht darin, doppelte Features zu verringern, die in Windows vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-153">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="d3f5a-154">Benachrichtigt</span><span class="sxs-lookup"><span data-stu-id="d3f5a-154">Notifiers</span></span>

<span data-ttu-id="d3f5a-155">Benutzern Benachrichtigungen zu Ihren Geräten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="d3f5a-155">Provide users with notifications regarding their devices</span></span>

<span data-ttu-id="d3f5a-156">**Remove**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-156">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="d3f5a-157">Windows stellt Benachrichtigungen für Benutzer über Ihre Geräte bereit.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-157">Windows provides notifications to users about their devices</span></span>

<br/>

<span data-ttu-id="d3f5a-158">**Pre-Launcher**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-158">**Pre-launchers**</span></span>

<span data-ttu-id="d3f5a-159">Einige der für apps benötigten vorläufigen Aktivitäten werden bei der Benutzeranmeldung in eine Start-App verlagert.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-159">Some of preliminary activities needed by apps is offloaded to a startup app during user login</span></span>

<span data-ttu-id="d3f5a-160">**Remove**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-160">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="d3f5a-161">Windows 8 ist für eine schnelle Darstellung von App-Starts optimiert.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-161">Windows 8 is optimized for a fast experience for app launches.</span></span>

<br/>

<span data-ttu-id="d3f5a-162">$ {ROWSPAN4} $**Utility**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="d3f5a-162">${ROWSPAN4}$**Utility**${REMOVE}$</span></span>  

<span data-ttu-id="d3f5a-163">PC-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="d3f5a-163">PC Sync</span></span>

<span data-ttu-id="d3f5a-164">Bereitstellen von Synchronisierungs Funktionen über mehrere Systeme hinweg</span><span class="sxs-lookup"><span data-stu-id="d3f5a-164">Provide sync functionality across multiple systems</span></span>

<span data-ttu-id="d3f5a-165">**Start** (potenzielle Updates in der Beta Version)</span><span class="sxs-lookup"><span data-stu-id="d3f5a-165">**Startup** (Potential updates in Beta)</span></span>

<span data-ttu-id="d3f5a-166">Sicherung und Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="d3f5a-166">Backup & Recovery</span></span>

<span data-ttu-id="d3f5a-167">Einstiegspunkt zum Speichern und Wiederherstellen des Zustands von Dateien, Einstellungen oder ganzen Systemen</span><span class="sxs-lookup"><span data-stu-id="d3f5a-167">Entry point to save and restore the state of files, settings, or entire systems</span></span>

<span data-ttu-id="d3f5a-168">**Windows Store-App für die Schnittstellen mit den Benutzern**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-168">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="d3f5a-169">Telemetrie</span><span class="sxs-lookup"><span data-stu-id="d3f5a-169">Telemetry</span></span>

<span data-ttu-id="d3f5a-170">Sammeln und Senden von Informationen über die Benutzerumgebung und die Umgebung</span><span class="sxs-lookup"><span data-stu-id="d3f5a-170">Collect and send info about the user experience and environment</span></span>

<span data-ttu-id="d3f5a-171">**Wartungs Task**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-171">**Maintenance Task**</span></span>

<span data-ttu-id="d3f5a-172">PC-Überwachung</span><span class="sxs-lookup"><span data-stu-id="d3f5a-172">PC Monitoring</span></span>

<span data-ttu-id="d3f5a-173">Bereitstellen von angeforderter Systemstatus Überwachung und Benachrichtigungen, die vorhandene Eingangsbox</span><span class="sxs-lookup"><span data-stu-id="d3f5a-173">Provide unsolicited system state monitoring and notifications that duplicate existing inbox functionality</span></span>

<span data-ttu-id="d3f5a-174">**Remove**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-174">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="d3f5a-175">Der Schlüssel besteht darin, doppelte Features zu verringern, die in Windows vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-175">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="d3f5a-176">$ {ROWSPAN2} $**Security**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="d3f5a-176">${ROWSPAN2}$**Security**${REMOVE}$</span></span>  

<span data-ttu-id="d3f5a-177">Eltern Steuerungs & Filter</span><span class="sxs-lookup"><span data-stu-id="d3f5a-177">Parental Control & Filters</span></span>

<span data-ttu-id="d3f5a-178">Erzwingen von Regeln und Einschränkungen für den Zugriff auf das Internet und die Verwendung</span><span class="sxs-lookup"><span data-stu-id="d3f5a-178">Enforce rules and restrictions established for Internet access and usage</span></span>

<span data-ttu-id="d3f5a-179">**Startup**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-179">**Startup**</span></span>

<span data-ttu-id="d3f5a-180">Konfiguration und Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d3f5a-180">Configuration & Management</span></span>

<span data-ttu-id="d3f5a-181">Benutzern das Steuern von Diagnose-und Wiederherstellungsoptionen für die Überwachung der Systemsicherheit gestatten Benutzer über Ergebnisse und Sicherheitsaktionen Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="d3f5a-181">Allow users to control diagnostic and remediation options for system security monitoring Notify users of findings and security actions</span></span>

<span data-ttu-id="d3f5a-182">**Windows Store-App für die Schnittstellen mit den Benutzern**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-182">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="d3f5a-183">**Kommunikation & Internet** (im & VoIP)</span><span class="sxs-lookup"><span data-stu-id="d3f5a-183">**Communication & Internet** (IM & VoIP)</span></span>

<span data-ttu-id="d3f5a-184">Senden und empfangen von Nachrichten und aufrufen</span><span class="sxs-lookup"><span data-stu-id="d3f5a-184">Send and receive messages and calls</span></span>

<span data-ttu-id="d3f5a-185">**Windows Store-App**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-185">**Windows Store app**</span></span>

<span data-ttu-id="d3f5a-186">**Musik & MP3**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-186">**Music & MP3**</span></span>

<span data-ttu-id="d3f5a-187">Spielen, speichern und Verwalten von Musik</span><span class="sxs-lookup"><span data-stu-id="d3f5a-187">Play, store, and manage music</span></span>

<span data-ttu-id="d3f5a-188">**Windows Store-App**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-188">**Windows Store app**</span></span>

<span data-ttu-id="d3f5a-189">**Foto & Video**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-189">**Photo & Video**</span></span>

<span data-ttu-id="d3f5a-190">Erkennen, aufzeichnen, wiedergeben, speichern und Verwalten von Fotos und Videos</span><span class="sxs-lookup"><span data-stu-id="d3f5a-190">Detect, record, render, store and manage photos and videos</span></span>

<span data-ttu-id="d3f5a-191">**Windows Store-App**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-191">**Windows Store app**</span></span>

<span data-ttu-id="d3f5a-192">**PC-Gaming**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-192">**PC Gaming**</span></span>

<span data-ttu-id="d3f5a-193">Spiele in verschiedenen Domänen starten</span><span class="sxs-lookup"><span data-stu-id="d3f5a-193">Launch games across various domains</span></span>

<span data-ttu-id="d3f5a-194">**Windows Store-App**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-194">**Windows Store app**</span></span>

<span data-ttu-id="d3f5a-195">**Upsell-& Ankündigung**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-195">**Upsell & Advertisement**</span></span>

<span data-ttu-id="d3f5a-196">Aufmerksamkeit auf waren und Dienste, die für den Kauf verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="d3f5a-196">Draw attention to goods and services available for purchase</span></span>

<span data-ttu-id="d3f5a-197">**Remove**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-197">**Remove**</span></span>



 

> [!Note]  
> <span data-ttu-id="d3f5a-198">Richtlinien für Barrierefreiheit-apps werden durch separate direkte Verpflichtungen mit ISVs abgedeckt.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-198">Accessibility apps guidelines are covered by separate direct engagements with ISVs.</span></span> <span data-ttu-id="d3f5a-199">Weitere Informationen finden Sie [*unter Programmieren für den einfachen Zugriff*](../winauto/ease-of-access---assistive-technology-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="d3f5a-199">See [*Programming for Ease of Access*](../winauto/ease-of-access---assistive-technology-registration.md) for details.</span></span>

 

<span data-ttu-id="d3f5a-200">**Windows Store-Apps**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-200">**Windows Store apps**</span></span>

<span data-ttu-id="d3f5a-201">Windows Store-Apps verbessern die Benutzeroberfläche durch die Einführung eines Windows-Raums mit neuen Koordinaten: ein neues app-Modell, eine neue Benutzeroberfläche und einen Windows Store.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-201">Windows Store apps enhance the user experience by introducing a Windows space with new coordinates: a new app model, a new user interface, and a Windows Store.</span></span> <span data-ttu-id="d3f5a-202">Diese sprach-und Präsentations Framework-Optionen sind für die Entwicklung von Windows Store-Apps verfügbar:</span><span class="sxs-lookup"><span data-stu-id="d3f5a-202">These language and presentation framework options are available for developing Windows Store apps:</span></span>

-   <span data-ttu-id="d3f5a-203">HTML/JavaScript/CSS</span><span class="sxs-lookup"><span data-stu-id="d3f5a-203">HTML/JavaScript/CSS</span></span>
-   <span data-ttu-id="d3f5a-204">XAML/C #</span><span class="sxs-lookup"><span data-stu-id="d3f5a-204">XAML/C#</span></span>
-   <span data-ttu-id="d3f5a-205">XAML/C++</span><span class="sxs-lookup"><span data-stu-id="d3f5a-205">XAML/C++</span></span>

<span data-ttu-id="d3f5a-206">Aggregierte Informationen für die Entwicklung von Windows Store-Apps finden Sie im [Windows dev Center](https://msdn.microsoft.com/windows/apps/).</span><span class="sxs-lookup"><span data-stu-id="d3f5a-206">Aggregated info for developing Windows Store apps is available at the [Windows Dev Center](https://msdn.microsoft.com/windows/apps/).</span></span>

<span data-ttu-id="d3f5a-207">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="d3f5a-207">Examples:</span></span>

-   <span data-ttu-id="d3f5a-208">[Entwickeln von Windows Store-spielen](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d3f5a-208">[Developing Windows Store games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="d3f5a-209">[Entwickeln einer Windows Store-App, die Medien verwendet](/previous-versions/windows/apps/hh465132(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d3f5a-209">[Developing Windows Store app that use Media](/previous-versions/windows/apps/hh465132(v=win.10))</span></span>

<span data-ttu-id="d3f5a-210">**Automatische Wartungs Tasks**</span><span class="sxs-lookup"><span data-stu-id="d3f5a-210">**Automatic maintenance tasks**</span></span>

<span data-ttu-id="d3f5a-211">Periodische Hintergrund Aktivitäten sollten als automatische Wartungs Tasks entworfen werden.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-211">Periodic background activity should be designed as Automatic Maintenance tasks.</span></span> <span data-ttu-id="d3f5a-212">Diese werden zur Leerlaufzeit des Systems geplant, um die Reaktionsfähigkeit und Energieeffizienz von Windows-PCs zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-212">These are scheduled at system idle time to increase the responsiveness and energy efficiency of Windows PCs.</span></span> <span data-ttu-id="d3f5a-213">Wartungs Tasks können von einer Desktop-App zur Installationszeit mithilfe des Desktop SDK erstellt und konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-213">Maintenance tasks can be created and configured by a desktop app at install time, using the desktop SDK.</span></span> <span data-ttu-id="d3f5a-214">Weitere Informationen finden Sie im folgenden Thema zur automatischen Wartung.</span><span class="sxs-lookup"><span data-stu-id="d3f5a-214">See the Automatic Maintenance topic that follows for details.</span></span>

## <a name="resources"></a><span data-ttu-id="d3f5a-215">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3f5a-215">Resources</span></span>

-   [<span data-ttu-id="d3f5a-216">Richtlinien für Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="d3f5a-216">Accessibility Guidelines</span></span>](../winauto/ease-of-access---assistive-technology-registration.md)
-   [<span data-ttu-id="d3f5a-217">Windows Developer Center</span><span class="sxs-lookup"><span data-stu-id="d3f5a-217">Windows Dev Center</span></span>](https://msdn.microsoft.com/windows/apps/)
-   <span data-ttu-id="d3f5a-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d3f5a-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span></span>

 

