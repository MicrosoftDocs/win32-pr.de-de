---
description: In diesem Abschnitt wird beschrieben, wie Sie bestimmen können, auf welcher Version der Shell-DLLs Ihre Anwendung ausgeführt wird und wie Sie Ihre Anwendung für eine bestimmte Version als Ziel festlegen.
title: 'Shell- und Shlwapi-DLL-Versionen '
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 49fb1767b7074da6480a47c52eb1384fb935317b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215930"
---
# <a name="shell-and-shlwapi-dll-versions"></a><span data-ttu-id="11c23-103">Shell- und Shlwapi-DLL-Versionen </span><span class="sxs-lookup"><span data-stu-id="11c23-103">Shell and Shlwapi DLL Versions</span></span>

<span data-ttu-id="11c23-104">In diesem Abschnitt wird beschrieben, wie Sie bestimmen können, auf welcher Version der Shell-DLLs Ihre Anwendung ausgeführt wird und wie Sie Ihre Anwendung für eine bestimmte Version als Ziel festlegen.</span><span class="sxs-lookup"><span data-stu-id="11c23-104">This section describes how to determine which version of the Shell DLLs your application is running on and how to target your application for a specific version.</span></span>

-   [<span data-ttu-id="11c23-105">DLL-Versionsnummern</span><span class="sxs-lookup"><span data-stu-id="11c23-105">DLL Version Numbers</span></span>](#dll-version-numbers)
-   [<span data-ttu-id="11c23-106">Verwenden von dllgetversion zum Ermitteln der Versionsnummer</span><span class="sxs-lookup"><span data-stu-id="11c23-106">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
    -   [<span data-ttu-id="11c23-107">Verwenden von "dllgetversion"</span><span class="sxs-lookup"><span data-stu-id="11c23-107">Using DllGetVersion</span></span>](#using-dllgetversion)
-   [<span data-ttu-id="11c23-108">Projekt Versionen</span><span class="sxs-lookup"><span data-stu-id="11c23-108">Project Versions</span></span>](#project-versions)

## <a name="dll-version-numbers"></a><span data-ttu-id="11c23-109">DLL-Versionsnummern</span><span class="sxs-lookup"><span data-stu-id="11c23-109">DLL Version Numbers</span></span>

<span data-ttu-id="11c23-110">Die in der shelldokumentation erörterten Programmier Elemente sind in zwei DLLs enthalten: Shell32.dll und Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="11c23-110">All but a handful of the programming elements discussed in the Shell documentation are contained in two DLLs: Shell32.dll and Shlwapi.dll.</span></span> <span data-ttu-id="11c23-111">Aufgrund von kontinuierlichen Verbesserungen implementieren verschiedene Versionen dieser DLLs verschiedene Funktionen.</span><span class="sxs-lookup"><span data-stu-id="11c23-111">Because of ongoing enhancements, different versions of these DLLs implement different features.</span></span> <span data-ttu-id="11c23-112">In der gesamten shellverweisdokumentation gibt jedes Programmier Element eine unterstützte dll-Versionsnummer an.</span><span class="sxs-lookup"><span data-stu-id="11c23-112">Throughout the Shell reference documentation, each programming element specifies a minimum supported DLL version number.</span></span> <span data-ttu-id="11c23-113">Diese Versionsnummer gibt an, dass das Programmier Element in dieser Version und in nachfolgenden Versionen der dll implementiert ist, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="11c23-113">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="11c23-114">Wenn keine Versionsnummer angegeben ist, wird das Programmier Element in allen vorhandenen Versionen der dll implementiert.</span><span class="sxs-lookup"><span data-stu-id="11c23-114">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="11c23-115">Vor Windows XP wurden neue Shell32.dll und Shlwapi.dll Versionen in einigen Fällen mit neuen Versionen von Windows Internet Explorer bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="11c23-115">Before Windows XP, new Shell32.dll and Shlwapi.dll versions were sometimes provided with new versions of Windows Internet Explorer.</span></span> <span data-ttu-id="11c23-116">Ab Windows XP wurden diese DLLs nicht mehr als verteilbare Dateien außerhalb neuer Versionen von Windows selbst bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="11c23-116">As of Windows XP, those DLLs were no longer provided as redistributable files outside of new versions of Windows itself.</span></span> <span data-ttu-id="11c23-117">In der folgenden Tabelle werden die verschiedenen dll-Versionen und deren Verteilung auf den Microsoft Internet Explorer 3,0, Windows 95 und Microsoft Windows NT 4,0 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="11c23-117">The following table outlines the different DLL versions and how they were distributed dating back to Microsoft Internet Explorer 3.0, Windows 95, and Microsoft Windows NT 4.0.</span></span>

<span data-ttu-id="11c23-118">Shell32.dll Version 4,0 wurde in den ursprünglichen Versionen von Windows 95 und Microsoft Windows NT 4,0 gefunden.</span><span class="sxs-lookup"><span data-stu-id="11c23-118">Shell32.dll version 4.0 is found in the original versions of Windows 95 and Microsoft Windows NT 4.0.</span></span> <span data-ttu-id="11c23-119">Die Shell wurde nicht mit der Version Internet Explorer 3,0 aktualisiert, sodass Shell32.dll nicht über die Version 4,70 verfügt.</span><span class="sxs-lookup"><span data-stu-id="11c23-119">The Shell was not updated with the Internet Explorer 3.0 release, so Shell32.dll does not have a version 4.70.</span></span> <span data-ttu-id="11c23-120">Shell32.dll Versionen 4,71 und 4,72 waren mit den entsprechenden Internet Explorer-Releases ausgeliefert, aber Sie wurden nicht notwendigerweise installiert (siehe Hinweis 1).</span><span class="sxs-lookup"><span data-stu-id="11c23-120">Shell32.dll versions 4.71 and 4.72 were shipped with the corresponding Internet Explorer releases, but they were not necessarily installed (see note 1).</span></span> <span data-ttu-id="11c23-121">Bei Releases nach Microsoft Internet Explorer 4,01 und Windows 98 sind die Versionsnummern für Shell32.dll und Shlwapi.dll voneinander abweicht.</span><span class="sxs-lookup"><span data-stu-id="11c23-121">For releases subsequent to Microsoft Internet Explorer 4.01 and Windows 98, the version numbers for Shell32.dll and Shlwapi.dll diverge.</span></span> <span data-ttu-id="11c23-122">Im Allgemeinen sollten Sie davon ausgehen, dass die DLLs über unterschiedliche Versionsnummern verfügen, und jede einzelne einzeln testen.</span><span class="sxs-lookup"><span data-stu-id="11c23-122">In general, you should assume that the DLLs have different version numbers and test each one separately.</span></span>

#### <a name="shell32dll"></a><span data-ttu-id="11c23-123">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="11c23-123">Shell32.dll</span></span>

| <span data-ttu-id="11c23-124">Version</span><span class="sxs-lookup"><span data-stu-id="11c23-124">Version</span></span> | <span data-ttu-id="11c23-125">Verteilungs Plattform</span><span class="sxs-lookup"><span data-stu-id="11c23-125">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="11c23-126">4,0</span><span class="sxs-lookup"><span data-stu-id="11c23-126">4.0</span></span>     | <span data-ttu-id="11c23-127">Windows 95 und Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="11c23-127">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="11c23-128">4.71</span><span class="sxs-lookup"><span data-stu-id="11c23-128">4.71</span></span>    | <span data-ttu-id="11c23-129">Microsoft Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="11c23-129">Microsoft Internet Explorer 4.0.</span></span> <span data-ttu-id="11c23-130">(siehe Hinweis 1).</span><span class="sxs-lookup"><span data-stu-id="11c23-130">See note 1.</span></span>                                |
| <span data-ttu-id="11c23-131">4.72</span><span class="sxs-lookup"><span data-stu-id="11c23-131">4.72</span></span>    | <span data-ttu-id="11c23-132">Internet Explorer 4,01 und Windows 98.</span><span class="sxs-lookup"><span data-stu-id="11c23-132">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="11c23-133">(siehe Hinweis 1).</span><span class="sxs-lookup"><span data-stu-id="11c23-133">See note 1.</span></span>                          |
| <span data-ttu-id="11c23-134">5.0</span><span class="sxs-lookup"><span data-stu-id="11c23-134">5.0</span></span>     | <span data-ttu-id="11c23-135">Windows 2000 und Windows Millennium Edition (Windows Me).</span><span class="sxs-lookup"><span data-stu-id="11c23-135">Windows 2000 and Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="11c23-136">Siehe Hinweis 2.</span><span class="sxs-lookup"><span data-stu-id="11c23-136">See note 2.</span></span>       |
| <span data-ttu-id="11c23-137">6.0</span><span class="sxs-lookup"><span data-stu-id="11c23-137">6.0</span></span>     | <span data-ttu-id="11c23-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="11c23-138">Windows XP</span></span>                                                                  |
| <span data-ttu-id="11c23-139">6.0.1</span><span class="sxs-lookup"><span data-stu-id="11c23-139">6.0.1</span></span>   | <span data-ttu-id="11c23-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11c23-140">Windows Vista</span></span>                                                               |
| <span data-ttu-id="11c23-141">6.1</span><span class="sxs-lookup"><span data-stu-id="11c23-141">6.1</span></span>     | <span data-ttu-id="11c23-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="11c23-142">Windows 7</span></span>                                                                   |

#### <a name="shlwapidll"></a><span data-ttu-id="11c23-143">Shlwapi.dll</span><span class="sxs-lookup"><span data-stu-id="11c23-143">Shlwapi.dll</span></span>

| <span data-ttu-id="11c23-144">Version</span><span class="sxs-lookup"><span data-stu-id="11c23-144">Version</span></span> | <span data-ttu-id="11c23-145">Verteilungs Plattform</span><span class="sxs-lookup"><span data-stu-id="11c23-145">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="11c23-146">4,0</span><span class="sxs-lookup"><span data-stu-id="11c23-146">4.0</span></span>     | <span data-ttu-id="11c23-147">Windows 95 und Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="11c23-147">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="11c23-148">4.71</span><span class="sxs-lookup"><span data-stu-id="11c23-148">4.71</span></span>    | <span data-ttu-id="11c23-149">Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="11c23-149">Internet Explorer 4.0.</span></span> <span data-ttu-id="11c23-150">(siehe Hinweis 1).</span><span class="sxs-lookup"><span data-stu-id="11c23-150">See note 1.</span></span>                                          |
| <span data-ttu-id="11c23-151">4.72</span><span class="sxs-lookup"><span data-stu-id="11c23-151">4.72</span></span>    | <span data-ttu-id="11c23-152">Internet Explorer 4,01 und Windows 98.</span><span class="sxs-lookup"><span data-stu-id="11c23-152">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="11c23-153">(siehe Hinweis 1).</span><span class="sxs-lookup"><span data-stu-id="11c23-153">See note 1.</span></span>                          |
| <span data-ttu-id="11c23-154">4,7</span><span class="sxs-lookup"><span data-stu-id="11c23-154">4.7</span></span>     | <span data-ttu-id="11c23-155">Internet Explorer 3. x</span><span class="sxs-lookup"><span data-stu-id="11c23-155">Internet Explorer 3.x</span></span>                                                       |
| <span data-ttu-id="11c23-156">5.0</span><span class="sxs-lookup"><span data-stu-id="11c23-156">5.0</span></span>     | <span data-ttu-id="11c23-157">Microsoft Internet Explorer 5 und Windows 98 SE.</span><span class="sxs-lookup"><span data-stu-id="11c23-157">Microsoft Internet Explorer 5 and Windows 98 SE.</span></span> <span data-ttu-id="11c23-158">Siehe Hinweis 2.</span><span class="sxs-lookup"><span data-stu-id="11c23-158">See note 2.</span></span>                |
| <span data-ttu-id="11c23-159">5.5</span><span class="sxs-lookup"><span data-stu-id="11c23-159">5.5</span></span>     | <span data-ttu-id="11c23-160">Microsoft Internet Explorer 5,5 und Windows Millennium Edition (Windows Me)</span><span class="sxs-lookup"><span data-stu-id="11c23-160">Microsoft Internet Explorer 5.5 and Windows Millennium Edition (Windows Me)</span></span> |
| <span data-ttu-id="11c23-161">6.0</span><span class="sxs-lookup"><span data-stu-id="11c23-161">6.0</span></span>     | <span data-ttu-id="11c23-162">Windows XP und Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11c23-162">Windows XP and Windows Vista</span></span>                                                |



<span data-ttu-id="11c23-163">**Hinweis 1:** Alle Systeme mit Internet Explorer 4,0 oder 4,01 verfügten über die zugehörige Version von Shlwapi.dll (4,71 oder 4,72).</span><span class="sxs-lookup"><span data-stu-id="11c23-163">**Note 1:** All systems with Internet Explorer 4.0 or 4.01 had the associated version of Shlwapi.dll (4.71 or 4.72, respectively).</span></span> <span data-ttu-id="11c23-164">Allerdings können Internet Explorer 4,0 und 4,01 für Systeme vor Windows 98 mit oder ohne die so genannte *integrierte Shell* installiert werden.</span><span class="sxs-lookup"><span data-stu-id="11c23-164">However, for systems prior to Windows 98, Internet Explorer 4.0 and 4.01 can be installed with or without what was known as the *integrated Shell*.</span></span> <span data-ttu-id="11c23-165">Wenn Internet Explorer mit der integrierten Shell installiert wurde, wurde auch die zugehörige Version von Shell32.dll (4,71 oder 4,72) installiert.</span><span class="sxs-lookup"><span data-stu-id="11c23-165">If Internet Explorer was installed with the integrated Shell, the associated version of Shell32.dll (4.71 or 4.72) was also installed.</span></span> <span data-ttu-id="11c23-166">Wenn Internet Explorer ohne die integrierte Shell installiert wurde, Shell32.dll als Version 4,0 geblieben.</span><span class="sxs-lookup"><span data-stu-id="11c23-166">If Internet Explorer was installed without the integrated Shell, Shell32.dll remained as version 4.0.</span></span> <span data-ttu-id="11c23-167">Anders ausgedrückt bedeutet das vorhanden sein von Version 4,71 oder 4,72 von Shlwapi.dll auf einem System nicht, dass Shell32.dll die gleiche Versionsnummer hat.</span><span class="sxs-lookup"><span data-stu-id="11c23-167">In other words, the presence of version 4.71 or 4.72 of Shlwapi.dll on a system does not guarantee that Shell32.dll has the same version number.</span></span> <span data-ttu-id="11c23-168">Alle Windows 98-Systeme verfügen über die Version 4,72 von Shell32.dll.</span><span class="sxs-lookup"><span data-stu-id="11c23-168">All Windows 98 systems have version 4.72 of Shell32.dll.</span></span>

<span data-ttu-id="11c23-169">**Hinweis 2:** Die Version 5,0 von Shlwapi.dll wurde mit Internet Explorer 5 verteilt und wurde auf allen Systemen gefunden, auf denen Internet Explorer 5 installiert war, mit Ausnahme von Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="11c23-169">**Note 2:** Version 5.0 of Shlwapi.dll was distributed with Internet Explorer 5 and was found on all systems on which Internet Explorer 5 was installed, with the exception of Windows 2000.</span></span> <span data-ttu-id="11c23-170">Die Version 5,0 von Shell32.dll wurde nativ mit Windows 2000 und Windows Millennium Edition (Windows Me) zusammen mit Version 5,0 Shlwapi.dll verteilt.</span><span class="sxs-lookup"><span data-stu-id="11c23-170">Version 5.0 of Shell32.dll was distributed natively with Windows 2000 and Windows Millennium Edition (Windows Me), together with version 5.0 of Shlwapi.dll.</span></span>

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="11c23-171">Verwenden von dllgetversion zum Ermitteln der Versionsnummer</span><span class="sxs-lookup"><span data-stu-id="11c23-171">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="11c23-172">Ab Version 4,71 haben die shelldlls unter anderem begonnen, [**dllgetversion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc)zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="11c23-172">Starting with version 4.71, the Shell DLLs, among others, began exporting [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="11c23-173">Diese Funktion kann von einer Anwendung aufgerufen werden, um zu bestimmen, welche DLL-Version auf dem System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="11c23-173">This function can be called by an application to determine which DLL version is present on the system.</span></span>

> [!Note]  
> <span data-ttu-id="11c23-174">DLLs exportieren nicht notwendigerweise [**dllgetversion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="11c23-174">DLLs do not necessarily export [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="11c23-175">Testen Sie Sie immer, bevor Sie versuchen, Sie zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="11c23-175">Always test for it before attempting to use it.</span></span>

<span data-ttu-id="11c23-176">Bei Windows-Versionen vor Windows 2000 gibt [**dllgetversion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) eine [**dllversioninfo**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) -Struktur zurück, die die Haupt-und neben Versionsnummern, die Buildnummer und eine Platt Form-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="11c23-176">For Windows versions earlier than Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure that contains the major and minor version numbers, the build number, and a platform ID.</span></span> <span data-ttu-id="11c23-177">Für Windows 2000-Systeme und spätere Systeme gibt **dllgetversion** möglicherweise stattdessen eine [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="11c23-177">For Windows 2000 and later systems, **DllGetVersion** might instead return a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="11c23-178">Zusätzlich zu den Informationen, die über **dllversioninfo** bereitgestellt werden, stellt **DLLVERSIONINFO2** auch die Hotfixnummer bereit, mit der die neuesten installierten Service Pack identifiziert werden, die eine stabilere Möglichkeit zum Vergleichen von Versionsnummern bietet.</span><span class="sxs-lookup"><span data-stu-id="11c23-178">In addition to the information provided through **DLLVERSIONINFO**, **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="11c23-179">Da der erste Member von **DLLVERSIONINFO2** eine **dllversioninfo** -Struktur ist, ist die spätere Struktur abwärts kompatibel.</span><span class="sxs-lookup"><span data-stu-id="11c23-179">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>

### <a name="using-dllgetversion"></a><span data-ttu-id="11c23-180">Verwenden von "dllgetversion"</span><span class="sxs-lookup"><span data-stu-id="11c23-180">Using DllGetVersion</span></span>

<span data-ttu-id="11c23-181">Die folgende Beispiel Funktion `GetVersion` lädt eine angegebene DLL und versucht, Ihre [**dllgetversion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="11c23-181">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="11c23-182">Wenn erfolgreich, wird ein Makro verwendet, um die Haupt-und neben Versionsnummern aus der [**dllversioninfo**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) -Struktur in ein **DWORD** zu packen, das an die aufrufenden Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="11c23-182">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="11c23-183">Wenn die DLL **dllgetversion** nicht exportiert, gibt die Funktion 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="11c23-183">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="11c23-184">Mit Windows 2000 und neueren Systemen können Sie die Funktion ändern, um die Möglichkeit zu verarbeiten, dass **dllgetversion** eine [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) -Struktur zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="11c23-184">With Windows 2000 and later systems, you can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="11c23-185">Wenn dies der Fall ist, verwenden Sie die Informationen im **ullversion** -Member der **DLLVERSIONINFO2** -Struktur, um Versionen, Buildnummern und Service Pack Releases zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="11c23-185">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="11c23-186">Das [**makedllverull**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) -Makro vereinfacht die Aufgabe, diese Werte mit den Werten in **ullversion** zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="11c23-186">The [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="11c23-187">Das nicht ordnungsgemäße Verwenden von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann Sicherheitsrisiken darstellen.</span><span class="sxs-lookup"><span data-stu-id="11c23-187">Using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="11c23-188">Informationen zum ordnungsgemäßen Laden von DLLs mit unterschiedlichen Versionen von Windows finden Sie in der Dokumentation zu **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="11c23-188">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


<span data-ttu-id="11c23-189">Im folgenden Codebeispiel wird veranschaulicht, wie Sie `GetVersion` mit überprüfen können, ob Shell32.dll die Version 6,0 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="11c23-189">The following code example illustrates how you can use `GetVersion` to test whether Shell32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a><span data-ttu-id="11c23-190">Projekt Versionen</span><span class="sxs-lookup"><span data-stu-id="11c23-190">Project Versions</span></span>

<span data-ttu-id="11c23-191">Um sicherzustellen, dass Ihre Anwendung mit unterschiedlichen Ziel Versionen einer DLL-Datei kompatibel ist, sind Versions Makros in den Header Dateien vorhanden.</span><span class="sxs-lookup"><span data-stu-id="11c23-191">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="11c23-192">Diese Makros werden verwendet, um bestimmte Definitionen für verschiedene Versionen der dll zu definieren, auszuschließen oder neu zu definieren.</span><span class="sxs-lookup"><span data-stu-id="11c23-192">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="11c23-193">Eine ausführliche Beschreibung dieser Makros finden [Sie unter Verwenden der Windows-Header](../winprog/using-the-windows-headers.md) .</span><span class="sxs-lookup"><span data-stu-id="11c23-193">See [Using the Windows Headers](../winprog/using-the-windows-headers.md) for an in-depth description of these macros.</span></span>

<span data-ttu-id="11c23-194">Beispielsweise befindet sich der Makro Name **\_ Win32 \_ IE** häufig in älteren Headern.</span><span class="sxs-lookup"><span data-stu-id="11c23-194">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="11c23-195">Sie sind dafür verantwortlich, das Makro als hexadezimale Zahl zu definieren.</span><span class="sxs-lookup"><span data-stu-id="11c23-195">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="11c23-196">Diese Versionsnummer definiert die Zielversion der Anwendung, die die dll verwendet.</span><span class="sxs-lookup"><span data-stu-id="11c23-196">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="11c23-197">In der folgenden Tabelle sind die verfügbaren Versionsnummern und die Auswirkungen der einzelnen Anwendungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="11c23-197">The following table shows the available version numbers and the effect each has on your application.</span></span>


| <span data-ttu-id="11c23-198">Version</span><span class="sxs-lookup"><span data-stu-id="11c23-198">Version</span></span> | <span data-ttu-id="11c23-199">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11c23-199">Description</span></span>                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c23-200">0x0200</span><span class="sxs-lookup"><span data-stu-id="11c23-200">0x0200</span></span>  | <span data-ttu-id="11c23-201">Die Anwendung ist kompatibel mit Shell32.dll Version 4,00 und höher.</span><span class="sxs-lookup"><span data-stu-id="11c23-201">The application is compatible with Shell32.dll version 4.00 and later.</span></span> <span data-ttu-id="11c23-202">Die Anwendung kann keine Features implementieren, die nach Version 4,00 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="11c23-202">The application cannot implement features that were added after version 4.00.</span></span>                                              |
| <span data-ttu-id="11c23-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="11c23-203">0x0300</span></span>  | <span data-ttu-id="11c23-204">Die Anwendung ist kompatibel mit Shell32.dll Version 4,70 und höher.</span><span class="sxs-lookup"><span data-stu-id="11c23-204">The application is compatible with Shell32.dll version 4.70 and later.</span></span> <span data-ttu-id="11c23-205">Die Anwendung kann keine Features implementieren, die nach Version 4,70 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="11c23-205">The application cannot implement features that were added after version 4.70.</span></span>                                              |
| <span data-ttu-id="11c23-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="11c23-206">0x0400</span></span>  | <span data-ttu-id="11c23-207">Die Anwendung ist kompatibel mit Shell32.dll Version 4,71 und höher.</span><span class="sxs-lookup"><span data-stu-id="11c23-207">The application is compatible with Shell32.dll version 4.71 and later.</span></span> <span data-ttu-id="11c23-208">Die Anwendung kann keine Features implementieren, die nach Version 4,71 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="11c23-208">The application cannot implement features that were added after version 4.71.</span></span>                                              |
| <span data-ttu-id="11c23-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="11c23-209">0x0401</span></span>  | <span data-ttu-id="11c23-210">Die Anwendung ist kompatibel mit Shell32.dll Version 4,72 und höher.</span><span class="sxs-lookup"><span data-stu-id="11c23-210">The application is compatible with Shell32.dll version 4.72 and later.</span></span> <span data-ttu-id="11c23-211">Die Anwendung kann keine Features implementieren, die nach Version 4,72 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="11c23-211">The application cannot implement features that were added after version 4.72.</span></span>                                              |
| <span data-ttu-id="11c23-212">0x0500 sein</span><span class="sxs-lookup"><span data-stu-id="11c23-212">0x0500</span></span>  | <span data-ttu-id="11c23-213">Die Anwendung ist kompatibel mit Shell32.dll und Shlwapi.dll Version 5,0 und höher.</span><span class="sxs-lookup"><span data-stu-id="11c23-213">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="11c23-214">Die Anwendung kann keine Features implementieren, die nach Version 5,0 von Shell32.dll und Shlwapi.dll hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="11c23-214">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="11c23-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="11c23-215">0x0501</span></span>  | <span data-ttu-id="11c23-216">Die Anwendung ist kompatibel mit Shell32.dll und Shlwapi.dll Version 5,0 und höher.</span><span class="sxs-lookup"><span data-stu-id="11c23-216">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="11c23-217">Die Anwendung kann keine Features implementieren, die nach Version 5,0 von Shell32.dll und Shlwapi.dll hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="11c23-217">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="11c23-218">0x0600 sein</span><span class="sxs-lookup"><span data-stu-id="11c23-218">0x0600</span></span>  | <span data-ttu-id="11c23-219">Die Anwendung ist kompatibel mit Shell32.dll und Shlwapi.dll Version 6,0 und höher.</span><span class="sxs-lookup"><span data-stu-id="11c23-219">The application is compatible with Shell32.dll and Shlwapi.dll version 6.0 and later.</span></span> <span data-ttu-id="11c23-220">Die Anwendung kann keine Features implementieren, die nach Version 6,0 von Shell32.dll und Shlwapi.dll hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="11c23-220">The application cannot implement features that were added after version 6.0 of Shell32.dll and Shlwapi.dll.</span></span> |


<span data-ttu-id="11c23-221">Wenn Sie das **\_ Win32- \_ IE** -Makro nicht in Ihrem Projekt definieren, wird es automatisch als 0x0500 definiert.</span><span class="sxs-lookup"><span data-stu-id="11c23-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="11c23-222">Wenn Sie einen anderen Wert definieren möchten, können Sie den Compilerdirektiven in ihrer Make-Datei Folgendes hinzufügen: Ersetzen Sie die gewünschte Versionsnummer für 0x0400.</span><span class="sxs-lookup"><span data-stu-id="11c23-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>

```
/D _WIN32_IE=0x0400
```

<span data-ttu-id="11c23-223">Eine andere Methode ist das Hinzufügen einer Zeile ähnlich der folgenden in Ihrem Quellcode, bevor Sie die shellheaderdateien einschließen.</span><span class="sxs-lookup"><span data-stu-id="11c23-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="11c23-224">Ersetzen Sie die gewünschte Versionsnummer für 0x0400.</span><span class="sxs-lookup"><span data-stu-id="11c23-224">Substitute the desired version number for 0x0400.</span></span>

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
