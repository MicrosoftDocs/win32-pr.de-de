---
description: Nur 64-Bit
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Nur 64-Bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d896fcaf4b8c4ebeadf7cfd5a5c22e511cb659
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088808"
---
# <a name="64-bit-only"></a><span data-ttu-id="ef2fb-103">Nur 64-Bit</span><span class="sxs-lookup"><span data-stu-id="ef2fb-103">64-Bit Only</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="ef2fb-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="ef2fb-104">Affected Platforms</span></span>

<span data-ttu-id="ef2fb-105">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef2fb-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="ef2fb-106">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="ef2fb-106">Feature Impact</span></span>

 <span data-ttu-id="ef2fb-107">**Schweregrad:** Niedrig</span><span class="sxs-lookup"><span data-stu-id="ef2fb-107">**Severity** - Low</span></span>  
<span data-ttu-id="ef2fb-108">**Häufigkeit** – Hoch</span><span class="sxs-lookup"><span data-stu-id="ef2fb-108">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="ef2fb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef2fb-109">Description</span></span>

<span data-ttu-id="ef2fb-110">Windows Server 2008 R2 wird nur mit einer 64-Bit-SKU versendet. Für die Serverversion des Betriebssystems ist keine 32-Bit-SKU verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-110">Windows Server 2008 R2 ships with a 64-bit SKU only; no 32-bit SKU is available for the server version of the operating system.</span></span> <span data-ttu-id="ef2fb-111">Eine 32-Bit-SKU ist jedoch weiterhin für den Windows 7-Client verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-111">However, a 32-bit SKU continues to be available for the Windows 7 client.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="ef2fb-112">Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="ef2fb-112">Manifestation of Impact</span></span>

<span data-ttu-id="ef2fb-113">Dies wirkt sich auf drei Bereiche aus:</span><span class="sxs-lookup"><span data-stu-id="ef2fb-113">This will impact three areas:</span></span>

-   <span data-ttu-id="ef2fb-114">32-Bit-Treiber</span><span class="sxs-lookup"><span data-stu-id="ef2fb-114">32-bit drivers</span></span>
-   <span data-ttu-id="ef2fb-115">32-Bit-Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="ef2fb-115">32-bit plug-ins</span></span>
-   <span data-ttu-id="ef2fb-116">Ausführbare 16-Bit-Dateien</span><span class="sxs-lookup"><span data-stu-id="ef2fb-116">16-bit executables</span></span>

## <a name="solution-for-32-bit-drivers"></a><span data-ttu-id="ef2fb-117">Lösung für 32-Bit-Treiber</span><span class="sxs-lookup"><span data-stu-id="ef2fb-117">Solution for 32-bit Drivers</span></span>

<span data-ttu-id="ef2fb-118">Kompilieren Sie 32-Bit-Treiber als signierte 64-Bit-Treiber neu.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-118">Recompile 32-bit drivers as signed 64-bit drivers.</span></span>

## <a name="solution-for-32-bit-plug-ins"></a><span data-ttu-id="ef2fb-119">Lösung für 32-Bit-Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="ef2fb-119">Solution for 32-bit Plug-ins</span></span>

<span data-ttu-id="ef2fb-120">WoW64, ein x86-Emulator, ermöglicht die nahtlose Ausführung von Windows-basierten 32-Bit-Anwendungen unter 64-Bit-Windows.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-120">WoW64, an x86 emulator, allows 32-bit Windows-based applications to run seamlessly on 64-bit Windows.</span></span> <span data-ttu-id="ef2fb-121">WoW64 ist jetzt ein optionales Feature, das Sie installieren müssen, wenn 32-Bit-Code ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-121">WoW64 is now an optional feature that you must install if it is necessary to run 32-bit code.</span></span>

<span data-ttu-id="ef2fb-122">Das System isoliert 32-Bit-Anwendungen von 64-Bit-Anwendungen, einschließlich der Verhinderung von Datei- und Registrierungskonflikten.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-122">The system isolates 32-bit applications from 64-bit applications, which includes preventing file and registry collisions.</span></span> <span data-ttu-id="ef2fb-123">Konsolen-, GUI- und Dienstanwendungen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-123">Console, GUI, and service applications are supported.</span></span> <span data-ttu-id="ef2fb-124">Das System bietet Interoperabilität über die 32/64-Grenze hinweg für Szenarien wie Ausschneiden und Einfügen und COM.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-124">The system provides interoperability across the 32/64 boundary for scenarios such as cut and paste and COM.</span></span> <span data-ttu-id="ef2fb-125">32-Bit-Prozesse können jedoch keine 64-Bit-DLLs laden, und 64-Bit-Prozesse können keine 32-Bit-DLLs laden.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-125">However, 32-bit processes cannot load 64-bit DLLs, and 64-bit processes cannot load 32-bit DLLs.</span></span> <span data-ttu-id="ef2fb-126">Dies wird häufig in Shell-Plug-Ins angezeigt, die für Windows-Explorer geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-126">We commonly see this in shell plug-ins written for Windows Explorer.</span></span>

<span data-ttu-id="ef2fb-127">Eine 32-Bit-Anwendung kann erkennen, ob sie unter WOW64 ausgeführt wird, indem sie die IsWow64Process-Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-127">A 32-bit application can detect whether it is running under WOW64 by calling the IsWow64Process function.</span></span> <span data-ttu-id="ef2fb-128">Die Anwendung kann mithilfe der GetNativeSystemInfo-Funktion zusätzliche Informationen zum Prozessor abrufen.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-128">The application can obtain additional information about the processor by using the GetNativeSystemInfo function</span></span>

<span data-ttu-id="ef2fb-129">Beachten Sie, dass 64-Bit-Windows die Ausführung von 16-Bit-Windows-basierten Anwendungen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-129">Note that 64-bit Windows does not support running 16-bit Windows-based applications.</span></span> <span data-ttu-id="ef2fb-130">Der Hauptgrund dafür ist, dass Handles 32 signifikante Bits unter 64-Bit-Windows aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-130">The primary reason is that handles have 32 significant bits on 64-bit Windows.</span></span> <span data-ttu-id="ef2fb-131">Daher können Handles nicht abgeschnitten und ohne Datenverlust an 16-Bit-Anwendungen übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-131">Therefore, handles cannot be truncated and passed to 16-bit applications without loss of data.</span></span> <span data-ttu-id="ef2fb-132">Beim Starten von 16-Bit-Anwendungen tritt folgender Fehler auf: ERROR \_ BAD \_ EXE \_ FORMAT.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-132">Attempts to launch 16-bit applications fail with the following error: ERROR\_BAD\_EXE\_FORMAT.</span></span>

## <a name="solution-for-16-bit-executables"></a><span data-ttu-id="ef2fb-133">Lösung für ausführbare 16-Bit-Dateien</span><span class="sxs-lookup"><span data-stu-id="ef2fb-133">Solution for 16-bit Executables</span></span>

<span data-ttu-id="ef2fb-134">64-Bit-Windows erkennt eine begrenzte Anzahl bestimmter 16-Bit-Installationsprogrammprogramme und ersetzt eine portierte 32-Bit-Version.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-134">64-bit Windows recognizes a limited number of specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span> <span data-ttu-id="ef2fb-135">Die Liste der Ersetzungen wird in der Registrierung unter dem folgenden Schlüssel gespeichert: HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ NtVdm64 Es gibt integrierte Unterstützung für mehrere Installer-Engines, einschließlich InstallShield 5.x-Installationsprogramme.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-135">The list of substitutions is stored in the registry under the following key: HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64 There is built-in support for several installer engines, including InstallShield 5.x installers.</span></span> <span data-ttu-id="ef2fb-136">Beachten Sie, dass der 64-Bit-Windows Installer nahtlos 32-Bit-MSI-basierte Anwendungen unter 64-Bit-Windows installieren kann.</span><span class="sxs-lookup"><span data-stu-id="ef2fb-136">Note that the 64-bit Windows Installer can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="ef2fb-137">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ef2fb-137">Links to Other Resources</span></span>

-   [<span data-ttu-id="ef2fb-138">Ausführen von 32-Bit-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ef2fb-138">Running 32-bit Applications</span></span>](/windows/desktop/WinProg64/running-32-bit-applications)
-   [<span data-ttu-id="ef2fb-139">Leistung und Arbeitsspeicherverbrauch</span><span class="sxs-lookup"><span data-stu-id="ef2fb-139">Performance and Memory Consumption</span></span>](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [<span data-ttu-id="ef2fb-140">WOW64-Implementierungsdetails</span><span class="sxs-lookup"><span data-stu-id="ef2fb-140">WOW64 Implementation Details</span></span>](/windows/desktop/WinProg64/wow64-implementation-details)
-   [<span data-ttu-id="ef2fb-141">Registrierungsumleitung</span><span class="sxs-lookup"><span data-stu-id="ef2fb-141">Registry Redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
-   [<span data-ttu-id="ef2fb-142">Dateisystem-Redirector</span><span class="sxs-lookup"><span data-stu-id="ef2fb-142">File System Redirector</span></span>](/windows/desktop/WinProg64/file-system-redirector)
-   [<span data-ttu-id="ef2fb-143">Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="ef2fb-143">Memory Management</span></span>](/windows/desktop/WinProg64/memory-management)
-   [<span data-ttu-id="ef2fb-144">Prozessoraffinität</span><span class="sxs-lookup"><span data-stu-id="ef2fb-144">Processor Affinity</span></span>](/windows/desktop/WinProg64/processor-affinity)
-   [<span data-ttu-id="ef2fb-145">Prozessübergreifende Kommunikation</span><span class="sxs-lookup"><span data-stu-id="ef2fb-145">Interprocess Communication</span></span>](/windows/desktop/WinProg64/interprocess-communication)
-   [<span data-ttu-id="ef2fb-146">Anwendungsinstallation auf 64-Bit-Systemen</span><span class="sxs-lookup"><span data-stu-id="ef2fb-146">Application Installation on 64-bit Systems</span></span>](/windows/desktop/WinProg64/application-installation)
-   [<span data-ttu-id="ef2fb-147">Debuggen von WOW64</span><span class="sxs-lookup"><span data-stu-id="ef2fb-147">Debugging WOW64</span></span>](/windows/desktop/WinProg64/debugging-wow64)
-   [<span data-ttu-id="ef2fb-148">**IsWow64Process-Funktion**</span><span class="sxs-lookup"><span data-stu-id="ef2fb-148">**IsWow64Process Function**</span></span>](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [<span data-ttu-id="ef2fb-149">**GetNativeSystemInfo-Funktion**</span><span class="sxs-lookup"><span data-stu-id="ef2fb-149">**GetNativeSystemInfo Function**</span></span>](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
