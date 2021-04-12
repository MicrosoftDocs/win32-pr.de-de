---
description: .
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: nur 64-Bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3178a15ec0a138a73789233dd2d787964a96b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218496"
---
# <a name="64-bit-only"></a><span data-ttu-id="d580b-103">nur 64-Bit</span><span class="sxs-lookup"><span data-stu-id="d580b-103">64-Bit Only</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="d580b-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="d580b-104">Affected Platforms</span></span>

<span data-ttu-id="d580b-105">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d580b-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="d580b-106">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="d580b-106">Feature Impact</span></span>

 <span data-ttu-id="d580b-107">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="d580b-107">**Severity** - Low</span></span>  
<span data-ttu-id="d580b-108">**Häufigkeit** -hoch</span><span class="sxs-lookup"><span data-stu-id="d580b-108">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="d580b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d580b-109">Description</span></span>

<span data-ttu-id="d580b-110">Windows Server 2008 R2 ist nur mit einer 64-Bit-SKU ausgeliefert. für die Server Version des Betriebssystems ist keine 32-Bit-SKU verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d580b-110">Windows Server 2008 R2 ships with a 64-bit SKU only; no 32-bit SKU is available for the server version of the operating system.</span></span> <span data-ttu-id="d580b-111">Für den Windows 7-Client ist jedoch weiterhin eine 32-Bit-SKU verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d580b-111">However, a 32-bit SKU continues to be available for the Windows 7 client.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="d580b-112">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="d580b-112">Manifestation of Impact</span></span>

<span data-ttu-id="d580b-113">Dies wirkt sich auf drei Bereiche aus:</span><span class="sxs-lookup"><span data-stu-id="d580b-113">This will impact three areas:</span></span>

-   <span data-ttu-id="d580b-114">32-Bit-Treiber</span><span class="sxs-lookup"><span data-stu-id="d580b-114">32-bit drivers</span></span>
-   <span data-ttu-id="d580b-115">32-Bit-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="d580b-115">32-bit plug-ins</span></span>
-   <span data-ttu-id="d580b-116">ausführbare 16-Bit-Dateien</span><span class="sxs-lookup"><span data-stu-id="d580b-116">16-bit executables</span></span>

## <a name="solution-for-32-bit-drivers"></a><span data-ttu-id="d580b-117">Lösung für 32-Bit-Treiber</span><span class="sxs-lookup"><span data-stu-id="d580b-117">Solution for 32-bit Drivers</span></span>

<span data-ttu-id="d580b-118">Kompilieren Sie 32-Bit-Treiber als signierte 64-Bit-Treiber neu.</span><span class="sxs-lookup"><span data-stu-id="d580b-118">Recompile 32-bit drivers as signed 64-bit drivers.</span></span>

## <a name="solution-for-32-bit-plug-ins"></a><span data-ttu-id="d580b-119">Lösung für 32-Bit-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="d580b-119">Solution for 32-bit Plug-ins</span></span>

<span data-ttu-id="d580b-120">WOW64, ein x86-Emulator, ermöglicht das nahtlose Ausführen von Windows-basierten 32-Bit-Anwendungen auf 64-Bit-Fenstern.</span><span class="sxs-lookup"><span data-stu-id="d580b-120">WoW64, an x86 emulator, allows 32-bit Windows-based applications to run seamlessly on 64-bit Windows.</span></span> <span data-ttu-id="d580b-121">WOW64 ist jetzt ein optionales Feature, das Sie installieren müssen, wenn es erforderlich ist, 32-Bit-Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d580b-121">WoW64 is now an optional feature that you must install if it is necessary to run 32-bit code.</span></span>

<span data-ttu-id="d580b-122">Das System isoliert 32-Bit-Anwendungen von 64-Bit-Anwendungen, einschließlich der Vermeidung von Datei-und Registrierungs Kollisionen.</span><span class="sxs-lookup"><span data-stu-id="d580b-122">The system isolates 32-bit applications from 64-bit applications, which includes preventing file and registry collisions.</span></span> <span data-ttu-id="d580b-123">Konsolen-, GUI-und Dienst Anwendungen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d580b-123">Console, GUI, and service applications are supported.</span></span> <span data-ttu-id="d580b-124">Das System stellt Interoperabilität zwischen der 32/64-Grenze für Szenarien wie Ausschneiden, einfügen und com bereit.</span><span class="sxs-lookup"><span data-stu-id="d580b-124">The system provides interoperability across the 32/64 boundary for scenarios such as cut and paste and COM.</span></span> <span data-ttu-id="d580b-125">Allerdings können 32-Bit-Prozesse keine 64-Bit-DLLs laden, und 64-Bit-Prozesse können keine 32-Bit-DLLs laden.</span><span class="sxs-lookup"><span data-stu-id="d580b-125">However, 32-bit processes cannot load 64-bit DLLs, and 64-bit processes cannot load 32-bit DLLs.</span></span> <span data-ttu-id="d580b-126">Wir sehen dies häufig in Shell-Plug-ins, die für Windows Explorer geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="d580b-126">We commonly see this in shell plug-ins written for Windows Explorer.</span></span>

<span data-ttu-id="d580b-127">Eine 32-Bit-Anwendung kann erkennen, ob Sie unter WOW64 durch Aufrufen der IsWow64Process-Funktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d580b-127">A 32-bit application can detect whether it is running under WOW64 by calling the IsWow64Process function.</span></span> <span data-ttu-id="d580b-128">Die Anwendung kann zusätzliche Informationen über den Prozessor mithilfe der GetNativeSystemInfo-Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="d580b-128">The application can obtain additional information about the processor by using the GetNativeSystemInfo function</span></span>

<span data-ttu-id="d580b-129">Beachten Sie, dass 64-Bit-Windows die Ausführung von 16-Bit-Windows-basierten Anwendungen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d580b-129">Note that 64-bit Windows does not support running 16-bit Windows-based applications.</span></span> <span data-ttu-id="d580b-130">Der Hauptgrund ist, dass Handles 32 signifikante Bits auf 64-Bit-Fenstern aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d580b-130">The primary reason is that handles have 32 significant bits on 64-bit Windows.</span></span> <span data-ttu-id="d580b-131">Daher können Handles nicht abgeschnitten und ohne Datenverlust an 16-Bit-Anwendungen übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="d580b-131">Therefore, handles cannot be truncated and passed to 16-bit applications without loss of data.</span></span> <span data-ttu-id="d580b-132">Der Versuch, 16-Bit-Anwendungen zu starten, schlägt mit folgendem Fehler fehl: fehlerhafte \_ \_ exe- \_ Format.</span><span class="sxs-lookup"><span data-stu-id="d580b-132">Attempts to launch 16-bit applications fail with the following error: ERROR\_BAD\_EXE\_FORMAT.</span></span>

## <a name="solution-for-16-bit-executables"></a><span data-ttu-id="d580b-133">Lösung für ausführbare 16-Bit-Dateien</span><span class="sxs-lookup"><span data-stu-id="d580b-133">Solution for 16-bit Executables</span></span>

<span data-ttu-id="d580b-134">64-Bit-Windows erkennt eine begrenzte Anzahl spezifischer Programme mit 16-Bit-Installer und ersetzt eine portierte 32-Bit-Version.</span><span class="sxs-lookup"><span data-stu-id="d580b-134">64-bit Windows recognizes a limited number of specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span> <span data-ttu-id="d580b-135">Die Liste der Substitutionen wird in der Registrierung unter folgendem Schlüssel gespeichert: HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64 es gibt integrierte Unterstützung für mehrere Installer-Engines, einschließlich InstallShield 5. x-Installer.</span><span class="sxs-lookup"><span data-stu-id="d580b-135">The list of substitutions is stored in the registry under the following key: HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64 There is built-in support for several installer engines, including InstallShield 5.x installers.</span></span> <span data-ttu-id="d580b-136">Beachten Sie, dass der 64-Bit-Windows Installer die auf 32-Bit-MSI basierende Anwendungen nahtlos auf 64-Bit-Windows installieren kann.</span><span class="sxs-lookup"><span data-stu-id="d580b-136">Note that the 64-bit Windows Installer can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="d580b-137">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d580b-137">Links to Other Resources</span></span>

-   [<span data-ttu-id="d580b-138">Ausführen von 32-Bit-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d580b-138">Running 32-bit Applications</span></span>](/windows/desktop/WinProg64/running-32-bit-applications)
-   [<span data-ttu-id="d580b-139">Leistung und Arbeitsspeicher Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d580b-139">Performance and Memory Consumption</span></span>](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [<span data-ttu-id="d580b-140">WOW64-Implementierungs Details</span><span class="sxs-lookup"><span data-stu-id="d580b-140">WOW64 Implementation Details</span></span>](/windows/desktop/WinProg64/wow64-implementation-details)
-   [<span data-ttu-id="d580b-141">Registrierungs Redirector</span><span class="sxs-lookup"><span data-stu-id="d580b-141">Registry Redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
-   [<span data-ttu-id="d580b-142">Datei System-Redirector</span><span class="sxs-lookup"><span data-stu-id="d580b-142">File System Redirector</span></span>](/windows/desktop/WinProg64/file-system-redirector)
-   [<span data-ttu-id="d580b-143">Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="d580b-143">Memory Management</span></span>](/windows/desktop/WinProg64/memory-management)
-   [<span data-ttu-id="d580b-144">Prozessoraffinität</span><span class="sxs-lookup"><span data-stu-id="d580b-144">Processor Affinity</span></span>](/windows/desktop/WinProg64/processor-affinity)
-   [<span data-ttu-id="d580b-145">Prozessübergreifende Kommunikation</span><span class="sxs-lookup"><span data-stu-id="d580b-145">Interprocess Communication</span></span>](/windows/desktop/WinProg64/interprocess-communication)
-   [<span data-ttu-id="d580b-146">Anwendungs Installation auf 64-Bit-Systemen</span><span class="sxs-lookup"><span data-stu-id="d580b-146">Application Installation on 64-bit Systems</span></span>](/windows/desktop/WinProg64/application-installation)
-   [<span data-ttu-id="d580b-147">Debuggen WOW64</span><span class="sxs-lookup"><span data-stu-id="d580b-147">Debugging WOW64</span></span>](/windows/desktop/WinProg64/debugging-wow64)
-   [<span data-ttu-id="d580b-148">**IsWow64Process-Funktion**</span><span class="sxs-lookup"><span data-stu-id="d580b-148">**IsWow64Process Function**</span></span>](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [<span data-ttu-id="d580b-149">**GetNativeSystemInfo-Funktion**</span><span class="sxs-lookup"><span data-stu-id="d580b-149">**GetNativeSystemInfo Function**</span></span>](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
