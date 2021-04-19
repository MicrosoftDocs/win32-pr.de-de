---
description: .
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Versionsverwaltung des Betriebssystems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e71cb671e19463ca6137c9b0ce7af04c2793e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357051"
---
# <a name="operating-system-versioning"></a><span data-ttu-id="8dd15-103">Versionsverwaltung des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="8dd15-103">Operating System Versioning</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="8dd15-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="8dd15-104">Affected Platforms</span></span>

<span data-ttu-id="8dd15-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="8dd15-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="8dd15-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8dd15-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="8dd15-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="8dd15-107">Feature Impact</span></span>

<span data-ttu-id="8dd15-108">**Schweregrad** -hoch</span><span class="sxs-lookup"><span data-stu-id="8dd15-108">**Severity** - High</span></span>  
<span data-ttu-id="8dd15-109">**Häufigkeit** -hoch</span><span class="sxs-lookup"><span data-stu-id="8dd15-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="8dd15-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dd15-110">Description</span></span>

<span data-ttu-id="8dd15-111">Die interne Versionsnummer für Windows 7 und Windows Server 2008 R2 ist 6,1.</span><span class="sxs-lookup"><span data-stu-id="8dd15-111">The internal version number for Windows 7 and Windows Server 2008 R2 is 6.1.</span></span> <span data-ttu-id="8dd15-112">Diese Versionsnummer wird von der Funktion GetVersion nun bei der Abfrage an Anwendungen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8dd15-112">The GetVersion function will now return this version number to applications when queried.</span></span> <span data-ttu-id="8dd15-113">Dies ist insbesondere für Antivirus-, Sicherungs-, hilfsprogrammanwendungen und den Kopierschutz wichtig.</span><span class="sxs-lookup"><span data-stu-id="8dd15-113">This is especially important for AntiVirus, backup, utility applications, and copy protection.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="8dd15-114">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="8dd15-114">Manifestation of Impact</span></span>

<span data-ttu-id="8dd15-115">Die Manifestation dieser Änderung ist anwendungsspezifisch.</span><span class="sxs-lookup"><span data-stu-id="8dd15-115">The manifestation of this change is application-specific.</span></span> <span data-ttu-id="8dd15-116">Dies bedeutet, dass jede Anwendung, die speziell auf die Betriebssystemversion prüft, eine höhere Versionsnummer erhält, was zu einer oder mehreren der folgenden Situationen führen kann:</span><span class="sxs-lookup"><span data-stu-id="8dd15-116">This means that any application that specifically checks for the operating system version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="8dd15-117">Anwendungs Installationsprogramme können die Anwendung möglicherweise nicht installieren, und Anwendungen können möglicherweise nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="8dd15-117">Application installers might be unable to install the application, and applications might be unable to start</span></span>
-   <span data-ttu-id="8dd15-118">Anwendungen werden möglicherweise instabil oder abstürzen</span><span class="sxs-lookup"><span data-stu-id="8dd15-118">Applications might become unstable or crash</span></span>
-   <span data-ttu-id="8dd15-119">Anwendungen generieren möglicherweise Fehlermeldungen, funktionieren jedoch weiterhin ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="8dd15-119">Applications might generate error messages, but continue to function properly</span></span>

## <a name="mitigation"></a><span data-ttu-id="8dd15-120">Minderung</span><span class="sxs-lookup"><span data-stu-id="8dd15-120">Mitigation</span></span>

<span data-ttu-id="8dd15-121">Die meisten Anwendungen funktionieren ordnungsgemäß unter Windows 7 und Windows Server 2008 R2, da die Anwendungs Kompatibilität in Windows 7 und Windows Server 2008 R2 sehr hoch ist.</span><span class="sxs-lookup"><span data-stu-id="8dd15-121">Most applications will function properly on Windows 7 and Windows Server 2008 R2 because the application compatibility in Windows 7 and Windows Server 2008 R2 is very high.</span></span> <span data-ttu-id="8dd15-122">Windows 7 und Windows Server 2008 R2 enthalten jedoch eine Kompatibilitäts Ansicht für Installationsprogramme und Anwendungen, die auf die Betriebssystemversion überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8dd15-122">However, Windows 7 and Windows Server 2008 R2 include a Compatibility View for installers and applications that check for operating system version.</span></span>

<span data-ttu-id="8dd15-123">Um die Kompatibilitäts Ansicht zu aktivieren, können Benutzer mit der rechten Maustaste auf die Verknüpfung oder die ausführbare Datei klicken und dann die Kompatibilitäts Ansicht von Windows XP SP2 oder Windows Vista auf der Registerkarte Kompatibilität anwenden. In den meisten Fällen sollte dadurch die Anwendung ordnungsgemäß ausgeführt werden können, ohne dass Änderungen an der Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8dd15-123">To enable the compatibility view, users can right-click the shortcut or the executable file, and then apply the Windows XP SP2 or Windows Vista Compatibility View from the Compatibility tab. In most cases, this should enable the application to operate properly without the need for any changes to the application.</span></span>

<span data-ttu-id="8dd15-124">IT-Fachleute können auch beliebige der anwendbaren versionlie-Kompatibilitäts Korrekturen mithilfe des Compatibility Administrator-Tools anwenden, das mit dem Anwendungskompatibilitäts-Toolkit (Application Compatibility Toolkit, Act) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="8dd15-124">IT Professionals can also apply any of the applicable VersionLie compatibility fixes, by using the Compatibility Administrator tool, which installs with the Application Compatibility Toolkit (ACT).</span></span> <span data-ttu-id="8dd15-125">Wenn beispielsweise eine Anwendung nicht funktionsfähig ist, weil Sie die Versionsinformationen für Windows XP® mit Service Pack 2 (SP2) überprüft, aber nicht findet, kann WinXPSP2VersionLie angewendet werden, um die richtigen Versionsnummern Informationen unabhängig von der tatsächlichen Betriebssystemversion, die auf dem Computer ausgeführt wird, an die Anwendung zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8dd15-125">For example, if an application fails to function because it is checking for, but not finding, the Windows XP® with Service Pack 2 (SP2) version information, the WinXPSP2VersionLie can be applied to return the proper version number information to the application, regardless of the actual operating system version that is running on the computer.</span></span> <span data-ttu-id="8dd15-126">Die verfügbaren versionlie-Kompatibilitäts Korrekturen lauten:</span><span class="sxs-lookup"><span data-stu-id="8dd15-126">The available VersionLie compatibility fixes are:</span></span>

-   <span data-ttu-id="8dd15-127">Win95VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-127">Win95VersionLie</span></span>
-   <span data-ttu-id="8dd15-128">Win98VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-128">Win98VersionLie</span></span>
-   <span data-ttu-id="8dd15-129">WinNT4SP5VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-129">WinNT4SP5VersionLie</span></span>
-   <span data-ttu-id="8dd15-130">Win2000VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-130">Win2000VersionLie</span></span>
-   <span data-ttu-id="8dd15-131">Win2000SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-131">Win2000SP1VersionLie</span></span>
-   <span data-ttu-id="8dd15-132">Win2000SP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-132">Win2000SP2VersionLie</span></span>
-   <span data-ttu-id="8dd15-133">Win2000SP3VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-133">Win2000SP3VersionLie</span></span>
-   <span data-ttu-id="8dd15-134">Winxpversionlie</span><span class="sxs-lookup"><span data-stu-id="8dd15-134">WinXPVersionLie</span></span>
-   <span data-ttu-id="8dd15-135">WinXPSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-135">WinXPSP1VersionLie</span></span>
-   <span data-ttu-id="8dd15-136">WinXPSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-136">WinXPSP2VersionLie</span></span>
-   <span data-ttu-id="8dd15-137">Vistartmversionlie</span><span class="sxs-lookup"><span data-stu-id="8dd15-137">VistaRTMVersionLie</span></span>
-   <span data-ttu-id="8dd15-138">VistaSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-138">VistaSP1VersionLie</span></span>
-   <span data-ttu-id="8dd15-139">VistaSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-139">VistaSP2VersionLie</span></span>
-   <span data-ttu-id="8dd15-140">Win2K3RTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-140">Win2K3RTMVersionLie</span></span>
-   <span data-ttu-id="8dd15-141">Win2K3SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="8dd15-141">Win2K3SP1VersionLie</span></span>

## <a name="solution"></a><span data-ttu-id="8dd15-142">Lösung</span><span class="sxs-lookup"><span data-stu-id="8dd15-142">Solution</span></span>

<span data-ttu-id="8dd15-143">Im Allgemeinen sollten Anwendungen keine Überprüfungen auf Betriebssystemversionen durchführen.</span><span class="sxs-lookup"><span data-stu-id="8dd15-143">Generally, applications should not perform operating system version checks.</span></span> <span data-ttu-id="8dd15-144">Wenn eine Anwendung eine bestimmte Funktion benötigt, empfiehlt es sich, das Feature zu finden, und es wird nur dann ein Fehler erzeugt, wenn die erforderliche Funktion fehlt.</span><span class="sxs-lookup"><span data-stu-id="8dd15-144">If an application needs a specific feature, it is preferable to try to find the feature, and fail only if the needed feature is missing.</span></span> <span data-ttu-id="8dd15-145">Anwendungen sollten mindestens Versionsnummern akzeptieren, die größer oder gleich der niedrigsten unterstützten Version des Betriebssystems sind.</span><span class="sxs-lookup"><span data-stu-id="8dd15-145">At a minimum, applications should always accept version numbers greater than or equal to the lowest supported version of the operating system.</span></span> <span data-ttu-id="8dd15-146">Ausnahmen sollten nur auftreten, wenn eine bestimmte gesetzliche, geschäftliche oder Systemkomponenten Anforderung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="8dd15-146">Exceptions should occur only if there is a specific legal, business, or system-component requirement.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="8dd15-147">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8dd15-147">Links to Other Resources</span></span>

-   [<span data-ttu-id="8dd15-148">Anwendungskompatibilitäts-Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="8dd15-148">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="8dd15-149">[Bekannte Kompatibilitäts Korrekturen, Kompatibilitäts Modi und AppHelp-Meldungen](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8dd15-149">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>

 

 
