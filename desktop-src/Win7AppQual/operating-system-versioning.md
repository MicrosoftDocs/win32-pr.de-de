---
description: Betriebssystemversionsierung
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Betriebssystemversionsierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b8c60994eaee7a3becfa9acc03fe2c61fb12
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088038"
---
# <a name="operating-system-versioning"></a><span data-ttu-id="28db1-103">Betriebssystemversionsierung</span><span class="sxs-lookup"><span data-stu-id="28db1-103">Operating System Versioning</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="28db1-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="28db1-104">Affected Platforms</span></span>

<span data-ttu-id="28db1-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="28db1-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="28db1-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28db1-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="28db1-107">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="28db1-107">Feature Impact</span></span>

<span data-ttu-id="28db1-108">**Schweregrad:** Hoch</span><span class="sxs-lookup"><span data-stu-id="28db1-108">**Severity** - High</span></span>  
<span data-ttu-id="28db1-109">**Häufigkeit** – Hoch</span><span class="sxs-lookup"><span data-stu-id="28db1-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="28db1-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28db1-110">Description</span></span>

<span data-ttu-id="28db1-111">Die interne Versionsnummer für Windows 7 und Windows Server 2008 R2 ist 6.1.</span><span class="sxs-lookup"><span data-stu-id="28db1-111">The internal version number for Windows 7 and Windows Server 2008 R2 is 6.1.</span></span> <span data-ttu-id="28db1-112">Die GetVersion-Funktion gibt diese Versionsnummer jetzt an Anwendungen zurück, wenn sie abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="28db1-112">The GetVersion function will now return this version number to applications when queried.</span></span> <span data-ttu-id="28db1-113">Dies ist besonders wichtig für Anti Antivirus, Sicherung, Hilfsprogrammanwendungen und Kopierschutz.</span><span class="sxs-lookup"><span data-stu-id="28db1-113">This is especially important for AntiVirus, backup, utility applications, and copy protection.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="28db1-114">Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="28db1-114">Manifestation of Impact</span></span>

<span data-ttu-id="28db1-115">Der Grund für diese Änderung ist anwendungsspezifisch.</span><span class="sxs-lookup"><span data-stu-id="28db1-115">The manifestation of this change is application-specific.</span></span> <span data-ttu-id="28db1-116">Dies bedeutet, dass jede Anwendung, die speziell nach der Betriebssystemversion sucht, eine höhere Versionsnummer erhalten, was zu einer oder mehreren der folgenden Situationen führen kann:</span><span class="sxs-lookup"><span data-stu-id="28db1-116">This means that any application that specifically checks for the operating system version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="28db1-117">Anwendungsinstallationsprogramme können die Anwendung möglicherweise nicht installieren, und Anwendungen können möglicherweise nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="28db1-117">Application installers might be unable to install the application, and applications might be unable to start</span></span>
-   <span data-ttu-id="28db1-118">Anwendungen können instabil werden oder abstürzen</span><span class="sxs-lookup"><span data-stu-id="28db1-118">Applications might become unstable or crash</span></span>
-   <span data-ttu-id="28db1-119">Anwendungen generieren möglicherweise Fehlermeldungen, funktionieren aber weiterhin ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="28db1-119">Applications might generate error messages, but continue to function properly</span></span>

## <a name="mitigation"></a><span data-ttu-id="28db1-120">Minderung</span><span class="sxs-lookup"><span data-stu-id="28db1-120">Mitigation</span></span>

<span data-ttu-id="28db1-121">Die meisten Anwendungen funktionieren unter Windows 7 und Windows Server 2008 R2 ordnungsgemäß, da die Anwendungskompatibilität in Windows 7 und Windows Server 2008 R2 sehr hoch ist.</span><span class="sxs-lookup"><span data-stu-id="28db1-121">Most applications will function properly on Windows 7 and Windows Server 2008 R2 because the application compatibility in Windows 7 and Windows Server 2008 R2 is very high.</span></span> <span data-ttu-id="28db1-122">Windows 7 und Windows Server 2008 R2 enthalten jedoch eine Kompatibilitätsansicht für Installationsprogramme und Anwendungen, die nach Betriebssystemversionen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="28db1-122">However, Windows 7 and Windows Server 2008 R2 include a Compatibility View for installers and applications that check for operating system version.</span></span>

<span data-ttu-id="28db1-123">Um die Kompatibilitätsansicht zu aktivieren, können Benutzer mit der rechten Maustaste auf die Verknüpfung oder die ausführbare Datei klicken und dann die Windows XP SP2- oder Windows Vista-Kompatibilitätsansicht auf der Registerkarte Kompatibilität anwenden. In den meisten Fällen sollte dies der Anwendung ermöglichen, ordnungsgemäß zu arbeiten, ohne dass Änderungen an der Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="28db1-123">To enable the compatibility view, users can right-click the shortcut or the executable file, and then apply the Windows XP SP2 or Windows Vista Compatibility View from the Compatibility tab. In most cases, this should enable the application to operate properly without the need for any changes to the application.</span></span>

<span data-ttu-id="28db1-124">IT-Experten können auch alle anwendbaren Versionskompatibilitätskorrekturen anwenden, indem sie das Kompatibilitätsadministratortool verwenden, das mit dem Application Compatibility Toolkit (ACT) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="28db1-124">IT Professionals can also apply any of the applicable VersionLie compatibility fixes, by using the Compatibility Administrator tool, which installs with the Application Compatibility Toolkit (ACT).</span></span> <span data-ttu-id="28db1-125">Wenn eine Anwendung z. B. nicht funktioniert, weil sie die Windows XP® mit Sp2-Versionsinformationen (Service Pack 2) überprüft, aber nicht gefunden hat, kann winXPSP2VersionLie angewendet werden, um die richtigen Versionsnummerninformationen an die Anwendung zurückzugeben, unabhängig von der tatsächlichen Betriebssystemversion, die auf dem Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28db1-125">For example, if an application fails to function because it is checking for, but not finding, the Windows XP® with Service Pack 2 (SP2) version information, the WinXPSP2VersionLie can be applied to return the proper version number information to the application, regardless of the actual operating system version that is running on the computer.</span></span> <span data-ttu-id="28db1-126">Die verfügbaren Versionslie-Kompatibilitätskorrekturen sind:</span><span class="sxs-lookup"><span data-stu-id="28db1-126">The available VersionLie compatibility fixes are:</span></span>

-   <span data-ttu-id="28db1-127">Win95VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-127">Win95VersionLie</span></span>
-   <span data-ttu-id="28db1-128">Win98VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-128">Win98VersionLie</span></span>
-   <span data-ttu-id="28db1-129">WinNT4SP5VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-129">WinNT4SP5VersionLie</span></span>
-   <span data-ttu-id="28db1-130">Win2000VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-130">Win2000VersionLie</span></span>
-   <span data-ttu-id="28db1-131">Win2000SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-131">Win2000SP1VersionLie</span></span>
-   <span data-ttu-id="28db1-132">Win2000SP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-132">Win2000SP2VersionLie</span></span>
-   <span data-ttu-id="28db1-133">Win2000SP3VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-133">Win2000SP3VersionLie</span></span>
-   <span data-ttu-id="28db1-134">WinXPVersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-134">WinXPVersionLie</span></span>
-   <span data-ttu-id="28db1-135">WinXPSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-135">WinXPSP1VersionLie</span></span>
-   <span data-ttu-id="28db1-136">WinXPSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-136">WinXPSP2VersionLie</span></span>
-   <span data-ttu-id="28db1-137">VistaRTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-137">VistaRTMVersionLie</span></span>
-   <span data-ttu-id="28db1-138">VistaSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-138">VistaSP1VersionLie</span></span>
-   <span data-ttu-id="28db1-139">VistaSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-139">VistaSP2VersionLie</span></span>
-   <span data-ttu-id="28db1-140">Win2K3RTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-140">Win2K3RTMVersionLie</span></span>
-   <span data-ttu-id="28db1-141">Win2K3SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="28db1-141">Win2K3SP1VersionLie</span></span>

## <a name="solution"></a><span data-ttu-id="28db1-142">Lösung</span><span class="sxs-lookup"><span data-stu-id="28db1-142">Solution</span></span>

<span data-ttu-id="28db1-143">Im Allgemeinen sollten Anwendungen keine Überprüfungen der Betriebssystemversion durchführen.</span><span class="sxs-lookup"><span data-stu-id="28db1-143">Generally, applications should not perform operating system version checks.</span></span> <span data-ttu-id="28db1-144">Wenn eine Anwendung ein bestimmtes Feature benötigt, ist es besser zu versuchen, das Feature zu finden, und schlägt nur fehl, wenn das erforderliche Feature fehlt.</span><span class="sxs-lookup"><span data-stu-id="28db1-144">If an application needs a specific feature, it is preferable to try to find the feature, and fail only if the needed feature is missing.</span></span> <span data-ttu-id="28db1-145">Anwendungen sollten immer Versionsnummern akzeptieren, die größer oder gleich der niedrigsten unterstützten Version des Betriebssystems sind.</span><span class="sxs-lookup"><span data-stu-id="28db1-145">At a minimum, applications should always accept version numbers greater than or equal to the lowest supported version of the operating system.</span></span> <span data-ttu-id="28db1-146">Ausnahmen sollten nur auftreten, wenn eine bestimmte rechtliche, geschäftliche oder Systemkomponentenanforderung besteht.</span><span class="sxs-lookup"><span data-stu-id="28db1-146">Exceptions should occur only if there is a specific legal, business, or system-component requirement.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="28db1-147">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="28db1-147">Links to Other Resources</span></span>

-   [<span data-ttu-id="28db1-148">Download des Anwendungskompatibilitätstoolkits</span><span class="sxs-lookup"><span data-stu-id="28db1-148">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="28db1-149">[Bekannte Kompatibilitätskorrekturen, Kompatibilitätsmodi und AppHelp-Meldungen](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="28db1-149">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>

 

 
