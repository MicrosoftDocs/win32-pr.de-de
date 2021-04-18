---
description: .
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: Bewährte Methoden für die Energieeffizienz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a9980d199e2d95c6dbd01c642a1f00f45e584c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352577"
---
# <a name="best-practices-for-energy-efficiency"></a><span data-ttu-id="1ac83-103">Bewährte Methoden für die Energieeffizienz</span><span class="sxs-lookup"><span data-stu-id="1ac83-103">Best Practices for Energy Efficiency</span></span>

## <a name="platform"></a><span data-ttu-id="1ac83-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="1ac83-104">Platform</span></span>

 <span data-ttu-id="1ac83-105">**Clients** – Windows XP Windows \| Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="1ac83-105">**Clients** – Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="1ac83-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ac83-106">Description</span></span>

<span data-ttu-id="1ac83-107">Windows-basierte Laptops müssen die gesetzlichen Anforderungen an die Energieeffizienz erfüllen, wie z. b. die der USA Umweltschutzbehörde (EPA) Energy Star Program.</span><span class="sxs-lookup"><span data-stu-id="1ac83-107">Windows-based laptops must meet energy efficiency regulatory requirements such as those of the United States Environmental Protection Agency (EPA) Energy Star program.</span></span> <span data-ttu-id="1ac83-108">Außerdem haben Umfragen ergeben, dass die Dauer der Dauer des Akkus länger dauert als die meisten Kunden, die in Laptops benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="1ac83-108">Furthermore, surveys have shown that longer battery life continues to be what consumers most want and need in laptops.</span></span> <span data-ttu-id="1ac83-109">Um Kundenanforderungen gerecht zu werden, müssen Windows-Laptops ständig in den folgenden Bereichen fortfahren:</span><span class="sxs-lookup"><span data-stu-id="1ac83-109">To meet consumer demands, Windows laptops must continually advance in the following areas:</span></span>

-   <span data-ttu-id="1ac83-110">Energieeffizienz in allen Verwendungs Szenarien, einschließlich Leerlauf, produktionsworkloads, DVD-und Medienwiedergabe und Branchen Benchmarks</span><span class="sxs-lookup"><span data-stu-id="1ac83-110">Energy efficiency in all usage scenarios, including idle, productivity workloads, DVD and media playback, and industry benchmarks</span></span>
-   <span data-ttu-id="1ac83-111">Akku Lebensdauer für mobile PCs – für Hardwareplattformen und für Windows</span><span class="sxs-lookup"><span data-stu-id="1ac83-111">Mobile PC battery life—for hardware platforms and for Windows</span></span>

<span data-ttu-id="1ac83-112">Die Windows-Plattform ist äußerst zuverlässig und ermöglicht eine schnelle und leistungsfähige Leistung.</span><span class="sxs-lookup"><span data-stu-id="1ac83-112">The Windows platform is highly reliable and enables fast on-and-off performance.</span></span> <span data-ttu-id="1ac83-113">Erweiterungen, die für mobile PC-Systeme bereitgestellt werden, wie z. b. Dienste, System Steuerungs Applets, Treiber und andere Software, können sich jedoch erheblich auf die Leistung, Zuverlässigkeit und Energieeffizienz auswirken.</span><span class="sxs-lookup"><span data-stu-id="1ac83-113">However, extensions provided with mobile PC systems, such as services, system tray applets, drivers, and other software, can significantly affect performance, reliability, and energy efficiency.</span></span>

<span data-ttu-id="1ac83-114">Energieeffizienz ist ein komplexes Problem, bei dem Faktoren betroffen sind, die sich auf alle Elemente des PC-Ökosystems auswirken.</span><span class="sxs-lookup"><span data-stu-id="1ac83-114">Energy efficiency is a complex problem, with factors affected by and affecting all elements of the PC ecosystem.</span></span> <span data-ttu-id="1ac83-115">Kleinere Verbesserungen in mehreren Szenarien können die Energieeffizienz verbessern, aber eine einzelne Anwendung, ein leistungsfähiges Gerät oder ein Feature mit schlechter Leistung kann den Energieverbrauch erheblich steigern.</span><span class="sxs-lookup"><span data-stu-id="1ac83-115">Small enhancements across multiple scenarios can improve energy efficiency, but a single poorly performing application, device, or system feature can increase energy consumption significantly.</span></span>

<span data-ttu-id="1ac83-116">Hardware und Geräte bilden die Grundlage für die Energieeffizienz.</span><span class="sxs-lookup"><span data-stu-id="1ac83-116">Hardware and devices form the foundation for energy efficiency.</span></span> <span data-ttu-id="1ac83-117">Anwendungs-und Dienst Software müssen jedoch auch effizient sein, damit das System eine optimale Akku Lebensdauer erzielen kann.</span><span class="sxs-lookup"><span data-stu-id="1ac83-117">However, application and service software must also be efficient to allow the system to achieve optimal battery life.</span></span> <span data-ttu-id="1ac83-118">Jede Softwarekomponente im System, einschließlich des Betriebssystems und der durch den Wert hinzugefügten Anwendungen und Dienste, muss den grundlegenden Effizienz Richtlinien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1ac83-118">Each software component on the system, including the operating system and value-added applications and services, must conform to basic efficiency guidelines.</span></span> <span data-ttu-id="1ac83-119">Eine einzelne Anwendung oder ein fehlerhafter Dienst kann jegliche Energieeffizienz erzielen, die der neueste Prozessor, die Geräte oder die Platt Form Hardware erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="1ac83-119">A single misbehaving application or service can eliminate any energy efficiency gains that the latest processor, devices, or platform hardware achieved.</span></span> <span data-ttu-id="1ac83-120">Ausführlichere Informationen zur Akku Lebensdauer und Energieeffizienz finden Sie im [Handbuch zur Akku Lebensdauer](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#).</span><span class="sxs-lookup"><span data-stu-id="1ac83-120">For more detailed information regarding battery life and energy efficiency please refer to the [Battery Life Solutions Guide](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#).</span></span>

<span data-ttu-id="1ac83-121">Die wichtigsten Probleme und Komponenten, die sich auf die Akku Lebensdauer auf einem mobilen PC auswirken, sind folgende:</span><span class="sxs-lookup"><span data-stu-id="1ac83-121">The principle issues and components that affect battery life in a mobile PC are:</span></span>

<span data-ttu-id="1ac83-122">**Akku Merkmale**</span><span class="sxs-lookup"><span data-stu-id="1ac83-122">**Battery Characteristics**</span></span>

-   <span data-ttu-id="1ac83-123">Größe, Typ und Qualität der Akkukapazität wirken sich auf die Akku Lebensdauer aus</span><span class="sxs-lookup"><span data-stu-id="1ac83-123">Size, type, and quality of battery capacity affect battery life</span></span>
-   <span data-ttu-id="1ac83-124">Je größer der Akku, desto größer das Netzteil.</span><span class="sxs-lookup"><span data-stu-id="1ac83-124">The larger the battery, the greater the power supply</span></span>
-   <span data-ttu-id="1ac83-125">Größere Akkus sind teurer und schwerer. Benutzer bevorzugen leichtere Systeme</span><span class="sxs-lookup"><span data-stu-id="1ac83-125">Larger batteries are more expensive and heavier; users prefer lighter systems</span></span>

<span data-ttu-id="1ac83-126">**Hardwarekomponenten**</span><span class="sxs-lookup"><span data-stu-id="1ac83-126">**Hardware Components**</span></span>

-   <span data-ttu-id="1ac83-127">Häufigkeit und Tiefe der Hardware in niedrigere Energiezustände</span><span class="sxs-lookup"><span data-stu-id="1ac83-127">Frequency and depth to which hardware can enter lower power states</span></span>
-   <span data-ttu-id="1ac83-128">Hardware Unterstützung von niedrigeren Energiezuständen</span><span class="sxs-lookup"><span data-stu-id="1ac83-128">Hardware support of lower power states</span></span>
-   <span data-ttu-id="1ac83-129">Treiber Optimierung für Energieeffizienz</span><span class="sxs-lookup"><span data-stu-id="1ac83-129">Driver optimization for energy efficiency</span></span>

<span data-ttu-id="1ac83-130">**Betriebs System – gesteuerte Energie Verwaltung**</span><span class="sxs-lookup"><span data-stu-id="1ac83-130">**Operating System–Directed Power Management**</span></span>

-   <span data-ttu-id="1ac83-131">Effizienz von Windows-Code im Vergleich zur Auslastung im Leerlauf</span><span class="sxs-lookup"><span data-stu-id="1ac83-131">Efficiency of Windows code while under a load versus while idle</span></span>
-   <span data-ttu-id="1ac83-132">Die Zusammenarbeit aller Komponenten mit Windows-gesteuerter Energie Verwaltung</span><span class="sxs-lookup"><span data-stu-id="1ac83-132">Cooperation level of all components with Windows-directed power management</span></span>
-   <span data-ttu-id="1ac83-133">Ordnungsgemäße Konfiguration des Betriebssystems zur Optimierung der Energie Verwaltung durch Energierichtlinien Einstellungen</span><span class="sxs-lookup"><span data-stu-id="1ac83-133">Proper configuration of the operating system to optimize for power management through power policy settings</span></span>

<span data-ttu-id="1ac83-134">**Anwendungs Software und-Dienste**</span><span class="sxs-lookup"><span data-stu-id="1ac83-134">**Application Software and Services**</span></span>

-   <span data-ttu-id="1ac83-135">Effizienz von Anwendungen, Treibern und Diensten im Vergleich zum Leerlauf</span><span class="sxs-lookup"><span data-stu-id="1ac83-135">Efficiency of applications, drivers, and services while under a load versus while idle</span></span>
-   <span data-ttu-id="1ac83-136">Anwendungsebene der Anwendungen mit Windows – gesteuerte Energie Verwaltung</span><span class="sxs-lookup"><span data-stu-id="1ac83-136">Cooperation level of applications with Windows–directed power management</span></span>
-   <span data-ttu-id="1ac83-137">Software Gewährung des Systems oder der Geräte, die in den Energiespar Zustand "Leerlauf" eingegeben werden sollen</span><span class="sxs-lookup"><span data-stu-id="1ac83-137">Software allowance of the system or devices to enter into low-power idle states</span></span>

<span data-ttu-id="1ac83-138">Eine einzelne Anwendung oder Dienst Komponente kann verhindern, dass ein System die optimale Akku Lebensdauer erkennt.</span><span class="sxs-lookup"><span data-stu-id="1ac83-138">A single application or service component can prevent a system from realizing optimal battery life.</span></span> <span data-ttu-id="1ac83-139">Obwohl Windows viele Energie Konfigurationsoptionen bereitstellt, sind vorinstallierte Software-oder Energierichtlinien Einstellungen auf vielen Systemen nicht für die Host Hardwareplattform optimiert.</span><span class="sxs-lookup"><span data-stu-id="1ac83-139">Although Windows provides many power configuration options, preinstalled software or power policy settings on many systems are not optimized for the host hardware platform.</span></span>

<span data-ttu-id="1ac83-140">Eine gängige Methode zum Auswerten der Akku Lebensdauer von vorinstallierter Software besteht darin, den Stromverbrauch des Systems mit einer Neuinstallation von Windows im Vergleich zu einer Windows-Installation zu vergleichen, die zusätzliche Software und Dienste umfasst.</span><span class="sxs-lookup"><span data-stu-id="1ac83-140">A common method for evaluating the battery-life impact of preinstalled software is to compare the power consumption of the system with a clean installation of Windows versus a Windows installation that includes value-added software and services.</span></span> <span data-ttu-id="1ac83-141">Obwohl es sich bei einer Neuinstallation nicht um die typische Plattform handelt, die von OEMs an Kunden ausgeliefert wird, kann der Stromverbrauchs Vergleich einen Einblick in die Energieeffizienz der vorinstallierten Software bieten.</span><span class="sxs-lookup"><span data-stu-id="1ac83-141">Although a clean installation does not represent the typical platform that OEMs ship to customers, the power consumption comparison can provide insight into the energy-efficiency of preinstalled software.</span></span>

## <a name="best-practices"></a><span data-ttu-id="1ac83-142">Bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="1ac83-142">Best Practices</span></span>

<span data-ttu-id="1ac83-143">Um sicherzustellen, dass Ihre Anwendung auf Windows-Plattformen optimiert ist, befolgen Sie die folgenden bewährten Methoden, wenn Sie Anwendungen oder Dienste entwerfen:</span><span class="sxs-lookup"><span data-stu-id="1ac83-143">To ensure that your application is optimized on Windows platforms, follow these best practices when you design applications or services:</span></span>

-   <span data-ttu-id="1ac83-144">**Vermeiden Sie die Verwendung von periodischen Zeit Gebern mit hoher Auflösung.**</span><span class="sxs-lookup"><span data-stu-id="1ac83-144">**Avoid use of high-resolution periodic timers**</span></span>

<dl> <span data-ttu-id="1ac83-145">Verwenden von periodischen Zeit Gebern mit hoher Auflösung (</span><span class="sxs-lookup"><span data-stu-id="1ac83-145">Using high-resolution periodic timers (</span></span><10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   <span data-ttu-id="1ac83-146">**In Leistungsoptimierungen investieren**</span><span class="sxs-lookup"><span data-stu-id="1ac83-146">**Invest in performance optimizations**</span></span>

<dl> <span data-ttu-id="1ac83-147">Jede Leistungsoptimierung ist eine Optimierung der Akku Lebensdauer.</span><span class="sxs-lookup"><span data-stu-id="1ac83-147">Every performance optimization is a battery life optimization.</span></span> <span data-ttu-id="1ac83-148">Durch die Reduzierung der erforderlichen Ressourcen, z. b. die Verwendung der geringeren Prozessorzeit oder der Datenträger Lesevorgänge bei der Batch Verarbeitung/Cluster Verarbeitung, kann sich die System Hardware in den Leerlauf versetzen und in den Modus</span><span class="sxs-lookup"><span data-stu-id="1ac83-148">Reductions in required resources, such as using less processor time or batching/clustering disk reads, allow system hardware to become idle and enter low-power modes.</span></span>  
</dl>

-   <span data-ttu-id="1ac83-149">**Anpassen an die Benutzer Energierichtlinie**</span><span class="sxs-lookup"><span data-stu-id="1ac83-149">**Adjust to user power policy**</span></span>

<dl> <span data-ttu-id="1ac83-150">Windows Vista und höher erleichtern es dem Benutzer, die Gesamtenergieeinsparung oder das Leistungsverhalten des Systems auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1ac83-150">Windows Vista and later make it easy for the user to choose the overall power-savings or performance behavior of the system.</span></span> <span data-ttu-id="1ac83-151">Ihre Anwendung sollte auf Änderungen der Energierichtlinie reagieren und die Ressourcennutzung reduzieren oder die Leistung entsprechend steigern.</span><span class="sxs-lookup"><span data-stu-id="1ac83-151">Your application should respond to changes in power policy and reduce resource usage or increase performance accordingly.</span></span> <span data-ttu-id="1ac83-152">Beispielsweise sollte eine Anwendung Hintergrund Aktivitäten wie z. b. Indizierung oder Systemüberprüfung deaktivieren, wenn der Benutzer einen Energiespar Energie Sparplan ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="1ac83-152">For example, an application should disable background activity such as indexing or system scanning when the user has selected a Power Saver power plan.</span></span>  
</dl>

-   <span data-ttu-id="1ac83-153">**Reduzieren der Ressourcennutzung, wenn sich das System im Akku Betrieb befindet**</span><span class="sxs-lookup"><span data-stu-id="1ac83-153">**Reduce resource usage when the system is on battery power**</span></span>

<dl> <span data-ttu-id="1ac83-154">Ihre Anwendung sollte den Ressourcenverbrauch reduzieren, z. b. die Häufigkeit des Aktualisierungs Intervalls, wenn sich das System in der Akkuleistung befindet.</span><span class="sxs-lookup"><span data-stu-id="1ac83-154">Your application should reduce its resource usage - such as background update frequency - when the system is on battery power.</span></span>  
</dl>

-   <span data-ttu-id="1ac83-155">**Nicht in der angezeigten Anzeige Rendering**</span><span class="sxs-lookup"><span data-stu-id="1ac83-155">**Do not render to the display when it is off**</span></span>

<dl> <span data-ttu-id="1ac83-156">Die System Anzeige ist möglicherweise deaktiviert, um Energieeinsparungen zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="1ac83-156">The system display might be off for power savings.</span></span> <span data-ttu-id="1ac83-157">Die Anwendung sollte keine unnötige Grafik Rendering durchführen, wenn die Anzeige deaktiviert ist, da dadurch Systemressourcen und eine Stromversorgung verschwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ac83-157">Your application should not perform unnecessary graphics rendering when the display is off because this wastes system resources and power.</span></span>  
</dl>

-   <span data-ttu-id="1ac83-158">**Vermeiden von Abfragen und Gliederung in engen Schleifen**</span><span class="sxs-lookup"><span data-stu-id="1ac83-158">**Avoid polling and spinning in tight loops**</span></span>

<dl> <span data-ttu-id="1ac83-159">Hohe Prozessorauslastung reduziert die Effektivität von Technologien zur Prozessor Energie Verwaltung, wie z. b. Prozessor-Leerlauf Zustände und Prozessor Leistungszustände.</span><span class="sxs-lookup"><span data-stu-id="1ac83-159">Heavy processor usage reduces the effectiveness of processor power-management technologies such as processor idle states and processor performance states.</span></span>  
</dl>

-   <span data-ttu-id="1ac83-160">**Verhindern, dass das System die Anzeige oder die Leerlaufzeit in den Standbymodus schaltet**</span><span class="sxs-lookup"><span data-stu-id="1ac83-160">**Do not prevent the system from turning off the display or idling to sleep**</span></span>

<dl> <span data-ttu-id="1ac83-161">Die Anwendung sollte mit der SetThreadExecutionState-API über die SetThreadExecutionState-API verfügen.</span><span class="sxs-lookup"><span data-stu-id="1ac83-161">Your application should make judicious power requests with the SetThreadExecutionState API.</span></span> <span data-ttu-id="1ac83-162">Das System sollte diese Anforderungen nur dann stellen, wenn kritische Vorgänge das System vor dem Ausschalten der Anzeige oder dem automatischen Wechsel in den Standbymodus verzögern müssen.</span><span class="sxs-lookup"><span data-stu-id="1ac83-162">The system should make these requests only when critical operations must delay the system from powering off the display or automatically entering sleep.</span></span>  
</dl>

-   <span data-ttu-id="1ac83-163">**Antworten auf häufige Ereignisse der Energie Verwaltung**</span><span class="sxs-lookup"><span data-stu-id="1ac83-163">**Respond to common power-management events**</span></span>

<dl> <span data-ttu-id="1ac83-164">Die Anwendung sollte sich für allgemeine Energie Verwaltungs Ereignisse registrieren und auf diese reagieren, wie z. b. Änderungen an der System Energiequelle und Einschalt-und Ausschalten von Benachrichtigungen für die Anzeige.</span><span class="sxs-lookup"><span data-stu-id="1ac83-164">Your application should register for and respond to common power-management events, such as system power-source changes and power-on and power-off notifications for the display.</span></span>  
</dl>

-   <span data-ttu-id="1ac83-165">**Aktivieren Sie die Debugprotokollierung nicht standardmäßig. Verwenden Sie stattdessen die Ereignis Ablauf Verfolgung für Windows.**</span><span class="sxs-lookup"><span data-stu-id="1ac83-165">**Do not enable debug logging by default; use Event Tracing for Windows instead**</span></span>

<dl> <span data-ttu-id="1ac83-166">Eine regelmäßige Debugprotokollierung kann die Datenträger-Spin-Down</span><span class="sxs-lookup"><span data-stu-id="1ac83-166">Periodic debug logging can prevent disk spin-down.</span></span>  
</dl>

## <a name="links-to-other-resources"></a><span data-ttu-id="1ac83-167">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1ac83-167">Links to Other Resources</span></span>

-   [<span data-ttu-id="1ac83-168">Leitfaden zu den Akku lebenslösungen</span><span class="sxs-lookup"><span data-stu-id="1ac83-168">Battery Life Solutions Guide</span></span>](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [<span data-ttu-id="1ac83-169">Energieeffizienz Portal</span><span class="sxs-lookup"><span data-stu-id="1ac83-169">Energy Efficiency Portal</span></span>](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [<span data-ttu-id="1ac83-170">Windows Performance Toolkit</span><span class="sxs-lookup"><span data-stu-id="1ac83-170">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



